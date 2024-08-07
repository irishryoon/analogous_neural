# Analogous cycles 

This repository contains code accompanying the following paper: Yoon et al 2024 "Tracking the topology of neural manifolds across populations". 


* One should first download & install <a href="https://julialang.org/downloads/">Julia</a>. The code has been tested on Julia version 1.10.4.
* We recommend running the code on a compute server rather than a laptop.
* Due to the large size of data, not all data files are included in this repository. Please contact Iris Yoon (hyoon@wesleyan.edu) for copies of the data. 
* The analogous cycles code is written in Julia. However, some of the preprocessing steps are done in Python. Each notebook clarifies which language one should use. 
* We use the phrase `analogous cycles` and `analogous bars` interchangably. 

# Quick-start: implementation of analogous cycles
* Download & install <a href="https://julialang.org/downloads/">Julia</a>. 
* The "examples" directory contain example notebooks illustrating how to compute analogous cycles. 
* When running the analogous cycles code, it is <u>important that one activates the virutal environment associated with this project.</u> See the following sections for instructions on using Jupyter notebook and activating the proper virtual environment. 

## Instructions: Running Jupyter notebook from Julia REPL
* Open Julia REPL
* Using the `cd` command, navigate to the root of this directory.
* Activate \& instantiate the virtual environment as follows.
```
using Pkg
Pkg.activate( "/env/.")
Pkg.instantiate()
```
* Open a notebook using the following command.
```
Pkg.build("IJulia")
using IJulia
notebook()
```
* You can now run the Jupyter notebooks in this repository.

# Instructions on running code on your data 
When running the analogous cycles script on your own data, please make sure to include the following command. 
```
using Pkg
Pkg.activate( "/env/.")
Pkg.instantiate()

include("src/Eirene_var.jl")
include("src/analogous_bars.jl")

using .Eirene_var
using .analogous_bars
```

# Running the code on the provided datasets
* See the`analysis` directory.
* We recommend running the code in the `experimental_visual` or `simulation_navigation` directories, as the computation can take a long time for the dataset in `simulation_visual`.
* For `simulation visual`, we recommend running the code on a server. 