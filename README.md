# Enhancing classical nanoparticle simulations with electronic corrections and machine learning

Classical simulations of materials and nanoparticles have the advantage of speed and scalability but at the cost of precision, whilst also lacking the ability to describe electronic properties. Quantum mechanical and electronic structure simulations have the advantage of providing accurate estimations of the electronic structure and charge transfer but are typically limited to small and simple systems due to the increased computational complexity. In this project, identical sets of classical and electronic structure simulations are used to train an artificial neural network to predict an energy correction term using structural properties of arbitrary gold nanoparticles to improve the classical simulation.

This repository provides a set of code bases for feature extraction and machine learning to predict energy differences between two metal nanoparticle simulations implemented using python and Jupyter notebooks. This code can be split into three parts based on the workflow.

  1. Feature extraction of nanoparticle structural properties. This has been implemented to extract general structural features from a point cloud LAMMPS simulation, along with the Mermin energy and Fermi level from a Density Functional Type Binding (DFTB+) simulation and is contained in the ```feature_extraction``` directory.

  2. Data science code that can be used to find and remove highly correlated features. This is contained in the ```data_science``` directory.

  3. Machine learning code implemented using the Sci-Kit learn python module that uses a decision tree regressor to identify important features and then uses an artificial neural network to generate a prediction of the energy correction term. This is contained in the ```machine_learning``` directory.
