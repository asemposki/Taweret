# Taweret

<img align="right" width="200" src="./logos/taweret_logo.PNG">

Welcome to the GitHub repo for Taweret, the state of the art Python package for applying Bayesian Model Mixing! 

## About
Taweret is a new generalized package to help with applying Bayesian model mixing methods, developed by members of the [BAND](https://bandframework.github.io/) collaboration, to a wide variety of problems in physics. 

## Features
At present, this package possesses the following BMM methods:
- Linear model mixing ( With simultaneous model mixing and calibration)
- Multivariate BMM 
- Bayesian Trees

## Documentation
See Taweret's docs webpage [here](https://bandframework.github.io/Taweret/).

### Cloning
This repository uses submodules. 
To clone this repository and automatically checkout all the submodules, use
```terminal
git clone --recursive https://github.com/TaweretOrg/Taweret.git 
```

If you want to limit the size of the repository (this or the submodules), you can use the `depth` flag
```terminal
git clone --depth=1 https://github.com/TaweretOrg/Taweret.git
```
Inside the directory containing the cloned repository, you then run
```terminal
git submodule update --init --depth=1
```

## Testing
The test suite requires the [pytest](https://pypi.org/project/pytest/) package to be installed and can be run from the `test/` directory. To test the current BMM methods, first install the required packages and then run the following three lines of code:

To installing requirements, first navigate to the Taweret directory. The requirements.txt file is located in the root of this directory. Once in the Taweret directory, then execute the following line of code from the terminal.

```
pip install -r requirements.txt
```

Then, install the OpenBT mixing package. To do this, please see the instructions under the Dependencies Section below.

Once all installation is complete, proceed with testing by naviagating to the `test/` directory and executing the following three lines of code.

```
pytest test_bivariate_linear.py
pytest test_gaussian.py
pytest test_trees.py
```

## Dependencies
Python dependencies are listed in the requirements.txt file. Taweret also depends on the OpenBT Mixing package in order to execute the trees modulde. To install OpenBT please follow the steps listed below:

**Linux:**

1. Download the OpenBT Ubuntu Linux 20.04 package:

```    
    $ wget -q https://github.com/jcyannotty/OpenBT/raw/Taweret-v0.3/openbt_mixing0.current_amd64-MPI_Ubuntu_20.04.deb  
```


2. Install the package and reset the library cache:

```    
    $ cd /location/of/downloaded/.deb
    $ dpkg -i openbt_mixing0.current_amd64-MPI_Ubuntu_20.04.deb
    $ ldconfig
```


**Mac OS/X:**

1. Install the OS/X OpenMPI package by running the following `brew` commands in a terminal window:

```    
    $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
    $ brew install open-mpi
```


2. Download the OpenBT OSX binary package, "OpenBT-Mixing-0.current.pkg", from https://github.com/jcyannotty/OpenBT/tree/Taweret-v0.3 .

3. Install the OpenBT OSX package by double-clicking on the downloaded .pkg file and follow the on-screen instructions.


**Windows:**

OpenBT will run within the Windows 10 Windows Subsystem for Linux (WSL) environment. For instructions on installing WSL,
please see (https://ubuntu.com/wsl). We recommend installing the Ubuntu 20.04 WSL build. There are also instructions
[here](https://wiki.ubuntu.com/WSL?action=subscribe&_ga=2.237944261.411635877.1601405226-783048612.1601405226#Installing_Packages_on_Ubuntu) 
on keeping your Ubuntu WSL up to date, or installing additional features like X support. Once you have installed the WSL Ubuntu layer, start the WSL Ubuntu shell from the start menu and then install the package:

```    
    $ cd /mnt/c/location/of/downloaded/.deb
    $ dpkg -i openbt_mixing0.current_amd64-MPI_Ubuntu_20.04.deb
```


**Alternative:**

Rather than installing the pre-built packages, one can also download the code from https://github.com/jcyannotty/OpenBT/tree/Taweret-v0.3 
and compile the C++ code locally. Then the trees module can be used by specifiying the location of the local openbt repository when  
initializing the trees class instance. 



## Citing BAND software
If you have benefited from Taweret, please cite the BAND collaboration software suite using the format [here](https://github.com/bandframework/bandframework#citing-the-band-framework).

## BAND SDK compliance
Check out our SDK form [here](https://github.com/TaweretOrg/Taweret/blob/main/Taweretbandsdk.md).

## Contact
To contact the Taweret team, please submit an issue through the Issues page. 

Authors: Kevin Ingles, Dan Liyanage, Alexandra Semposki, and John Yannotty.


