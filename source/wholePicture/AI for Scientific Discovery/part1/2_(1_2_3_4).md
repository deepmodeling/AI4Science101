## 2.1  Manifesto
Ever since the time of Isaac Newton, there have been two different paradigms for scientific research: the **Keplerian** paradigm and the **Newtonian** paradigm.

<center> <img src=https://dp-public.oss-cn-beijing.aliyuncs.com/community/figures-AI%20for%20Scientific%20Discover/Keplerian.png# pic_center width="30%" height="30%"/> 
<img src=https://dp-public.oss-cn-beijing.aliyuncs.com/community/figures-AI%20for%20Scientific%20Discover/Newtonian.png# pic_center width="36%" height="30%" /> </center>

<center>Figure 1: Portrait of Johannes Kepler and Isaac Newton, from Wikipedia</center>


The Keplerian paradigm, often referred to as the ``data-driven'' approach, expects to extract new physical rules or trends through data analysis and utilize these rules to solve actual problems. The discovery of Kepler's laws of planetary motion was the canonical implementation of this paradigm. Nowadays, many successful examplesbioinformatics and cheminformatics have demonstrated the effectiveness of this paradigm in areas from multi-scale modeling, protein structure prediction, to drug discoveryincluding drug discovery or disease treatment. 

The Newtonian paradigm is based on working from first principles, with the aim to figure out fundamental physical rules that govern the world as we know it. Based on these principles, scientists are able to explain most of the experimentally observed phenomenons. One of the most successful theories is quantum mechanics because it almost prepares us with all necessary laws for much of engineering and natural sciences. However, as pointed out by Dirac, "the exact application of these laws leads to equations much too complicated to be solved". The central difficulty is called "the curse of dimensionality", i.e., the problems we are encountered are actually too high-dimensional and cannot be solved efficiently. For a long time, natural scientists have only had limited ability to handle these equations with at most thousands of variables.

**<center> BUT things are going to change! </center>**

Machine learning, especially deep learning (or generally AI) techniques emerge as effective tools to approximate arbitrary high-dimensional functions as illustrated by its unprecedented success in computer vision (CV) and natural language processing (NLP). In the Newtonian paradigm, AI methods have been applied to incorporate physical laws to solve more much complicated problems or system simulations than toy examples. In the Keplerian paradigm, AI can be directly applied to analyze and learn from data in an end-to-end manner. With the promises of AI in solving real and challenging scientific problems, **"AI for Science" (AI4S)** has become established as a new term and prevailed in both AI and scientific research communities. In the past few years, successful applications of AI methods have opened up a wide research avenue for both communities, from AlphaFold2
[1]
that solves the 50-year-old protein structure prediction puzzle, DeePMD
[2] 
that extending *ab initio* simulation to unprecedentedly large scales, to controlling nuclear reactor with AI agents
[3]
. The new paradigm of scientific research empowered by AI has been formed, and aforementioned successful examples have paved the way for this new paradigm. However, as scientific discovery has a very broad scope with many different disciplines many grand challenges that are critical to our lives still remain unsolved. Despite the early success, we have to acknowledge that AI for Science is still nascent and requires joint efforts from both AI and scientific communities. 

<center><img src=https://dp-public.oss-cn-beijing.aliyuncs.com/community/figures-AI%20for%20Scientific%20Discover/Paul.png# pic_center width="40%" height="40%" /></center>
<center>Figure 2: Paul A. M. Dirac (1902 – 1984), from wikipedia</center>

We are living in an era with the opportunity and means to tackle grand challenges in scientific discovery. To facilitate this emergent field and bridge gaps between AI and scientific communities, this blog aims to equip researchers in the AI community with some basic scientific knowledge and an overview of new challenges in scientific discovery, which may appear significantly different from common AI application areas such as computer vision and speech recognition. 

## 2.2 Success of AI in Scientific Discovery
### 2.2.1 Protein Structure Prediction

When it comes to AI for Science, arguably the most famous and successful example of AI-advanced scientific discovery is AlphaFold2 which addresses the problem of accurately predicting protein 3D structures from their sequence, one of the "holy grail" problems in structural biology. The structures of proteins are essential to their biological functions and accurate 3D modeling at the atomistic level is significant for a variety of field from drug discovery to synthetic biology. However, resolving structures experimentally is highly expensive and time-consuming, so computational methods to predict accurate protein structures have long been studied, represented by the series of CASP competitions[4]. Anfinsen's hypothesis, stating that for most proteins, the native structures in standard physiological environments are determined solely by the proteins' amino acid sequences, grounds the study of computational method for the protein structure prediction problem. Traditionally, structural biologists utilize "homology modeling" to make such predictions. In those methods, multiple proteins, whose sequences are similar to the query one and structures have already been resolved experimentally, will be found. These structures will be then be assembled to provide the predicted result. The accuracy of homology modeling depends heavily on sequence identity, and sometimes fails to reach a satisfying level. Deep learning methods, however, have stronger ability to discover correlations between sequences and structures. With carefully-designed attention-based neural networks and multiple-sequence-alignment (MSA) information, in 2020, the AlphaFold2 model achieved an astonishing average RMSD of 0.96 angstroms on the test cases in the prestigious CASP competition. Such accuracy is even comparable to experimental errors and AF2 was considered to make a breakthrough in solving this 50-year structural biological puzzle.


<center><img src=https://dp-public.oss-cn-beijing.aliyuncs.com/community/figures-AI%20for%20Scientific%20Discover/illustration_protain.png# pic_center width="40%" height="40%" /></center>
<center>Figure 3: An illustration of AI predicted protein structure</center>

### 2.2.2 Multi-scale Modeling
As mentioned in the manifesto, the principles of our physical world are almost completely known but the mathematical equations are too complicated to be solved accurately. Therefore, for problems at different time and space scales, scientists have to develop different computational methods with the necessary approximations to reduce the computational complexity which is called multi-scale modeling in computational science. In this area, *ab initio* and classical molecular dynamics (shortened as AIMD and classical MD) are two widely used techniques. However, there has been a longstanding trade-off problem between the accuracy and efficiency of these methods. Specifically, in AIMD, the energy and forces of given systems are calculated by quantum mechanics (usually density functional theory or DFT), thus it is more accurate but more time-consuming. The computational complexity is $O\left (N^3\right)$, where $N$ is the number of electrons in the systems. In classical MD, the potential energy surface is given by fixed mathematical forms with manually curated parameters (named "force fields"), so it is much faster ($ O\left(N\right)$) but less accurate. Recently, AI methods have been largely developed to bridge this gap
[5,6,7]
. Specifically, researchers designed neural networks that preserving necessary physical symmetries and generated a neural representation of atomic configurations which could be used to fit DFT-level potential energy surfaces. However, it still requires large-scale dataset to train such models. Concurrent learning
[8]
workflows are here to rescue, by heuristically exploring the configuration space to collect as few data as possible. In this manner, construction of neural network potentials becomes more automatic, which further enables a variety of applications in complex systems in condensed matters as well as material science
[9]
.

<center><img src=https://dp-public.oss-cn-beijing.aliyuncs.com/community/figures-AI%20for%20Scientific%20Discover/Protein-Multimers.png#pic_center width="40%" height="40%" /></center>
<center>Figure 4: An illustration of protein-multimers</center>

## 2.3 Why is AI for Science different?
### 2.3.1 Data is Important

Undoubtedly, AI methods rely on datasets with both high-quality and high-quantity to achieve excellent performance in solving problems, which has been demonstrated by ImageNet
[10]
, Cifar-10[11]
, etc. This is also very true for scientific problems, examplified by RCSB Protein Data Bank (PDB)[12]
. This database, containing approximate 200,000 data entries and maintained by researchers all over the world for over 40 years, is one of the best database for experimentally resolved biomolecular structures. Deep learning methods would never reach such a success without efforts from maintainers of PDB. In particular, scientific problems usually involve real and challenging scenarios for many AI-interested topics, e.g., out-of-distribution generalization, low-data regime learning, etc. And it is often the case that in many topics, no high-quality dataset is available to generate effective deep learning models. Therefore, it is encouraged that AI researchers to pay more attention to data collection and structuralization, during which domain expertise and joint efforts are required.
% Some examples include learning from structures studied in several years ago to predict structures of researchers' interest today for out-of-distribution generalization, learning from highly expensive quantum property data to predict property for new data (low-data regime), etc.
### 2.3.2 Problem Formulation
Many scientific discovery problems are much more complex than simple classification or regression tasks. For AI researchers, scientific problems have to be decomposed and well-formulated to an extent that inputs, outputs, and objective functions (often needs to be differentiable) can be clearly defined. For example, "drug design" is a huge pipeline which consists of a sequence of steps and is obviously not a well-formulated problem itself. Instead, we can decompose this problem into different pieces that are AI-solvable: molecular property prediction for virtual screening molecular databases, molecular generation for proposing better drug candidates, etc. Problems failed to be compliant with this standard are often referred to as "dirty" ones, and are unlikely to be addressed solely with AI methods.