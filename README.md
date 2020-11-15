# Gazebo Panda

A standard bare-bone ROS Gazebo simulator for the Franka Emika Panda robot built using inbuilt Gazebo ROS controllers and RobotHW interfaces. Robot controllable using standard ROS control interfaces. No dependencies on franka_ros or libfranka.

## Dependencies

- [franka_panda_description](https://github.com/justagist/franka_panda_description)

## Interface Details

- Hardware interface: hardware_interface/EffortJointInterface
- Transmission interface: transmission_interface/SimpleTransmission
- Controllers:
  - gazebo_panda/effort_joint_position_controller: effort_controllers/JointGroupPositionController
  - gazebo_panda/effort_joint_torque_controller: effort_controllers/JointGroupEffortController
  - gazebo_panda/panda_gripper_controller: effort_controllers/JointGroupPositionController
