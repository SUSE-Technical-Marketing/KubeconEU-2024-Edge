# Demo 1: Edge Image Builder

## Intro
In this demo, we will show how EIB works, explaining the concepts, the structure, and how to use it. Long story short, EIB allows you to prepare a full stack deployment in an ISO image, enabling the deployment of a fully functional k3s or RKE2 cluster with the ISO without further configuration or internet connectivity. This simplifies the deployment of Kubernetes at the edge or Zero Touch Provisioning workflows like the one used in SUSE ATIP/Edge 3.0 leveraging CAPI and Metal3 to deploy on bare metal machines.

## The demo
Two config files are provided on this demo, these config files combined with EIB will deploy a single node of RKE2 or k3s running on top of SLE micro 5.5.

The first step is clonning the edge image builder on your computer, or if you are you the same settings than this demo you will be using a computer to run EIB and CoreDNS, also to be your desktop environment for the demos you the recommendation would be using openSUSE Tumbleweed. The repo for EIB is https://github.com/suse-edge/edge-image-builder.git, in there you can find the basic steps and all the info necessary to working with EIB, anyway we will describe step by step all. You need to install some packages in openSUSE before clonning the repo or using EIB. 

```
# Pre EIB packages

sudo zypper install -y git

sudo zypper install -y podman

sudo zypper install -y gpgme-devel device-mapper-devel libbtrfs-devel

# Clonning the repo

git clone https://github.com/suse-edge/edge-image-builder.git

```

Now the repo is ready to start working, go inside the folder and create a folder named eib. After move inside the eib folder, and let's create the necessary structure for EIB to work. Create a builder folder where the builds and combustion will be created, a base-images folder, a kubernetes folder, and a custom folder. Each one will host different content and have a different purpose. After the folders are created, and assuming a config file present we will end having an structure like this:

```
❯ tree
.
├── _build
├── base-images
├── custom
├── eib-slm-k3s.yaml
├── eib-slm-rke2.yaml
└── kubernetes
    └── config
        └── server.yaml

5 directories, 3 files

```

In the eib folder inside this repo you'll find a copy of the structure and two config files to configure SLE Micro 5.5 + RKE2 or k3s in an iso.
In the EIB repo you can find more options and different folders, for instance you can create a rpm folder where you can store rpm files that will be automatically installed once the OS is installed. But for now this is enough for our demo.
In the ```_build```folder you'll find the EIB logs, the combustion files, and other scripts necessary to create your ISO images. All will be created by the EIB itself when you run it. In the ```base-images``` you have to store the OS ISOs or RAW files that you want to use with EIB. In this case we want to showcase SLE Micro and that's the images we've used. Inside ```kubernetes/config```. In the ```custom/scripts``` you can place combustion scripts that will be executed alongside the rest of the combustion scripts, helping the automation process.
