## AI in MD

The current difficulties restricting MD simulation are as follows:

  - Simulation accuracy
    
      - Introduced by the classical force field approximations to quantum mechanics.

  - Sampling efficiency
    
      - This is the most essential problem of MD. It is partly solved by enhanced sampling techniques but traditional enhanced sampling methods cannot solve high-dimensional problems. Excessive heating or aggressively increasing bias potential can lead to denaturation of systems.

Here, some people draw inspiration and seek solutions from deep learning to try solve these problems.

  - DeePMD[10] 
    
      -  By fitting quantum chemical data with neural networks, a potential energy surface with quantitative accuracy is obtained. The computational complexity of neural networks is far less than solving Schrödinger equations, so DeepMD can achieve molecular dynamics simulations with high-precision.

  - Neural-networks-based enhanced sampling
    
      - These methods obtain the representation of the high-dimensional free energy surface by fitting the mean-force data using neural networks. The bias potential is applied to the system to boost simulations, where neural networks alleviate the high-dimensional problem of multiple CVs. These works include NN-VES, Reinforced Dynamics, etc.

  - CV Discovering
    
      - Reduce the dimensionalities of the data through machine learning methods (SVM, VAE, GAN, etc.) to find the most essential collective variables. TorchCV[11] is a good example for this.

**Difficulties:**

  - How to generate MD data for training ML models?
    
      - Possible solutions: active learning, concurrent learning

  - It is temporarily hard to do end-to-end simulation with similar efficiency to well-developed MD software.
    