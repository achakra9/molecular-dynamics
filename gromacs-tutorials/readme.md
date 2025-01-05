This is my attempt at learning gromacs from various tutorials. I will keep updating it as I progress. Currently going through the tutorials documented in mdtutorials.com website.

- Installing gromacs
  - cretae a conda environment with the command `conda create -n gromacs python=3.11`
  - activate the environment with `conda activate gromacs`
  - To install GROMACS `conda install -c conda-forge gromacs`
  - To verify the installation type `gmx --version`. This is what I see when I do this:
  ```
gmx --version
                   :-) GROMACS - gmx, 2024.4-conda_forge (-:

Executable:   /opt/anaconda3/envs/gromacs/bin.AVX2_256/gmx
Data prefix:  /opt/anaconda3/envs/gromacs
Working dir:  /Users/arnab/GitHub/molecular-dynamics/gromacs-tutorials
Command line:
  gmx --version

GROMACS version:     2024.4-conda_forge
Precision:           mixed
Memory model:        64 bit
MPI library:         thread_mpi
OpenMP support:      enabled (GMX_OPENMP_MAX_THREADS = 128)
GPU support:         disabled
SIMD instructions:   AVX2_256
CPU FFT library:     fftw-3.3.10-sse2-avx
GPU FFT library:     none
Multi-GPU FFT:       none
RDTSCP usage:        disabled
TNG support:         enabled
Hwloc support:       disabled
Tracing support:     disabled
C compiler:          /Users/runner/miniforge3/conda-bld/gromacs_1730738380979/_build_env/bin/x86_64-apple-darwin13.4.0-clang Clang 18.1.8
C compiler flags:    -mavx2 -mfma -Wno-missing-field-initializers -O3 -DNDEBUG
C++ compiler:        /Users/runner/miniforge3/conda-bld/gromacs_1730738380979/_build_env/bin/x86_64-apple-darwin13.4.0-clang++ Clang 18.1.8
C++ compiler flags:  -mavx2 -mfma -Wno-reserved-identifier -Wno-missing-field-initializers -Weverything -Wno-c++98-compat -Wno-c++98-compat-pedantic -Wno-source-uses-openmp -Wno-c++17-extensions -Wno-documentation-unknown-command -Wno-covered-switch-default -Wno-switch-enum -Wno-switch-default -Wno-extra-semi-stmt -Wno-weak-vtables -Wno-shadow -Wno-padded -Wno-reserved-id-macro -Wno-double-promotion -Wno-exit-time-destructors -Wno-global-constructors -Wno-documentation -Wno-format-nonliteral -Wno-used-but-marked-unused -Wno-float-equal -Wno-conditional-uninitialized -Wno-conversion -Wno-disabled-macro-expansion -Wno-unused-macros -Wno-unsafe-buffer-usage -Wno-cast-function-type-strict SHELL:-fopenmp=libomp -O3 -DNDEBUG
BLAS library:        External - detected on the system
LAPACK library:      External - detected on the system
  ```
If we look at "OpenMP support" and "GPU support", it is clear that in my current machine I can run GROMACS in parallel, but I do not have GPU acceleration.

- Lysozome-water tutorial