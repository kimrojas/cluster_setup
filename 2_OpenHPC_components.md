# 2. Installation of Open HPC components

#### Redine the CHROOT location
```
export CHROOT=/opt/ohpc/admin/images/centos7
```

## 2.1: Essential packages

### A. Essential development tools

```
yum -y install EasyBuild-ohpc automake-ohpc autoconf-ohpc cmake-ohpc hwloc-ohpc libtool-ohpc spack-ohpc valgrind-ohpc
```

### B. Development packages (GNU based)

#### Compiler Families (GNU)

```
yum -y install gnu7-compilers-ohpc gnu8-compilers-ohpc 
```

#### MPI Families (GNU)

```
yum -y install openmpi3-gnu7-ohpc openmpi3-gnu8-ohpc
```

### # Default compiler for Head node (GNU)

```
yum -y install lmod-defaults-gnu8-openmpi3-ohpc
```

#### Python tools (GNU)

```
yum -y install \
python34-scipy-gnu7-openmpi3-ohpc python34-scipy-gnu8-openmpi3-ohpc \
python34-numpy-gnu7-ohpc python34-numpy-gnu8-ohpc \
python34-mpi4py-gnu7-openmpi3-ohpc python34-mpi4py-gnu8-openmpi3ohpc
```

### C. Development packages (Intel based)

**~Requires Intel parallel studio installation before hand~**

#### Compiler Families (Intel)

```
yum -y install intel-compilers-devel-ohpc
```

#### MPI Families (Intel)

```
yum -y install intel-mpi-devel-ohpc
```

#### Python tools (Intel)

```
yum -y install \
python34-numpy-intel-ohpc \
python34-mpi4py-intel-impi-ohpc \

python34-scipy-gnu7-openmpi3-ohpc python34-scipy-gnu8-openmpi3-ohpc \
python34-numpy-gnu7-ohpc python34-numpy-gnu8-ohpc \
python34-mpi4py-gnu7-openmpi3-ohpc python34-mpi4py-gnu8-openmpi3ohpc
```

### D. Other packages

#### For slurm
```
yum -y install slurm-sview-ohpc slurm-pam slurm-ohpc
```

#### For Performance analysis tools
```
yum -y install \
dimemas-gnu8-openmpi3-ohpc dimemas-intel-impi-ohpc \
extrae-gnu8-openmpi3-ohpc extrae-intel-impi-ohp \
geopm-gnu8-openmpi3-ohpc geopm-intel-impi-ohpc \
imb-gnu7-openmpi3-ohpc imb-gnu8-openmpi3-ohpc imb-intel-impi-ohpc \
likwid-gnu7-ohpc likwid-gnu8-ohpc likwid-intel-ohpc \
mpiP-gnu7-openmpi3-ohpc mpiP-gnu8-openmpi3-ohpc mpiP-intel-impi-ohpc \ 
pdtoolkit-gnu7-ohpc pdtoolkit-gnu8-ohpc pdtoolkit-intel-ohpc \
scalasca-gnu7-openmpi3-ohpc scalasca-gnu8-openmpi3-ohpc scalasca-intel-impi-ohpc \
tau-gnu7-openmpi3-ohpc tau-gnu8-openmpi3-ohpc tau-intel-openmpi3-ohpc
```

#### For IO libraries
```
yum -y isntall \
adios-gnu7-openmpi3-ohpc adios-gnu8-openmpi3-ohpc adios-intel-impi-ohpc \
hdf5-gnu7-ohpc hdf5-gnu8-ohpc hdf5-intel-ohpc \
netcdf-cxx-gnu7-openmpi3-ohpc netcdf-cxx-gnu8-openmpi3-ohpc netcdf-cxx-intel-impi-ohpc \
netcdf-fortran-gnu7-openmpi3-ohpc netcdf-fortran-gnu8-openmpi3-ohpc netcdf-fortran-intel-impi-ohpc \
netcdf-gnu7-openmpi3-ohpc netcdf-gnu8-openmpi3-ohpc netcdf-intel-impi-ohpc \
phdf5-gnu7-openmpi3-ohpc phdf5-gnu8-openmpi3-ohpc phdf5-intel-impi-ohpc \
pnetcdf-gnu7-openmpi3-ohpc pnetcdf-gnu8-openmpi3-ohpc pnetcdf-intel-impi-ohpc \
sionlib-gnu7-openmpi3-ohpc sionlib-gnu8-openmpi3-ohpc sionlib-intel-impi-ohpc \
```

#### For runtimes
```
yum -y install \
charliecloud-ohpc ocr-gnu7-ohpc ocr-gnu8-ohpc ocr-intel-ohpc singularity-ohpc
```

#### For Serial/Threaded Libraries
```
yum -y install \ 
R-gnu7-ohpc R-gnu8-ohpc gsl-gnu7-ohpc gsl-gnu8-ohpc \
metis-gnu7-ohpc metis-gnu8-ohpc metis-intel-ohpc \
openblas-gnu7-ohpc openblas-gnu8-ohpc \
plasma-gnu7-ohpc plasma-gnu8-ohpc plasma-intel-ohpc \
scotch-gnu7-ohpc scotch-gnu8-ohpc scotch-intel-ohpc \
superlu-gnu7-ohpc superlu-gnu8-ohpc superlu-intel-ohpc 
```

#### For Parallel libraries 
```
yum -y install \
boost-gnu7-openmpi3-ohpc boost-gnu8-openmpi3-ohpc boost-intel-impi-ohpc \
fftw-gnu7-openmpi3-ohpc fftw-gnu8-openmpi3-ohpc \
hypre-gnu7-openmpi3-ohpc hypre-gnu8-openmpi3-ohpc hypre-intel-impi-ohpc \
mfem-gnu7-openmpi3-ohpc mfem-gnu8-openmpi3-ohpc mfem-intel-impi-ohpc \
mumps-gnu7-openmpi3-ohpc mumps-gnu8-openmpi3-ohpc mumps-intel-impi-ohpc \
opencoarrays-gnu8-openmpi3-ohpc \
petsc-gnu7-openmpi3-ohpc petsc-gnu8-openmpi3-ohpc petsc-intel-impi-ohpc\
ptscotch-gnu7-openmpi3-ohpc ptscotch-gnu8-openmpi3-ohpc ptscotch-intel-impi-ohpc \
scalapack-gnu8-openmpi3-ohpc scalapack-intel-impi-ohpc \
slepc-gnu7-openmpi3-ohpc slepc-gnu8-openmpi3-ohpc slepc-intel-impi-ohpc \
superlu_dist-gnu7-openmpi3-ohpc superlu_dist-gnu8-openmpi3-ohpc superlu_dist-intel-impi-ohpc \
trilinos-gnu7-openmpi3-ohpc trilinos-gnu8-openmpi3-ohpc trilinos-intel-impi-ohpc
```