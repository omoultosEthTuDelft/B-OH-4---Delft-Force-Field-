
In this directory you will find sample simulation files for MD simulations in LAMMPS (version August 2018) for transport properties of H2 in aqueous NaB(OH)_4 solutions. The details regarding the MD simulations and the force fields used can be found in the main manuscript. 

The details regarding the LAMMPS software and the functions used can be found in the LAMMPS manual: https://docs.lammps.org/Manual.html

The simulations inputs (and outputs) shown in these directories are at 298 K, 1 atm, and a molality of 3 mol NaB(OH)_4 / kg water. The units, temperature, pressure and the length of equilibration/production runs can be controlled in the "simulation.in" file. The "forcefield.in" file gives information on the force fields used and the "data.lmp" file is an initial configuration generated using packmol (see: https://m3g.github.io/packmol/).

Please note that in order to use the "fix integrate all rigid/npt/small molecule" command in LAMMPS we had to introduce a dummy site near Na (within the sigma of Na) (denoted as site M in the force field file, i.e., "forcefield.in") with no charge / LJ interactions, as the "fix integrate all rigid" command cannot be used when one of the molecules/ions is a single particle. 
