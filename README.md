<p align="center">
  <strong>MDGVRP-PD</strong><br />
  Benchmark instances for multi-depot green vehicle routing with pickups and deliveries.
</p>

<p align="center">
  <img alt="Text instances" src="https://img.shields.io/badge/format-text-2f6f4e" />
  <img alt="Instances 14" src="https://img.shields.io/badge/instances-14-444444" />
  <img alt="ICCL 2021" src="https://img.shields.io/badge/reference-ICCL%202021-0a6ed1" />
</p>

<p align="center">
  <code>MDGVRP</code> | <code>Pickup and Delivery</code> | <code>Green Routing</code> | <code>Benchmarks</code>
</p>

---

`MDGVRP-PD` stores benchmark instances for the Multi-Depot Green Vehicle Routing Problem with Pickups and Deliveries. The files include city metadata, depots, customer requests, time windows, service durations, demands, and vehicle classes.

The instances were prepared for "Optimization of Green Pickup and Delivery Operations in Multi-Depot Distribution Problems", presented at ICCL 2021. The repository does not include a solver or experiment runner.

## Product Surface

| Area | Contract |
| --- | --- |
| Runtime | None; static benchmark files |
| Data format | Plain-text routing instances |
| Data path | External solver reads instance files directly |
| Storage | Git-tracked `.txt` files |
| Documentation | This README |
| Distribution | GitHub repository |

## Runtime Shape

```mermaid
flowchart LR
  researcher["Researcher"] --> repo["MDGVRP-PD"]:::primary
  repo --> instances["14 city instances"]
  instances --> solver["Routing model or algorithm"]

  classDef primary fill:#2f6f4e,stroke:#173927,color:#ffffff,stroke-width:2px
```

## Responsibilities

- Preserve the MDGVRP-PD benchmark instance files.
- Store city, depot, vehicle, request, demand, service-time, and time-window data.
- Document the expected file sections for parser development.
- Keep solver logic and result reporting outside this repository.

## How It Is Built

| File Pattern | Role |
| --- | --- |
| `pd_bar-*.txt` | Barcelona instances. |
| `pd_ber-*.txt` | Berlin instances. |
| `pd_nyc-*.txt` | New York City instances. |
| `pd_poa-*.txt` | Porto Alegre instances. |
| `README.md` | Data contract and citation notes. |

## Platform and Service Dependencies

<table>
  <tr>
    <th>Service / Object</th>
    <th>Provider</th>
    <th>Usage</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td><code>pd_*.txt</code></td>
    <td>Repository files</td>
    <td>Consumed by external MDGVRP-PD solvers.</td>
    <td>Provides reproducible benchmark data for pickup-and-delivery routing experiments.</td>
  </tr>
</table>

## File Structure

Each instance includes:

- General metadata: name, location, size, depots, route duration limit, and time-window length.
- Vehicle classes with curb weight and maximum payload.
- Customer/request nodes with coordinates, demand, service duration, time windows, and pickup-delivery pairing.
- Depot nodes with coordinates and operating windows.

The route duration limit is 240 minutes. Demands and vehicle capacities are expressed in kilograms.

## Reference

The publication associated with these instances is available through Springer:

<https://link.springer.com/chapter/10.1007/978-3-030-87672-2_32>

## Verification

No automated tests are defined. Recommended manual verification is to parse one instance per city and confirm the expected `VEHICLES`, `NODES`, and `DEPOTS` sections.

## Secret Handling

The repository contains benchmark data only and should not store credentials or private operational data.
