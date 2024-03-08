# KubeconEU-2024-Edge
## Repo for Kubecon EU 2024 Edge demos
This repository will contain the information for 4 demos:
- Demo 1: Edge Image Builder (EIB)
- Demo 2: k3s - 2 node HA cluster 
- Demo 3: k3s & Akri video
- Demo 4: k3s & Linkerd for IoT

## Requirements

### Compute
In order to deliver this setup you'll need 3 NUC-like PCs. Each NUC should provide at least 8 GB of RAM, 4 Cores CPU, 8 Threads. If you want to add Rancher Prime to the equation a fourth NUC will be necessary with at least 16 GB of RAM. Also a Raspberry Pi 4 or superior with 4GB of RAM.
- 4xNUC
- 1xRaspberry Pi

### Devices & power
- IP camera Reolink + POE adapter if the switch does not support POE
- Power base, at least 6 power connections 

### Networking
8x1Gbps port switch
6x RJ45 cables

### OS
- 1x openSUSE Tumbleweed
- 3x SLE Micro 5.5
- 1x openSUSE Leap

# Demo 1: Edge Image Builder

## Intro
On this demo we will show how EIB works, explaining the concepts, the structure and how to use it. Long story short, EIB allows you to prepare a full stack deployment in an ISO image allowing to deploy a fully functional k3s or RKE2 cluster with the ISO and with no further configuration or internet connectivity, simplifying extremely the deployment of kubernetes at the edge or Zero Touch Provisioning workflows like the one used for ATIP or Edge 3.0 using CAPI and Metal3 to deploy on bare metal machines.
