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


