# Infrastructure Report

## 1. Operating System

- **Operating System:** Ubuntu 24.04.4 LTS
- **Distribution:** Ubuntu
- **Codename:** Noble

## 2. Kernel Version

- **Kernel Version:** 6.8.0-13-generic

## 3. CPU Information

- **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **Number of CPU Cores:** 1
- **Architecture:** x86_64

## 4. Memory

- **Total RAM:** 1.9 GiB
- **Available RAM:** 1.4 GiB

## 5. Disk Information

- **Main Disk Capacity:** 19G
- **Root Filesystem:** /dev/vda1
- **Root Filesystem Size:** 19G

## 6. Mounted File Systems

The Linux server contains several mounted file systems, including:

- `/`
- `/boot`
- `/boot/efi`
- `/dev/shm`
- `/run`
- `/proc`
- `/sys`
- `/dev`

## 7. Hostname

- **Hostname:** ubuntu

## 8. IP Address

- **IP Address:** 172.30.1.2

## 9. Linux Commands Executed

The following Linux commands were used to investigate the cloud server:

```bash
cat /etc/os-release
uname -r
lscpu
nproc
free -h
df -h
mount
hostname
hostname -I
