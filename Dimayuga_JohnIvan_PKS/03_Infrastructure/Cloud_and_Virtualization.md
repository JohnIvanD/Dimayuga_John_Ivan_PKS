# Cloud and Virtualization Fundamentals

[← Back to index](../README.md)

## Virtualization
Running multiple virtual machines (VMs) on one physical host using a **hypervisor**.
- **Type 1 (bare-metal):** runs directly on hardware (VMware ESXi, Hyper-V).
- **Type 2 (hosted):** runs on top of an OS (VirtualBox, VMware Workstation).

Security benefits: isolation, snapshots, safe testing environments (e.g., running DVWA in a VM).

## Cloud service models
| Model | You manage | Example |
|---|---|---|
| IaaS | OS, apps, data | AWS EC2 |
| PaaS | Apps, data | Google App Engine |
| SaaS | Data and settings | Gmail |

## Deployment models
Public, private, hybrid, community.

## Shared responsibility
The provider secures the cloud itself (hardware, facilities); the customer secures what they put in it (data, access, configuration).

## My Reflection
I learned that virtualization allows multiple operating systems to run on one physical computer using virtual machines. During our Parrot OS setup, I experienced how important it is to configure memory, processors, and virtual disk storage correctly. I also encountered installation problems and had to troubleshoot the virtual machine before continuing. This activity helped me become more familiar with VirtualBox and understand how virtualization can provide a separate environment for cybersecurity practice.

## Review Questions
1. Difference between Type 1 and Type 2 hypervisors?
2. Who is responsible for data security in SaaS?
3. Why are snapshots useful in a lab?
