
This repository contains data related to the Bachelor's thesis "Performance Engineering for Hierarchical Grids in AutoPas" by Alexander Glas.

The data includes template input files, Python scripts that convert these templates into the input files used for training, and SLURM job arrays. These are mostly adaptations from https://github.com/SamNewcome/Algorithm-Selection-in-Short-Range-Molecular-Dynamics-Simulations/tree/main.

Additionally, this repository contains all Jupyter notebooks used to generate figures and images for the thesis.

Software version:
AutoPas and md-flexible commit id: 5bb7317
Compiler version: GCC 13.2.0

cmake version: 3.30.0

cmake options used:
cmake -S . -B build\
  -DCMAKE_BUILD_TYPE=Release \
  -DAUTOPAS_ENABLE_ENERGY_MEASUREMENTS=OFF \
  -DAUTOPAS_OPENMP=ON \
  -DAUTOPAS_USE_VECTORIZATION=ON \
  -DAUTOPAS_VECTOR_INSTRUCTIONS=AVX2 \
  -DMD_FLEXIBLE_MODE=SINGLESITE \
  -DMD_FLEXIBLE_USE_MPI=OFF \
  -DAUTOPAS_ENABLE_RULES_BASED_AND_FUZZY_TUNING=OFF \
  -DAUTOPAS_ENABLE_FAST_MATH=OFF
cmake --build build --target md-flexible -j
