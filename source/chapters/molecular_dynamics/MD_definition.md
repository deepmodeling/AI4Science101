## What is Molecular Dynamics?

Molecular Dynamics (MD) studies how atomic coordinates evolve under given conditions. It relies on the framework of **classical mechanics**(also known as **Newtonian mechanics**) and simulates the motion of molecular systems numerically. For instance, you can imagine the motion of two rigid balls connected by a spring.


### Experiments on a computer

MD is a computational method, a chemical experiment performed on computers. Let's imagine a chemical experiment in the real world first. One may have to prepare experimental instruments and drugs, set instrument parameters, conduct experiments, wait for chemical reactions to proceed, obtain experimental results, and then analyze experimental results. MD is quite similar; we use a table to compare MD with the traditional chemical experiments:

| Chemical experiment              | Molecular dynamics simulation                                                                                   |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Prepare experimental instruments | Prepare computing hardware (CPU, GPU, etc.)<br>Prepare calculation software (Gromacs, Lammps, etc.)                                                                     |
| Prepare experimental drugs       | Prepare a file describing the molecular structure as an initial conformation for the simulation process         |
| Set instrument parameters        | Set simulation parameters (simulation temperature, simulation time, etc.)<br>Set force field parameters (parameters that can be analogous to spring coefficients)                   
| Conduct chemical experiments     | Run MD simulations                                                                                              |
| Get experimental results         | Get the simulated trajectory                                                                                    |
| Analyze experimental results     | Analysis of physico-chemical properties from trajectories obtained from simulations (calculation of statistics) |


<center> <span id="tab:addlabel" label="tab:addlabel">Table 1: Molecular Dynamics Procedure</span> </center>

### Why do we run MD?

Molecular dynamics simulations can allow us to simulate chemical and physical processes on computers, obtain kinetic information at the microscopic scale, provide theoretical support for experiments and guide chemical experiments. Moreover, computational simulations can help reduce the cost of manually conducting experiments. MD can also be performed under special (usually severe) conditions (ultra-high pressure, ultra-high temperature, strong electric field, magnetic field, etc.)

However, its basis in classical mechanics means that MD can only be effective for physical processes at the molecular scale (e.g. $nm$). For simulations involving electronic structures MD doesn't work.

  - Systems that can be simulated with classical molecular dynamics:
    
      - Protein systems (protein folding problems, etc.)
    
      - RNA systems
    
      - Atomic-scale material systems
    
      - Free energy calculation
    
      - Catalytic reactions that do not involve electron transfer

  - Problems that classical MD *can not* solve (or cannot be solved only by classical MD):
    
      - Magnetic and electrical properties of materials (requires quantum chemistry tools)
    
      - Calculate the energy of molecular conformation (requires quantum chemistry method, current software include Gaussian, Vasp)
    
      - Protease-catalyzed reactions involving electron transfer (requires QM/MM method)
    
      - Chemical reactions involving electron transfer (requires QM/MM method)

### The inputs and outputs of MD

Inputs to molecular dynamics simulations are an initial conformation of molecules. They should contain the coordinates of the atoms, the information of chemical bonds among atoms (also called topology information), etc.

The outputs of molecular dynamics are molecular trajectories (trajectory refers to a continuous molecular motion in the coordinate space or Cartesian space) simulated from the initial conformations.