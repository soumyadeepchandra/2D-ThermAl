Dataset:

The data.zip consists of the uncropped thermal images generated using COMSOL I have used for training/testing the ThermAl model.

The naming format followed is as follows: <image number>\_<transient timestep>.png



e.g.: 558\_005.png represents the dataset log: 558 and 005 is the 5th transient step starting from 001 to 041.





Codes:

The codes have three subfolders for ablation:

1\. Without Image Pair (Basic encoder-decoder network with feature concatenation)

2\. With Image Pair (Encoder-decoder with Condition-based Source-Target Image Pair Learning)

3\. With Physics Regularizer (Complete network with physics regulated loss function to bound the output to obey physics-constrained heat diffusion)





Literature References:

\[1] Hotspot: Huang, W., Stan, M. R., Skadron, K., Sankaranarayanan, K., Ghosh, S., \& Velusam, S. Compact thermal modeling for temperature-aware design. In Proceedings of the 41st annual Design Automation Conference (pp. 878-883).

\[2] LSTM+DCT: Sadiqbatcha, S., Zhao, Y., Zhang, J., Amrouch, H., Henkel, J., \& Tan, S. X. D. (2020, January). Machine learning based online full-chip heatmap estimation. In 2020 25th Asia and South Pacific Design Automation Conference (ASP-DAC) (pp. 229-234). IEEE.

\[3] Power Blurring: Ziabari, A., Park, J. H., Ardestani, E. K., Renau, J., Kang, S. M., \& Shakouri, A. (2014). Power blurring: Fast static and transient thermal analysis method for packaged integrated circuits and power devices. IEEE Transactions on Very Large Scale Integration (VLSI) Systems, 22(11), 2366-2379.

\[4] PACT: Yuan, Z., Shukla, P., Chetoui, S., Nemtzow, S., Reda, S., \& Coskun, A. K. (2021). PACT: An extensible parallel thermal simulator for emerging integration and cooling technologies. IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems, 41(4), 1048-1061.

\[5] ThermGAN: Jin, W., Sadiqbatcha, S., Zhang, J. \& Tan, S. Full-chip thermal map estimation for commercial multi-core CPUs with generative adversarial learning. Proceedings Of The 39th International Conference On Computer-Aided Design. pp. 1-9 (2020)



Report:

The final report submitted is under review in IEEE TCAD 2025.

