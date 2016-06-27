#Measuring Internet Video Quality of Experience from the Viewer's Perspective
##Primary Forms of Streaming Video
1. Progressive Video  
In the progressive method, sections of a single file are delivered in bursts, with no consideration for available bandwidth. For situations in which videos are available with different display quality choices(each of which are corresponds to a different bitrate), the video client(or user)mannually selects a particular resolution, which corresponds to a different file on the server.
2. Adaptive Video  
Adaptive video modulates the display quality based on the network's available transport capacity(i.e., bandwidth). It achieves this effect by fetching 'chunks' of the video in a piecewise manner; the chunk chosen is of the maximun deliverable display quality.

##Considerations for Measuring Video QoE
1. Session Lifetime and Sampling Frequency  
The necessary measurements should be taken throughout the full duration, and the frequency to take the measurements should be feasible.
2. Correlation Across Sessions  
It is of fundamental importance to be able to correlate the same asset across multiple GET transactions issued into the same, or different, TCP connections.
3. Routing Asymmetry  
For the purposes of measuring video QoE, all routing asymmetry must be resolved.

##Measuring Progressive Video QoE
In a progressive video stream, a 'seek' action can occur when a user moves a control(such as a slider) to choose a different time or the client re-buffers on a stall. Tracking these seek actions is the only way in which the transport quality of a progressive flow can be measured.
##Measuring Adaptive Video QoE
To properly measure the delivered quality of adaptive video, the measurement solution must be protocol-aware(e.g., HLS) and container-aware(to see the resolution/bitrate/codec), and also must measure stalling in the backchannel from the client.
##Why TCP Packet Loss Doesn't Matter  
The end-to-end connection adjusts to the slowest link in the chain. We can not use TCP packet loss as a means of finding the narrowest path because it will stop dropping once it determines the rate of the narrowest link, and it is also the reason why in both normal and congested situations packet loss occurs on the network.
