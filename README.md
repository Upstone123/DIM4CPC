# Distributed Inference on Manifolds for Cooperative Planning and Control of Multiple Underactuated Autonomous Surface Vehicles

This repository presents simulation figures and animations for cooperative trajectory planning and control of underactuated autonomous surface vehicles (ASVs). The proposed method combines local error dynamics on the vehicle state manifolds with inter-ASV distance factors. Expectation propagation provides Gaussian separation messages, which are incorporated into the trajectory and control update for each vehicle.

## Case 1: Six-ASV crossing

Six ASVs travel to distinct destinations in a workspace containing circular and polygonal obstacles. The animations show the executed paths of the proposed method.

![Six-ASV crossing animation](Figure_2.gif)

| Paper figure             | Content                                                   |
| ------------------------ | --------------------------------------------------------- |
| [Figure 2](Figure_2.png) | Executed trajectories and ASV positions at selected times |
| [Figure 3](Figure_3.png) | Surge and sway velocities and yaw rates                   |
| [Figure 4](Figure_4.png) | Applied surge forces and yaw moments                      |

## Case 2: Twelve-ASV position swap

Twelve ASVs exchange start and goal positions in six opposite pairs. The animation compares **online DMPC** (left), adapted from [Luis et al. (2020)](https://doi.org/10.1109/LRA.2020.2964159), with the **proposed method** (right) under the same initial references and disturbance realization.

![Twelve-ASV position-swap comparison](Figure_5.gif)

The following plots show the minimum distance at each time across all ASV pairs and across all ASV–obstacle combinations, respectively.

![Figure 6(a): Minimum inter-ASV distance](Figure_6a.png)

![Figure 6(b): Minimum static-obstacle distance](Figure_6b.png)

### Supplementary trajectories and control results

| Method          | Body-frame velocity and yaw rate                           | Control inputs                                                    |
| --------------- | ---------------------------------------------------------- | ----------------------------------------------------------------- |
| Online DMPC     | [Velocity profiles](12_ASV_Online_DMPC_Velocities.png)     | [Surge force and yaw moment](12_ASV_Online_DMPC_Controls.png)     |
| Proposed method | [Velocity profiles](12_ASV_Proposed_method_Velocities.png) | [Surge force and yaw moment](12_ASV_Proposed_method_Controls.png) |

## Code availability

The simulation code will be released as open source in this repository.
