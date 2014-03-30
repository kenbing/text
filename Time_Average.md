One of the most common question we hear from customers is, "How will
Optimizely affect my page's load time?" They have good reason. Page load time
has never been more important. Pages with faster response times reduce bounce
rate and they can even improve your ranking in Google searches.

Any third party code snippet you add to a web page will impact its overall load
time. This is because, in most cases. the third party code needs to finish
loading before the rest of the page can begin to load. If the vendor providing
the code is doing a good job, that impact should be so small that your
visitors don't notice it at all.

Some vendors attempt to mitigate impact on load times by providing an
asynchronous code snippet--in other words, a snippet that loads simultaneously
with the rest of the page. This is primarily used for background services,
like Google Analytics, where the code isn't making a visible change to the
page. In most cases, it isn't appropriate to load the code snippet for an A/B
testing platform like Optimizely asynchronously. This is because parts of the
page may load before the snippet, causing the user to see the original page
flash on the page and then change to the appropriate variation. that's why we
recommend including the Optimizely snippet at the beginning of the head tag.
some vendors provide timeout thresholds to prevent this from happening, but
doing so limits your sample size to visitors within a caertain response
threshold--also not ideal.

REgardless of the implementation, a vendor snippet needs to load before the
rest of the page to be useful, so minimizing snippet response time is still
extremely important. The first step toward managing response thimes is knowing
which metrics to use to measure it, and unfortunately, this is where a lot of
businesses make mistakes. Frequently, businesses will turn to "convenience
metrics" average (or mean) response times to gauge overall performance.
However while the average might be easy to understand it's also extrmely
misleading. Why? Because looking at your average response time is like
measuring the average temperature of a hospital. What you really care about is
a patient's temperature, and in particular, the patients who need the most
help. the best way to measure this to track the 99th percentile response time:
the worst 1%.
