## What does AI bring to the scientific Community?


![image](https://dp-public.oss-cn-beijing.aliyuncs.com/community/Scientific%20Discovery%20in%20the%20era%20of%20AI/Protain_S_P.png)


#### Traditional Discovery Process in Science (a day of a scientist)

  - Goal - Drug design (AI can help in different phases of drug design)

  - Hypothesis - Hand-crafted design (AI can help search the vast chemical space and propose drug candidates)

  - Simulation - Computer simulation (AI can accelerate and improve the accuracy of computer simulation)

  - Experiment - lab experiment (AI can guide lab experiment design)

  - Result analysis - Statistical analysis (AI can analyze high-dimensional data)

  - Repeat

  - Conclusion & Finding

Goals             | Traditional Methods                                                             | AI-Based Methods                                                          
------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------
Drug Design       |- Error-prone and intuition-based workflows                                       | - AI aided rational drug design
Virtual Screening |- Docking (based on physical scoring functions) <br> - 2D/3D/based on pharmacophore similarity search | - Neural network-based scoring functions <br> - Generative models                    
Lead Optimization | - MD-based free energy calculation with empirical force field<br> - Wet-lab experiment                     | - AI-predicted binding<br>- Simulation with more accurate force fields developed with neural networks  affinity| 
Drug Synthesize   | - Error-prone experiments to find optimal synthesis route and reaction conditions | - Retro-synthesis analysis by AI models <br>- AI predicted reaction outcomes<br>- Automated wet-Lab experiment                 
ADMET             | - Experiments                                                                     | - AI-based prediction models                                                


<center><span id="tab:addlabel" label="tab:addlabel">Table 1: Examples of AI methods in assisting the drug discovery process</span></center>

#### Even decades ago, AI was widely used in the scientific community

  - Example: principal component analysis/PCA, linear regression, Kalman Filter, clustering algorithms, etc.

#### Data analysis empowered by modern AI

  - **Why has AI become so popular recently? (What changed the game?)**
    
      - **Accumulated Big Data**
    
      - **Advanced Algorithms (especially Rising of Deep Learning)**
    
      - **Improved Computing Power and Storage**

  - **What is data?** Data are individual facts, statistics, or items of information, often numeric. In a more technical sense, data are a set of values of qualitative or quantitative variables about one or more persons or objects.

  - **What is learning?** Learning refers to machine learning, which is the study of computer algorithms that improve automatically through experience.

  - **Why do we learn from data?** Learning from accumulated data enables us to analyze data and execute certain tasks.

  - **What are common tasks that could be solved by AI?**
    
      - **Predictive tasks** refer to predicting the value or status of something of interest.
        
          - Example: predict whether an image is a cat or dog.
    
      - **Generative tasks** refer to generating new data by learning from existing data.
        
          - Example: generate new drug-like molecules.
    
      - **Decision-making tasks** refer to making decisions based on the information provided.
        
          - Example: decide on trading strategies for the stock market.

  - **How do we learn from data?** Two essential components of learning from data are (1) data and (2) learning.
    
      - **Data** includes two main components, data points, and labels, data points refer to the single instances of facts, statistics, or items of information, while labels are meaningful and informative tags for the data points. (Note the labels are often expensive to obtain, thus most of the data are unlabelled)
        
          - Data Points:\(X\) cab be in any format, text, image, graph, etc.
            
            \- Example: images of cats and dogs
        
          - Labels: \(Y\) are informative tags
            
            \- Example: cat or dog
    
      - **Learning** essentially involves three main broad categories, **Supervised Learning**, **Unsupervised Learning, and Reinforcement Learning**. We include an additional learning diagram, **Active Learning**, which is commonly used in scientific discovery.
        
          - **Supervised Learning** learns with labeled data, usually, for predictive tasks, a special case is Semi-supervised Learning where only partial data are labeled, since labels allow us to directly assess the predictive performance of a machine learning model in certain circumstances.
            
            \- Example: predicting molecular properties from molecular structures
        
          - **Unsupervised Learning** learns with unlabeled data and discovers patterns from data, usually for clustering, dimensionality reduction, and visualization tasks. Another rising topic, Self-supervised Learning, also requires no labeled data by training models to predict “missing” or masked parts of the input, and it focuses more on predictive tasks similar to supervised learning.
            
            \- Example 1: clustering galaxy images with similar patterns
            
            \- Example 2: clustering molecule conformations with similar patterns which reduces the workloads for MD analysis
        
          - **Reinforcement Learning** concerns how intelligent agents ought to take actions in an environment in order to maximize the notion of cumulative reward.
            
            \- Example: AI agent for nuclear fusion reactor control
        
          - **Active Learning** is a learning algorithm that can request labels (or propose experiments) that provide information that be most useful for it to improve predictive performance. It is also referred to as optimal experimental design.
            
            \- Example: uncertainty estimation to guide the experiment/data collection

  - **How do we collect or represent data?**
    
      - **Representation Learning** is a set of techniques that allows a system to automatically discover the representations needed for feature detection or classification from raw data. This replaces manual feature engineering and allows a machine to both learn the features and use them to perform a specific task.
        
          - **Tabular Representation (columns are features)**
            
            \- Example: weather data stored in tables
        
          - **Grid Representation (stored in grids)**
            
            \- Example: cell images
        
          - **Sequence Representation (stored in sequences)**
            
            \- Example: genes
        
          - **Graph Representation (stored in nodes and edges)**
            
            \- Example: molecular graphs
        
          - **Geometry Representation (stored in 3D geometries)**
            
            \- Example: protein structures

  - **Could we generate new data?**
    
      - **Generative Modeling** learns the distributions of observed samples and generates unseen samples.
        
          - Example: goal-oriented molecule generation, protein conformations sampling
