# 2D-simulations-TSK
Repository containing data and code for 2D simulations of Triangular, Stripes and Kagome phases. 

## Content 
| Directory | Description | 
|:----------|:----------|
| triangular | Contains the LAMMPS simulations scripts, the force-field and the starting configuration for the triangular phase |
| stripes | Contains the LAMMPS simulations scripts, the force-field and the starting configuration for the stripes phase |
| kagome | Contains the LAMMPS simulations scripts, the force-field and the starting configuration for the kagome phase |

## How to run the code 

In order to run the code, for instance, starting from the config_start.data, and raising the temperature to T = 0.01 (LJ units),

```bash
lmp_mpi -in run_md2.lmp -v Tnew 0.01 -v filein config_start.data
```
Now, to raise the temperature from 0.01 up to 0.02 and using the last configuration from the previous run, 
```bash
lmp_mpi -in run_md3.lmp -v Tnew 0.02 -v Told 0.01 -v filein config_T_0.01.data
```
