# DigiTEF
Digital TEst Facility - customized build of OpenFOAM, based on OpenFOAM+ and other tools from community and UniCFD
DigiTEF is distributed under GPL v.3 license and includes next parts:
* OpenDTEF library https://github.com/unicfdlab/OpenDTEF with
    * Customized version of OpenFOAM+ platform https://openfoam.com/
    * PyFoam https://github.com/Unofficial-Extend-Project-Mirror/openfoam-extend-Breeder-other-scripting-PyFoam
    * swak4Foam https://github.com/Unofficial-Extend-Project-Mirror/openfoam-extend-swak4Foam-dev
    * compressibleTools library https://github.com/unicfdlab/libcompressibleTools
* UniCFD lab modules
    * QGD & QHD solver for regularized gasdynamic and hydrodynamic equations, https://github.com/unicfdlab/QGDsolver 
    * Hybrid central solvers for compressible flows in Mach range from 0 to 5, https://github.com/unicfdlab/hybridCentralSolvers
    * libAcoustics library for far field acoustics, https://github.com/unicfdlab/libAcoustics
    * salinityBoussinesqFoam solver for buoyancy driven flows solver, https://github.com/unicfdlab/salinityBoussinesqPimpleFoam
    * libSchemes library with tailored numerical schemes for advection, https://github.com/unicfdlab/libSchemes
    
Installation
============

1. Download OpenDTEF https://github.com/unicfdlab/OpenDTEF from the corresponding branch (v1812 corresponds to OpenFOAM-v1812, v1912 corresponds to OpenFOAM-v1912)

2. Build OpenDTEF with Allwmake script (for example it is in $HOME/OpenDTEF/OpenDTEF-v1912):

export WM_NCOMPPROCS=10 #Number of processors
export WM_MPLIB=SYSTEMOPENMPI #Use system version of OpenMPI
source /unicluster/bl2x220Cluster/bem/python/2.7.11/env #Path to the python
source $HOME/OpenDTEF/OpenDTEF-v1912
cd $HOME/OpenDTEF/OpenDTEF-v1912 && ./Allwmake

3. Download all needed sources from corresponding branches (see above), or request united archive from developers

    
