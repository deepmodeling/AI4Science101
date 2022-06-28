## Rare Events and Enhanced Sampling

  - Molecular dynamics algorithms have time reversibility and ergodic hypotheses. We assume that all states of a molecule have a probability to be explored (or traversed/sampled) after a sufficiently long simulation. These states include ground states, meta-stable states, and some high-energy states (unstable states). When the simulation reaches equilibrium, the distribution of molecular conformations in the system satisfies **the Boltzmann distribution** under its **ensemble**.

  - Different states have different probabilities to be sampled. In most cases, the molecules are stuck in a local minimum on the energy surface, and it is difficult to jump over the energy barriers. Therefore, under finite-time simulations, the probability of sampling some high-energy state or another meta-state separated by an energy barrier is very low. These are **rare events**.
    
      -  Here, it can be compared with Monte Carlo (MC) simulations of a high-dimensional function, starting from a random value of the high-dimensional function to explore the global minima of the function. This can take a lot of time and computational resources.

  - To increase the probability of rare events occurring in MD simulations, the simulation process can be interfered with using various methods:
    
      - Enhanced sampling based on temperature:
        
          - Raise the temperature, lower the energy barriers, and increase the probability of rare events.
        
          - Replica-Exchange Molecular Dynamics (REMD)[5], selective integrated tempering sampling (SITS)[6], etc.
    
      - Enhanced sampling based on bias potential:
        
          - Collective variables (CV), are functions of system coordinates. The free energy are defined on collective variables. (Please refer to the difference between free energy and potential energy)
        
          - Add bias potential to the given CVs during the simulations, which can push the trajectory out of the local minima on the energy surface to explore other states.
        
          - Metadynamics[7], VES[8], RiD[9], etc.
        
          - Traditional boosted sampling methods based on bias potential suffer from **the curse of dimensionality.**