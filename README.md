Dataset:
The data.zip consists of the uncropped thermal images generated using COMSOL I have used for training/testing the ThermAl model.
The naming format followed is as follows: <image number>_<transient timestep>.png

e.g.: 558_005.png represents the dataset log: 558 and 005 is the 5th transient step starting from 001 to 041.


Codes:
The codes have three subfolders for ablation:
1. Without Image Pair (Basic encoder-decoder network with feature concatenation)
2. With Image Pair (Encoder-decoder with Condition-based Source-Target Image Pair Learning)
3. With Physics Regularizer (Complete network with physics regulated loss function to bound the output to obey physics-constrained heat diffusion)


Dataset:
The dataset can be found here: [2D-ThermAl](https://bit.ly/thermal2d)
Please email: chand133@purdue.edu if you want access to download.


Report:
The final report submitted is under review in IEEE TCAD 2025.

