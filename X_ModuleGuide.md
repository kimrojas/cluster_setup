# Guide for running module

### Default loadout

gnu + mpich

### enable Intel-impi loadout

```
module purge
module load intel impi
```

### list of loaded modules

`module list`

### available module for loading

`module avail`

Note: Some modules only apear when the right compiler and mpi are loaded \
for example: intel impi are required by VASP and QE modules

### FOR ADMIN - Module file location 

`/opt/ohpc/modulefiles`

### FOR ADMIN - Addition of new software 

Add new software in :
`/opt/ohpc/modulelibs`