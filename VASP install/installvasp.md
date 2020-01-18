# Vasp installation

Requires an installed intel compiler (parallel studio) and properly sourced

In this system just run envornment by:

```
module purge
module load intel
module load impi
```

## Downoad the source files and patches (if any)

For the case of VASP 5.4.4 (as of January 2020), you will have the following files:

1. vasp.5.4.4.tar.gz
2. patch.5.4.416052018

## Prepare source files

1. Untar
```
tar zxvf vasp.5.4.4.tar.gz
```

2. Patch


3. Prepare makefile

3.1. Copy the makefile to the main directory

```
cp vasp.5.4.4/arch/makefile.include.linux_intel vasp.5.4.4/makefile.include
```

3.2. Edit Makefile

L1 cache of i7 6700 is 256KiB 
(Dcache size = l1 cache / 16) 
(DMPI_BLOCK = 2xDchache size)
change parameter to -DCACHE_SIZE = 16000
change parameter to -DMPI_BLOCK=32000

change parameter to -mkl=cluster

change parameter OFLAG = -03 -ipo -xCORE-AVX2 (FOR NEW CPU)
Note in my system, I can use xCORE AVX2 only for my nodes (6th gen intel cpu) \
but not in my head node which uses an old Intel E5. I can still compile vasp \
using the E5 but it won't run. Havent tried to make it run yet. 

clear options in BLACS SCALAPACK