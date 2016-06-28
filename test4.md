#Measuring Internet Video Quality of Experience from the Viewer's Perspective
##QoE Metric
1. Should measure the QoE from the perspective of the viewer, because the viewer's experience is most important.
2. Must measure both *display quality* and *transport quality*, and must integrate both into the QoE metric.
3. Must not use any TCP jitter or packet loss, because these metrics are irrelevant to video QoE, and entirely uncorrelated.
4. The QoE metric must be calculated differently for progressive streams and adaptive streams, because progressive streaming and adaptive streaming are fundamentally and profoundly different in behavior.

##Sessions
1. Measurements must be made throughout the full duration of a video session, because video sessions are generally long-lived, with viriable quality.
2. The frequency of measurements must be sufficient to avoid sampling error. Sampling must be optimized to give accurate results without onerous performance overhead; practically, sampling at 15 second or 30 second intervals is appropriate.
3. The video QoE solution must be able to correlate delivery of the same asset across multiple HTTP GET transactions issued into the same, or different, TCP connections. What looks like a single video to the end user is actually split within and across TCP connections that must all be considered as a whole.
4. The video QoE solution must be deployed in such a manner that it sees each video flow in a perfectly symmetrical manner; that is, routing asymmetry must be completely resolved from perspective of the measuring device.

##Progressive Video QoE
1. The Video QoE solution must be able to keep track of seek actions(whether initiated by the user or the video client) dynamically for all HTTP transactions. It is required to both measure the duration of a progressive video flow and to count buffer events.
2. The video QoE solution must be able to extract display quality information from the video container. THe container holds the display quality information, which is a required dimension of video streaming QoE.

##Adaptive Video QoE
1. The video QoE solution must be protocol-aware. It is required to measure the transport quality.
2. The video QoE solution must be able to extract display quality information from the video container. The container holds the display quality information, which is a required demension of video streaming QoE.
3. Video QoE metric must not be based in any part on transferred bytes. Since the display quality(and bitrate) varies dynamically, the number of bytes transferred is irrelevant.

