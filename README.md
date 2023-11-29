# GW Project 4

# Background:
This dataset is officially managed by the Jet Propulsion Laboratory (JPL) of the California Institute of Technology, an organization affiliated with NASA. It encompasses a comprehensive collection of data related to asteroids, publicly accessible through their website. The fundamental definitions of the dataset columns are outlined below.
Website Link: [JPL Small-Body Database Search Engine](https://ssd.jpl.nasa.gov/tools/sbdb_query.html)

# Objectives:
1) Explore the feasibility of training a model for the identification of hazardous asteroids.
2) Investigate methods to augment the model with additional data while maintaining data integrity.
3) Determine the essential data required for accurate identification of hazardous asteroids.

# Essential Data for Asteroid Identification: 
While the dataset initially comprised numerous columns, we thought it was best to keep what's listed down below. These attributes are crucial for the model training aimed at identifying potential hazardous asteroids:
- NEO (Near Earth Object) Flag
- H (Absolute Magnitude Parameter)
- Diameter (Object Diameter)
- Moid (Earth Minimum Orbit Intersection Distance)
- RMS (Root Mean Square, representing the error of the fit of the asteroid's orbit to the observed data)
- Class (Spectral Class or Type)

# Model Training Results:
    First Model Features:
- Sequential model
- 36 inputs
- 2 layers with Relu activation
- Last layer with sigmoid activation
- Compiled with loss- binary cross entropy and optimized with adam
- Epochs: 10
- Loss: 0.01; Accuracy 99.86%

      Second Model Features:
- Changes: “sigma” columns removed from dataset, fewer nodes per layer
- Sequential model
- 24 inputs
- 2 layers with Relu activation
- Last layer with sigmoid activation
- Compiled with loss- binary cross entropy and optimized with adam
- Epochs: 10
- Loss: 0.01; Accuracy 99.86%

      Third Model Features:
- Changes: All but 6 key feature columns removed from dataset, fewer nodes per layer
- Sequential model
- 6 inputs
- 2 layers with Relu activation
- Last layer with sigmoid activation
- Compiled with loss- binary cross entropy and optimized with adam
- Epochs: 10
- Loss: 0.002; Accuracy 99.89%
 
      Fourth Model Features:
- Changes: All but 3 key feature columns removed from dataset, fewer nodes per layer, 1 layer dropped
- Sequential model
- 3 inputs
- 1 layer with Relu activation
- Last layer with sigmoid activation
- Compiled with loss- binary crossentropy and optimized with adam
- Epochs: 10
- Loss: 0.003; Accuracy 99.82%

      Fifth Model Features:
- Changes: Reverted data back to third model attempt columns, layers and nodes. Data was processed using these 6 columns resulting in more data to train with.
- Sequential model
- 6 inputs
- 2 layer with Relu activation
- Last layer with sigmoid activation
- Compiled with loss- binary crossentropy and optimized with adam
- Epochs: 10
- Loss: 0.001; Accuracy 99.92%

# Group Members:
Amie Shank, Katherine Young, Siobhan Byrne, Amber Amparo
