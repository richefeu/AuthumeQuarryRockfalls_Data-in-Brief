This repository holds the datasets related to the paper in Data-in-Brief 

# Experiments

### The site of Authume quarry

[Photos site + explanantions]

[Two drop points P1 and P2]

### Deposite

The data files for the stop positions of the released boulders are named `EXP_endpoints/endpoints_P1.txt` (41 boulders) and `EXP_endpoints/endpoints_P2.txt` (48 boulders, the boulder at line #xx is the one with shape SP3A).
They are ASCII text files where the meaning of each column is described in the following table.  

| Column # | Description              |
|:--------:|:-------------------------|
| 1        | $x$ position (m)         |
| 2        | $y$ position (m)         |
| 3        | $z$ position (m)         |
| 4        | mass of the boulder (kg) |
| 5        | $L_1$ (m)                |
| 5        | $L_2$ (m)                |
| 5        | $L_3$ (m)                |

[Explain $L_1 \geq L_2 \geq L_3$...]
[Notice that the positions are given in the same cartesian framework that the one used in the simulation datasets.]
[Say how the mass has been measured or estimated] 

# Simulations



### Geometries

##### Digital terrain

The terrain topology is provided in the form of `.stl` ASCII files, and also in a more raw format of cloud points (`.xyz` ASCII files) in the folders `Geometries/STL` and `Geometries/Point_cloud`, respectively.

Any position in the dataset of this repository is a cartesian coordinate expressed in the same framework. [says y is upwards, ref to top view]

The limits of the digital terrain are given in the following table.

|         | min | max |
|---------|-----|-----|
| $x$ (m) | -8  | 109 |
| $y$ (m) | 148 | 215 |
| $z$ (m) | 217 | 428 |

There are actually 3 `.stl` files for the terrain topology; they can be merged border-to-border. They correspond to 3 zones of different types of subtratum. The blue zones are vegetated slopes, the gray zones correspond to hard surfaces (vertical rock walls and the horizontal sturdy soil), and the red zones are rocky slopes[...] 


[show photographs and top viewed map with colors, and the framework]

[say how the DTM has been acquired and post-processed]

##### Digital boulders



[say how the digital blocks has been acquired and post-processed]

### Drop positions

For profiles P1 and P2 -> drop positions



### Trajectories

By means of discrete element simulations with the code `Rockable` (see REF),
the four digital boulders have been released from 4 drop positions in each profile P1 and P2. This corresponds to 2$\times$4$\times$4 simulations, but 64 initial orientations, evenly distributed in all possible orientations, where tested for each profile $\times$ drop-position $\times$ boulder-shape. This led to a total of 2048 computed trajetories that are organised according to the following tree structure: `Trajectories/P?/SP??/Drop_position_?/orientation_?.txt`, where the question mark has to be set to select the desired trajectory.


The trajectory datasets are ASCII text files with the following columns:

| Column # | Description                                    |
|:--------:|:-----------------------------------------------|
| 1        | Time from release (s)                          |
| 2        | $x$ position (m)                               |
| 3        | $y$ position (m)                               |
| 4        | $z$ position (m)                               |
| 5        | $x$ velocity (m/s)                             |
| 6        | $y$ velocity (m/s)                             |
| 7        | $z$ velocity (m/s)                             |
| 8        | $s$ scalar component of orientation quaternion |
| 9        | $x$ vector component of orientation quaternion |
| 10       | $y$ vector component of orientation quaternion |
| 11       | $z$ vector component of orientation quaternion |
| 12       | $x$ angular velocity (rad/s)                   |
| 13       | $y$ angular velocity (rad/s)                   |
| 14       | $z$ angular velocity (rad/s)                   |
| 15       | $x$ contact force (N)                          |
| 16       | $y$ contact force (N)                          |
| 17       | $z$ contact force (N)                          |
| 18       | $x$ contact moment (Nm)                        |
| 19       | $y$ contact moment (Nm)                        |
| 20       | $z$ contact moment (Nm)                        |



