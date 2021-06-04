# Instances for the Multi-Depot Pickup and Delivery Cumulative Vehicle Routing Problem (MD-PDCumVRP)

In this repository you can find information about the MD-PDCumVRP instances proposed in the submitted article entitled *Multi-depot one-to-one pickup and delivery cumulative vehicle routing problem*, International Conference on Computational Logistics (ICCL2021), September 27-29, 2021, University of Twente, Enschede, The Netherlands. The article is available via e-mail [here](mailto:affernan@jp.inf.utfsm.cl).

The generated data instances consist on a modified subset of the n100 and n200 groups of instances proposed in [Sartori and Buriol (2020)](https://www.sciencedirect.com/science/article/pii/S0305054820301829), where the authors considering real urban locations set of routes can be performed in a single labor day (eight hours). For that, the following two instances was plotted thorugh [Google Maps](https://www.google.com/maps/d/edit?mid=1Y-Qd16qhqWWvHsVQsBDVs4q4_Car6wVq&usp=sharing).


The modified test have n+m locations. There are n customer locations and m depots. The n locations are paired to form a total of n requests (pickup and delivery couples). This instances consists of three different groups, ranging from 10 to 200 customers and are classified in three different complexity levels: small-scale with the first 10 or 50 customers from original {n100} group from [Sartori and Buriol (2020)](https://www.sciencedirect.com/science/article/pii/S0305054820301829); medium-scale with the first 70 or 100 customers from {n100;n200}, and the last group for the large-scale with the first 150 or 200 customers. For all instances considered in this section, the time limit tour duration is 240 minutes and we add four depot locations from the remaining locations that were not used in the generated instances.  The customers’ demands and the capacity of the vehicles are considered in kilogram. Also, the vehicle parameters used is based on Light Duty type with curb-weight of 3500 kg and maximum payload of 4000 kg, what it is known as gross vehicle weight rating of a vehicle.

## Instance files

Information on how to obtain the 14 files containing the definiton of the instances in the set are available under the folder [instances/](https://github.com/affernan/MDPD_CUMVRP).
