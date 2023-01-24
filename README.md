# GPU Density Matrix construction for DFTB+

This patch utilizes MAGMA BLAS functions to construct the density matrix in the GPU for DFTB+. 

## Building

* The patch must be applied to DFTB+ 19.1.

https://github.com/dftbplus/dftbplus/releases/download/19.1/dftbplus-19.1.source.tar.xz

* The patch must be applied in the location of the dftbplus-19.1 directory as follows:

$ patch -p0 < dftbplus-19.1-gpu_dm.patch

* For compilation refer to its INSTALL.rst file for the instructions.

* Fortran pre-processing flag -Dmagma_devptr_t="integer(kind=8)" must be used.
