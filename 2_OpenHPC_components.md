# 2. Installation of Open HPC components

#### Redine the CHROOT location
```
export CHROOT=/opt/ohpc/admin/images/centos7
```

## 2.1: Development tools
#### Install autotools meta-package (Default)
```
yum -y install  ohpc-autotools EasyBuild-ohpc hwloc-ohpc spack-ohpc valgrind-ohpc | tee autotools.o
```

## 2.2: Basic compilers (gcc ver 7 & 8 )
 ```
yum -y install gnu7-compilers-ohpc gnu8-compilers-ohpc
```

## 2.3: Basic MPI stacks
```
yum -y install openmpi3-gnu7-ohpc openmpi3-gnu8-ohpc mpich-gnu7-ohpc mpich-gnu8-ohpc
```