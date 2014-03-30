In computer science, the event loop, message dispatcher, message loop, message
pump, or run loop is a programming construct that waits for and dispatches
events or messages in a program. It works by making a request to some internal
or external "event provider" (which generally blocks the request untill an
event has arrived), and then it calls the relevant event handler ("dispatches
the event"). The event-loop may be used in conjunction with a reactor, if the
event provider follows the file interface, which can be selected or 'polled'
(the Unix system call, not actual polling). The event loop almost always
operates asynchronously with the message originator. When the event loop forms
the central control flow construct of a program, as it often does, it may be
termed the main loop or main event loop. This title is appropriate because
such an event loop is at the highest level of control within the program.

### Message passing

Message pumps are said to 'pump' messages from the program's message queue
(assigned and usually owned by the underlying operating system) into the
program for processing. In the strictest sense, an event loop is one of the
methods for implementing inter-process communication. In fact, message
processing exists in many systems, including a kernel-level component of the
Mach operating system. The event loop is a specific implementation technique
of systems that use message passing.

### Alternative designs

This approach is in contrast to a number of other alternatives:
Traditionally, a program simply ran once then terminated. This type of program
was very common in the early days of computing, and lacked any form of user
interactivity. This is still used frequently, particularly in the form of
command line driven programs. Any parameters are set up in advance and passed
in one go when the program starts.
Menu-driven designs. These still may feature a main loop but are not usually
thought of as event driven in the usual sense. Instead, the user is presented
with an ever-narrowing set of options until the task they wish to carry out is
the only option available. Limited interactivity through the menus is
available.

### Usage
