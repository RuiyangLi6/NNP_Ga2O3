# Neural Network Potential for Beta-Ga2O3
Here are the training data sets and trained potential for beta-Ga2O3 crystal.

1) First, there are two data sets. In the folder "raw_with0K", we have ab initio raw data of Ga2O3 at 0 K (DFT) and finite temperatures (50 - 600 K), which corresponds to 9200 snapshots in total. In the folder "raw_without0K", only AIMD data at finite temperatures is included. The data sets are prepared in the format of numpy binary data that can be directly used by the training program.

2) We used the DeePMD-kit to train this neural network potential. For instructions of the potential development, please go to https://github.com/deepmodeling/deepmd-kit.

3) "Ga2O3.pb" is the final frozen potential model, which can be used with LAMMPS to perform molecular dynamics simulations.
(P.S. If you find that this potential is not compatible with your computer or DeePMD program, it is recommended to install the latest DeePMD-kit and train your own potential with the given raw data.) 

4) An example script for training is included ("train.json"). To use it, please follow the instructions for DeePMD-kit.

5) An example LAMMPS input file is provided ("in.run"). Please make sure you have installed DeePMD-kit and compiled LAMMPS such that it can perfrom MD simulations with DeePMD potential.

6) "ga2o3.data" is a atomic coordinate file for a 4 by 4 by 4 supercell of beta-Ga2O3.
