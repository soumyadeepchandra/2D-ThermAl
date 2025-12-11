# 2D-ThermAl: Physics-Informed Framework for Thermal Analysis of Circuits using Generative AI
This repository contains code for the paper

# Abstract 
Thermal analysis is increasingly critical in modern integrated circuits, where non-uniform power dissipation and high transistor densities lead to rapid temperature spikes and reliability concerns. Traditional methods such as FEM-based simulations are accurate but computationally prohibitive for early-stage design, often requiring multiple iterative redesign cycles to resolve late-stage thermal failures. To address these challenges, we propose `ThermAl', a physics-informed generative AI framework which effectively identifies heat sources and estimates full-chip transient and steady-state thermal distributions from input activity profiles. ThermAl leverages a hybrid U-Net architecture enhanced with positional encoding and a Boltzmann regularizer to maintain physical fidelity. Our model is trained on an extensive dataset of heat dissipation maps for more than 200+ circuit configurations, ranging from simple logic gates (e.g., inverters, NAND, XOR) to complex designs, generated via COMSOL and Cadence EDA flows. The dataset captures diverse activity patterns, and we note that material-dependent thermal properties may require targeted fine-tuning to ensure accuracy across different fabrication contexts. Experimental results demonstrate that ThermAl delivers precise temperature mappings for large circuits, with a root mean squared error (RMSE) of only $0.71^{\circ}$C and outperforms conventional FEM tools by running up to $\sim200\times$ faster. We analyze performance across diverse layouts and workloads, and discuss its applicability to large-scale EDA workflows. Limitations such as 2D-only modeling and real-world validation are addressed with concrete future directions, including 3D extension, generalization across technology nodes, and transfer learning strategies. 

### Motivation for ThermAl
![alt text](https://github.com/soumyadeepchandra/2D-ThermAl/blob/main/Motivation.jpg?raw=true)

### Model Pipeline
![alt text](https://github.com/soumyadeepchandra/2D-ThermAl/blob/main/Model.jpg?raw=true)


## Enviroment
Pytorch == 2.0.1, 
torchvision == 0.15.2, 
python == 3.11, 
CUDA == 11.7

## Datasets used
The dataset can be found here: [2D-ThermAl]([https://bit.ly/thermal2d](https://purdue0-my.sharepoint.com/:f:/g/personal/chand133_purdue_edu/IgAB4G-8tmVgQ5PNUFUJt_IVASPrY6_te7pSm8-dmKiQgn4))
Please email: chand133@purdue.edu if you want access to download.

1. Download the dataset data.zip (Cholec80 / any other dataset). 

2. Unzip the data.zip file to the current folder (./Dataset)

3. The data.zip consists of the thermal images generated using COMSOL used for training/testing the ThermAl model.
The naming format followed is as follows: ./<Train/Test>/<transient timestep>/<image number>_<transient timestep>.png

e.g.: 558_005.png represents the dataset log: 558 and 005 is the 5th transient step starting from 001 to 041.


## Codebase
The codes have three subfolders for ablation:
1. Without Image Pair (Basic encoder-decoder network with feature concatenation)
2. With Image Pair (Encoder-decoder with Condition-based Source-Target Image Pair Learning)
3. With Physics Regularizer (Complete network with physics regulated loss function to bound the output to obey physics-constrained heat diffusion)


## Citation

If you find our codes or paper useful, please consider giving us a star or cite with:  

The final report submitted is under review in IEEE TCAD 2025.


