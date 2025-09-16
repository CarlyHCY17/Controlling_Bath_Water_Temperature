This is an exercise in using the proportional controller. In this scenario, we need a temperature controlled bath for a chemistry experiment. The temperature of the bath is assumed to be constantthroughout by use of a magnetic stirrer. There is a constant flow of water into the bath through a long pipe, so there is a convective time delay of 12 seconds. The baseline temperature for the bath is 35C. The maximum and minimum possible temperatures for the bath is 50c and 10c respectively. The goal of this exercise is to determine the K value forthe proportional controller in order to minimise settling time. 
The strategy for determining K is as follow: 
1. graph the root locus of the plant.
2. Let K=1 so that the system's default rise time, settling time can be determined.
3. The K is then adjusted accordingly.
Results:
From the root locus graph, the system has only one real negative pole. The system is first order in nature. Since a larger negative real value means faster settling time, the control strategy is to increase K by a factor of 10 for multiple iterations. In total, 5 iterations were done, including K=1. The control strategy is proven effective:
K=1     Settling Time:97.8019
K=10    Settling Time:17.7822
K=100   Settling Time:1.9367
K=1000  Settling Time:0.1954
K=10000 Settling Time:0.0196
It is reasonable to conclude as K increases exponentially, the settling time should decrease exponentially. However, this is just a scenario I picked out from my homework. Some real life drawbacks of increasing K exponentially includes noise amplification and also that it might saturate the system, which is not great.
