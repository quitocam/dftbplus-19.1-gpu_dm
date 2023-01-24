# GPU Density Matrix construction for DFTB+

This patch utilizes MAGMA BLAS functions to construct the density matrix in the GPU for DFTB+. 

## Building

* The patch must be applied to DFTB+ 19.1.

https://github.com/dftbplus/dftbplus/releases/download/19.1/dftbplus-19.1.source.tar.xz

* To apply the patch must go to the location where the dftbplus-19.1 directory resides and do as follows:

$ patch -p0 < dftbplus-19.1-gpu_dm.patch

* For compilation refer to the INSTALL.rst file for the instructions.

* Fortran pre-processing flag -Dmagma_devptr_t="integer(kind=8)" must be used.
