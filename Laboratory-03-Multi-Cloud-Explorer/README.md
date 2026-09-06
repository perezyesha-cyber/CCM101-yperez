# Laboratory 03 – Multi-Cloud Explorer

## Checkpoint 7 – Linux Server Investigation

The Linux server was investigated using the KillerCoda Playground and Linux commands.

### Operating System

The KillerCoda environment is running **Ubuntu 24.04** with a Linux 6.8.0-31-generic kernel.

Command used:

```bash
uname -a
```
The system uses the x86_64 architecture.

### CPU Information

Command used:
```bash
lscpu
```
The server has 1 CPU using an Intel Xeon E312xx (Sandy Bridge, IBRS update) processor with a CPU frequency of approximately 2.0 GHz.

Memory

Command used:
```bash
free -h
```
The server has approximately 1.9 GiB of total memory. It has 416 MiB used, 832 MiB free, and 1.5 GiB available memory. The system also has 1.0 GiB of swap space.

Disk Space

Command used:
```bash
df -h
```
The main filesystem /dev/vda1 has 19 GB of total space, with 5.4 GB used and 13 GB available. The disk is currently 31% used.

Cloud Migration Options

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services from the three major cloud providers.

| Cloud Provider        | Cloud Service          |
| --------------------- | ---------------------- |
| AWS                   | Amazon EC2             |
| Microsoft Azure       | Azure Virtual Machines |
| Google Cloud Platform | Compute Engine         |


These services provide virtual computing environments that can be used to run Linux-based workloads.
