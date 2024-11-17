# Distributed Tracking Protocol for Multi-Quadrotors with Super-Twisting Sliding Mode Control (STSMC)
This project focuses on designing and implementing a distributed tracking protocol for quadrotors to achieve efficient formation control and obstacle avoidance in three-dimensional space. The proposed control system uses a Super-Twisting Sliding Mode Controller (STSMC) with a PID sliding surface for each quadrotor subsystem, ensuring accurate tracking of reference commands even in the presence of external disturbances. The goal is to achieve rapid formation of both fixed and dynamic configurations using consensus theory, while enabling the system to recover the desired formation promptly after obstacle avoidance.

The key objectives of this research include:

1. Formation Control

   Ensuring stable and efficient formation of multiple quadrotors, even in dynamic environments. This involves achieving consensus between quadrotors, both in fixed and 
   dynamic configurations, to ensure coordinated movement.

2. Obstacle Avoidance

   Implementing an artificial potential field-based strategy that allows the quadrotors to navigate safely around static and dynamic obstacles, ensuring they maintain a safe 
   minimum distance from each other and obstacles during maneuvering.

4. PID Tuning for STSMC

   Carefully tuning the PID sliding surface parameters to minimize steady-state errors and ensure convergence of the error trajectory, improving system performance and 
   robustness against external disturbances.

The research addresses the challenges of precise formation control and robust obstacle avoidance in multi-quadrotor systems. The use of STSMC guarantees that the system remains resilient to external disturbances, while the artificial potential field-based strategy ensures safe navigation in complex environments.

# STSMC Control For Position Control And Trajectory Tracking Of A Single Quadrotor
![Screenshot 2024-11-17 181205](https://github.com/user-attachments/assets/f9b48cc5-dc86-444c-a3ff-e564fb756e91). ![image](https://github.com/user-attachments/assets/cbb55ba6-a79a-42be-9035-566020d99213)

The above proposed stsmc controller was developed into a ROS-node in order to autonomously control a single drone to hover at an altitude of 15m thereby establishing a position control.Later on the drone was made to draw out various trajectories based on the inputs given by the user and then land again. Fig shows the drone's trajectory using the Q-ground-Control ground control station. The simulator also utilizes a wind generator plugin that is capable of simulating various wind profiles (both constant and stochastic) for speed and direction.



# STSMC Control For Trajectory Tracking Of a Multi-Quadrotor System
![image](https://github.com/user-attachments/assets/09326d93-a5f5-4958-ac4e-e4d54776608a)  ![image](https://github.com/user-attachments/assets/edfcf260-c43f-4aed-85ae-7987717f2cb0)

For the multi-quad rotor system a stsmc controller was made for each of the quadrotors to enable both trajectory tracking as well as for formation control using the consensus theory. The controller first calculates the actuator commands to be given to the individual drones and then later on calculates the setpoints between each drones based on the information received by each one of them through their odometry and publishes commands to maintain formation. The controller was first tested for the position control of three drones.Then later on for the application of trajectory tracking in multi-quadrotor systems essentially a leader follower approach has been adopted to enable a formation to trace out a given trajectory. Only the leader drone was supplied with the necessary coordinates and trajectory using a function. The follower drones essentially have to bring down the consensus error to zero which will enforce the formation and in turn make all the three drones to trace out a desired trajectory. In this scenario as well, a circular trajectory was supplied to the leader drone. The stsmc controller in the leader drone in this case was taking care of trajectory tracking while the stsmc controllers in the follower drones where essentially trying to bring the setpoints i.e the consensus error to zero to enforce the formation

