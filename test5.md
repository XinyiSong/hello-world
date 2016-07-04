#QoE Matters More Than QoS: Why People Stop Watching Cat Videos
This paper evaluates various QoE metrics by analyzing video abandonment rates in YouTuBe. An abandonment accurs if a viewer closes the video during playback, either due to lack of interest or because they are annoyed by playback events such as long start-up latency, frequent rebufferings and bitrate changes. The key findings and contributions can be divided into three categories:

1. Development of an analysis tool for video QoE.  
YouSlow is designed to detect various playback events while a video is being played. It allows viewers to track their viewing experiences such as statistics of average played bitrates and rebufferings in real time.
2. Development and evaluation of QoE metrics.  
Tracking rebuffering ratio and bitrate changes during playback is useful to quantify abandonment rates for short vedios.
3. An analysis of YouTuBe.  
This paper shows that rebufferings increase abandonment six times as much as the start-up latency caused (mostly) by pre-roll ads. Most interestingly, it shows that even increasing a bitrate during playback can annoy viewers; when the bitrate changes, they abandon videos more than four times as much. Further, it shows that a single rebuffering event can cause abandonment rate three times higher than a single bitrate change.
