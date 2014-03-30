***Scribe*** is a server for aggregating streaming log data. It is designed to scale
to a very large number of nodes and be robust to network and node failures.
There is a scribe server runing on every node in the system, configured to
aggregare messages and send them to a central scribe server (or servers) in
larger groups. If the central scribe server isn't available the local scribe
server writes the messages to the files that are their final destination,
typically on an nfs filer or a distributed filesystem, or send them to another
layer scribe servers.

Scribe is unique in that clients log entries consisiting of two strings, a
category and a message. The category is a high level description of the
intended destination of the message and can have a specific configuration in
the scribe server, which allows data stores to be moved by changing the scribe
configuration instead of client code. The server also allows for
configurations based on category prefix, and a default configuration that can
insert the category name in the file path. Flexibility and extensibility is
provided through the "store" abstraction. Stores are loaded dynamically based
on a configuration file, and can be changed at runtime without stopping the
server. Stores are implemented as a class hierarchy, and stores can contain
other stores. This allows a user to chain features together in different
orders and combinations by changing only the configuration.

Scribe is implemented as a thrift service using the non-blocking C++ server.
The installation at Facebook runs on thousands of machines and reliably
delivers tens of billions of messages a day.
