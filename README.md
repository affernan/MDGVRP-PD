# MDGVRP-PD Instances

This repository contains benchmark instances for the Multi-Depot Green Vehicle Routing Problem with Pickups and Deliveries (MDGVRP-PD).

The instances were prepared for the work "Optimization of Green Pickup and Delivery Operations in Multi-Depot Distribution Problems", presented at the International Conference on Computational Logistics (ICCL 2021). The publication is available through Springer: <https://link.springer.com/chapter/10.1007/978-3-030-87672-2_32>.

## Contents

The repository includes 14 plain-text instances:

- Barcelona: `pd_bar-*`
- Berlin: `pd_ber-*`
- New York City: `pd_nyc-*`
- Porto Alegre: `pd_poa-*`

The instances cover problem sizes from 10 to 200 customers and include four depots.

## Instance Structure

Each file includes:

- General metadata: name, location, size, number of depots, route duration limit, and time-window length.
- Vehicle classes with curb weight and maximum payload.
- Customer and request nodes with coordinates, demand, service duration, time windows, and pickup-delivery pairing.
- Depot nodes with coordinates and operating windows.

The route duration limit is 240 minutes. Demands and vehicle capacities are expressed in kilograms.

## Source Data

The instances are based on modified subsets of the open-data pickup and delivery instances proposed by Sartori and Buriol (2020), using real urban locations.

## Suggested Citation

If these instances are used in academic work, please cite the ICCL 2021 paper associated with this repository and the original open-data instance source when appropriate.
