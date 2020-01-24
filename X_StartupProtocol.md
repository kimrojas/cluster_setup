# Run these commands on shutdown event / power outtage
# This restarts the services

```
systemctl restart gmond 
systemctl restart gmetad 
systemctl restart dhcpd 
wwsh pxe update
```

```
wwsh file resync
```

`pdsh -w c[1-6] uptime`

```
systemctl restart munge
systemctl restart slurmctld
pdsh -w c[1-6] systemctl restart slurmd
```

```
munge -n | unmunge
munge -n | ssh c1 unmunge
munge -n | ssh c2 unmunge
munge -n | ssh c3 unmunge
munge -n | ssh c4 unmunge
munge -n | ssh c5 unmunge
munge -n | ssh c6 unmunge
```

```
systemctl status slurmctld
ssh c1 systemctl status slurmd
ssh c2 systemctl status slurmd
ssh c3 systemctl status slurmd
ssh c4 systemctl status slurmd
ssh c5 systemctl status slurmd
ssh c6 systemctl status slurmd
```

```
scontrol show nodes
```