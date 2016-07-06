#Evaludation of Throughput Performance of Traffic Shapers
This paper investigates the accuracy of NetEm and KauNet shapers for their respective throughput shaping. It discusses the behavior of each shaper with respect to different shaping values and PDU sizes. Moreover, it also studies the effect of hardware platform by evaluating the shapers, installed on Intel and AMD platforms. Here is what it finds:

1. In case of KauNet hardware has no effect, while NetEm reveals a nominal difference of shaped throughput on basis of the hardware platform.
2. KauNet shapes throughput accurately for big PDUs. 
3. NetEm shapes throughput accurately for big PDUs especially on the AMD platform.
4. It also calculates the buffer content of both shapers and shows that NetEm's buffer is twice as large as that of KauNet.
5. In most cases, both shapers allows for consistent throughput shaping on the investigated time scales between 1 ms and 1 s, with a slight advantage for NetEm.
