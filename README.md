# Kraken cluster setup

![alt text](https://github.com/kimrojas/cluster_setup/blob/master/kraken.JPG)

### Description:

This setup repository should be helpful in creating a simple cluster setup based on *OpenHPC* managed by *SLURM*. This project is mainly done for making a usable cluster for Scientific calculations (QUANTUM ESPRESSO, GROMACS, VASP, Python-based codes)

Disclaimer: This repository is actually meant to guide me when I forget how to do this.   

References:









This cluster guide is thanks to the following as basis: 

 Install guide with Warewulf + Slurm (https://openhpc.community/downloads/)

### 1. Requirements /  assumption
#### - BASH command-line
#### - PXE booting enabled nodes
#### - One (1) HEAD NODE and four (4) COMPUTE NODES.
- Head node - will be provisioned with CentOS 7.6 
- with NFS file system available for compute nodes
- 2 ethernet port (eth0: data network(to internet), eth1: backend (to compute node switch)




1. Rocks 7 \
2. Node installation \ 
3. MPI (HPC ROLL) \


