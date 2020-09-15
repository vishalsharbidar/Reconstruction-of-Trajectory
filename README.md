# Reconstruction-of-Trajectory

The goal of this project is to use the preprocessed static data set to reconstruct a fairly complex vehicle trajectory.

The Input data has 4 variables i.e,
  * Timestamp
  * Displacement
  * Yaw rate
  * Acceleration

#### The data set can be seen below,

![Input data set](/figures/Input_data.PNG)

timestamp - Timestamps are all measured in seconds. The time between successive timestamps Δt will always be the same within a trajectory's data set (but not between data sets).

displacement - Displacement data from the odometer is in meters and gives the **total** distance traveled up to this point.

yaw_rate- Yaw rate is measured in radians per second with the convention that positive yaw corresponds to counter-clockwise rotation. 

acceleration - Acceleration is measured in m/s^2 and is always in the direction of motion of the vehicle (forward). 
