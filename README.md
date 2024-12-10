# Containerize a conda environment
Instructions on how to containarize a conda environment using Singularity/Apptainer

## Define environment in yaml file
Use a `.yml` file to define your conda environment. This file needs to be in the same folder as `miniconda.def` during the build.

## Build container image
With singularity/apptainer build the environment from the definition file:
```
singularity build ${environment}.sif miniconda.def
``` 

## List packages installed in the environment  

```
singularity exec ${environment}.sif conda list
```
