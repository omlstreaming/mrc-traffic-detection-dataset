# Datasets

Public (anonymized) datasets from Huawei Munich Research Center, used in the
Querying Top-k Dominant Traffic Flows on Large Urban Road Networks [1] paper.

All data that are described are having the form of:
```
anonymized_car_plate,startDate,startTime,endDate,endTime,leaving_edge,intersection,incoming_edge
```
All data files are sorted based on the `anonymized_car_plate` and on the `startTime`.

------------------------------------

## RM and RD

RM is a real-life dataset collected in the period of March 2020 from traffic
detectors in an area of a Chinese city. The detectors were located
in 6 intersections monitoring the traffic on 44 road edges. Each
detector was collecting data every 1 second for all the road edges
in its radius. In total, 2894174 detections were collected, from
337089 different vehicles.

RD includes the data from RM for one of the days in that month.
The data from that day include 116268 detections from 44643 vehicles

------------------------------------

## COM

This is a synthetic dataset that generated in
the same road network as the real-life data RM and RD, with the
difference that we included detectors in the 2 intersections where
the real scenario didn’t have. Then, we generated equally random
trips over the road network. In total we generated 18910 detections
from 7500 vehicles

------------------------------------

## GRID

This dataset was created using the SUMO Simulation of Urban Mobility [2].
We randomly generated trips on a 10𝑥10 intersections grid road
network using a utility from SUMO that equally generates trips
over the road network. Then, running the simulation and using
TraCI Traffic Control Interface library [3] we read the simulation
data and collect the detections. The simulation collected data
include 1806141 detections from 135618 different vehicles.

------------------------------------

## REFERENCES

[1] Stella Maropaki, Paolo Sottovia, and Stefano Bortoli. 2021. Querying
Top-k Dominant Traffic Flows on Large Urban Road Networks. In 2021 24th
International Conference on Extending Database Technology (EDBT).

[2] Pablo Alvarez Lopez, Michael Behrisch, Laura Bieker-Walz, Jakob Erdmann,
Yun-Pang Flötteröd, Robert Hilbrich, Leonhard Lücken, Johannes Rummel,
Peter Wagner, and Evamarie WieBner. 2018. Microscopic traffic simulation
using sumo. In 2018 21st International Conference on Intelligent Transportation
Systems (ITSC). IEEE, 2575–2582.

[3] https://sumo.dlr.de/docs/TraCI.html
