# KubeconEU-2024-Edge

## Repo for Kubecon EU 2024 Edge demos

This repository will contain the information for 4 demos:
- **Demo 1:** Edge Image Builder (EIB)
- **Demo 2:** k3s - 2 node HA cluster with Synadia

## Purpose
This repository is meant to be used as a tool to easily repeat the demos that will be delivered by the TMM/SA team in the Kubecon EU 2024. All the demos are based in the new features in either SUSE ATIP 3.0 or SUSE Edge 3.0, showcasing the most visual demos possible.

## Requirements

### Compute
In order to deliver this setup, you'll need 3 NUC-like PCs. Each NUC should provide at least 8 GB of RAM, 4 Cores CPU, and 8 Threads. If you want to add Rancher Prime to the equation, a fourth NUC will be necessary with at least 16 GB of RAM.
- 3x NUC

### Networking
- 4x 1Gbps port switch
- RJ45 cables

### OS
- 1x openSUSE Tumbleweed
- 2x SLE Micro 5.5

## Local DNS services
To use any "invented domain" as a local domain and make sure that all the demo machines have access to it and connect to each other properly a simple local DNS service is necessary. It will implemented will CoreDNS and podman following the next steps:
- Configure CoreDNS
- Start the CoreDNS pod with podman
- Make sure that all the machines have a static IP and that in etc/resolv.conf the first entry is the IP of the machine where the CoreDNS container is running. In this case the primary DNS resolution will be in 192.168.1.113, in there basically will find the local DNS resolution and if an external resolution were necessary will forward you to an external DNS service. 
