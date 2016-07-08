#Evaluation of Delay Performance of Traffic Shapers
This paper presents the fixed one-way delay evaluation results of three traffic shapers, NIST Net, Netem and KauNet. It discusses how each of these shapers implement one-way delays on the packets when instructed with certain nominal values of one-way delays. It also filters out the effects of hardware platforms by doing experiments with shapers installed on Intel and AMD platforms. It concludes taht:

1. The major effect of variation from the applied delays was due to the hardware platform, while the shaper software was playing a minor role. In the Intel case, the applied one-way delays are much closer to the desired delays.
2. Netem applies delays more accurately as compared to other two shapers.
3. KauNet applies delays both below and above the set delay values therefore choice of nominal delay values must be made keeping this in mind.
