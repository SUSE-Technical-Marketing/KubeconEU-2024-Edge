# KubeconEU-2024-Edge

## Repo for Kubecon EU 2024 Edge demos

This repository will contain the information for 4 demos:
- **Demo 1:** Edge Image Builder (EIB)
- **Demo 2:** k3s - 2 node HA cluster with Synadia
- **Demo 3:** k3s & Akri for IoT, IP camera video streaming
- **Demo 4:** k3s & Linkerd for IoT

## Purpose
This repository is meant to be used as a tool to easily repeat the demos that will be delivered by the TMM/SA team in the Kubecon EU 2024. All the demos are based in the new features in either SUSE ATIP 3.0 or SUSE Edge 3.0, showcasing the most visual demos possible.

## Requirements

### Compute
In order to deliver this setup, you'll need 3 NUC-like PCs. Each NUC should provide at least 8 GB of RAM, 4 Cores CPU, and 8 Threads. If you want to add Rancher Prime to the equation, a fourth NUC will be necessary with at least 16 GB of RAM. Also, a Raspberry Pi 4 or superior with 4GB of RAM.
- 4x NUC
- 1x Raspberry Pi

### Devices & Power
- IP camera Reolink + POE adapter if the switch does not support POE
- Power base, with at least 6 power connections 

### Networking
- 8x 1Gbps port switch
- 6x RJ45 cables

### OS
- 1x openSUSE Tumbleweed
- 3x SLE Micro 5.5
- 1x SLES

