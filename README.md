# Reconstruction-of-Trajectory

The goal of this project is to use the preprocessed static data set to reconstruct a fairly complex vehicle trajectory.

The Input data has 4 variables i.e,
  * Timestamp
  * Displacement
  * Yaw rate
  * Acceleration

#### The data set can be seen below,

![Input data set](/figures/Input_data.PNG)

**`timestamp`** - Timestamps are all measured in seconds. The time between successive timestamps **Δt** will always be the same within a trajectory's data set (but not between data sets).

**`displacement`** - Displacement data from the odometer is in meters and gives the **total** distance traveled up to this point.

**`yaw_rate`** - Yaw rate is measured in radians per second with the convention that positive yaw corresponds to **counter-clockwise** rotation. 

**`acceleration`** - Acceleration is measured in m/s2 and is always in the direction of motion of the vehicle (forward). 

### Solution

Here I have created four functions named,
* `get_speeds` - returns a length N list where entry i contains the speed (m/s) of the vehicle at t = i * Δt 

* `get_headings` - returns a length N list where entry i contains the heading (radians,  0≤𝜃<2𝜋 ) of the vehicle at t = i * Δt 

* `get_x_y` - returns a length N list where entry i contains an `(x, y)` tuple corresponding to the x and y coordinates (meters) of the vehicle at t = i * Δt 

* `show_x_y` - generates an x vs. y scatter plot of vehicle positions. 

Once the functions are defined, using these functions the below results were obtained.


**1.Roundabout** (For the above data set)

![Roundabout](/figures/trajectory_1.PNG) 

**2.Lane Crossing**

![Lane crossing](/figures/trajectory_2.PNG)

**3.Parallel Parking**

![Parallel parking](/figures/trajectory_3.PNG) 

