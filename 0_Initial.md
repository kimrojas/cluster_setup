# Initialization

### OS installation

Create a bootable drive (CentOS) using:

1. CentOS 7 https://www.centos.org/download/
2. Rufus https://rufus.ie/

Notes: \
[a] as of time of writing CentOS 7.7 was the latest version \
[b] disk allocation can be automatic but I prefer */opt* to have better

### Summarize Cluster information

| Machine | Category| Description |
|---|---|---|
|Master|Hostname: | master |
||Private Network: | eth0 10.20.100.200 (MAC:192.168.1.254) |
||Public Network: | eth0 10.20.100.200 (MAC:192.168.1.254) 
|Compute01|Hostname: | c1 |
||Private Network: | eth0 10.20.100.200 (MAC:192.168.1.254) |
||Public Network: | eth0 10.20.100.200 (MAC:192.168.1.254) 
|Compute02|Hostname: | c2 |
||Private Network: | eth0 10.20.100.200 (MAC:192.168.1.254) |
||Public Network: | eth0 10.20.100.200 (MAC:192.168.1.254) 

### Edit host file

```
echo "192.168.1.254 master" >> /etc/hosts
hostnamectl set-hostnname master
```

### Disable firewall

```
systemctl disable firewalld
systemctl stop firewalld
```

### Disable selinux

```
vi /etc/selinux/config
```

edit file to `SELINUX=disabled`

### Reboot master node

`reboot`

### Update CentOS

`yum -y update`

### Enable reading of Exfat USB

```
yum -y install epel-release
rpm -v --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro
rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm
yum -y install exfat-utils fuse-exfat
```

### Install htop
`yum -y install htop`


