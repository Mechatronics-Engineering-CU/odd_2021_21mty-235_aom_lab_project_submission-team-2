# <p align="center"> UAV Trajectory Controller </p>

## Team members:
**1. [Ankit Chaudhary](https://github.com/chaudhary-ankit)**   
**2. [Kartikay](https://github.com/Chiranjeev-Kartik)**   
**3. [Om Jagga](https://github.com/Ommmmmm05)**   
**4. [Ajit Singh](https://github.com/ajitsohal)**   
**5. [Sanket Sharma](https://github.com/snktshrma)**

## Documentation:
### [Documentation and Report](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/Autopilot_Research_Report.pdf)

## Overview:
As drones are growing rapidly in popularity, their use in multiple section is increasing exponentially. Over the past few years, drones have become central to the functions of various businesses and governmental organizations and have managed to pierce through areas where certain industries were either stagnant or lagging behind. From quick deliveries at rush hour to scanning an unreachable military base, drones are proving to be extremely beneficial in places where man cannot reach or is unable to perform in a timely and efficient manner.

Drone is not just a body with a battery with propellers; it works in a much complex way as it seem to be. There are many intrinsic and extrinsic factors affecting the flight of drone.

Applying and modeling full dynamics of drone is not a new idea and is not the focus of paper. Instead, contribution of this paper is a novel way to understand the core and basic dynamics of a quadrotor drone while replicating a defined trajectory in YZ plane. This way has enabled us to understand the very basic and important extrinsic and intrinsic factor affecting the drone flight.

# Getting Started

## Requirements:
- MATLAB
- Simulink
- Control System Toolbox
- Simulink Control Design

## Setup and run:
1. Clone the simulink file attached below.
2. Open the downloaded `.slx` file in simulink and run.
3. Click of the scopes added to the model to visualize the trajectory with respect to time.

## Models:

### Plant model:
Our system combine two approaches, plant and feedback model, to design trajectory and control model of a quadrotor 
UAV. This combined approach will help the model design to be much efficient. 
In our plant model approach, mathematical model for dynamics of drone with respect to Z and Y plane are constructed. This is done to find the dynamics displacement of drone in Z and Y axis in a particular time interval by double integrating the required equations of motion. Further in construction of model, it is linearized around hover point.

![Plant Model](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/Plant.png?raw=true)

### Feedback model:
The open-loop configuration is not efficient to change the thrust, moment and roll angle of the quadrotor depending upon the error between desired co-ordinate and actual rotor position. Hence a PID feedback system is  employed in quadrotor control system.

![Feedback Model](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/Model.png?raw=true)

## Demonstration Video:
[![Youtube video](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/yt.png?raw=true)](https://youtu.be/ZMkLm3y0A9g)

## Link to Simulink file: 
[UAV_trajectory_and_control_model.slx](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/UAV_trajectory_and_control_model.slx)

## Output graphs:

### Y graph:
![Y graph](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/Y.png?raw=true)

### Z graph:
![Z graph](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/Z.png?raw=true)

### Phi graph:
![Phi graph](https://github.com/Mechatronics-Engineering-CU/odd_2021_21mty-235_aom_lab_project_submission-team-2/blob/main/TEAM-2/images/Phi.png?raw=true)

# Conclusion:
In this project, we presented and experimentally tested a trajectory and control system designed a quadrotor UAV that uses a mathematical model at the core to replicate a quadrotor controller. 

At the core we created a plant model in Simulink that models that dynamics of the drone in YZ plane, using two equations of motions. The model inputs the thrust from the rotor and the moment to output dynamics displacement of drone in YZ plane. The trajectory to be followed by the drone in input to the plant using a feedback system. Error (difference of trajectory input Y and Z and the output of the  plant Y, Z  and  Φ) is fed back to the plant model as inputs. 

We demonstrated a basic control and trajectory model for a quadrotor UAV. 
