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
![Screenshot 2024-11-17 181205](https://github.com/user-attachments/assets/f9b48cc5-dc86-444c-a3ff-e564fb756e91).                          ![image](https://github.com/user-attachments/assets/cbb55ba6-a79a-42be-9035-566020d99213)



# STSMC Control For Trajectory Tracking Of a Multi-Quadrotor System
![image](https://github.com/user-attachments/assets/09326d93-a5f5-4958-ac4e-e4d54776608a)  ![image](https://github.com/user-attachments/assets/edfcf260-c43f-4aed-85ae-7987717f2cb0)



