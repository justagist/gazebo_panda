# Gazebo Panda

A standard bare-bone ROS Gazebo simulator for the Franka Emika Panda robot built using inbuilt Gazebo ROS controllers and RobotHW interfaces. Robot controllable using standard ROS control interfaces. No dependencies on franka_ros or libfranka.

**NOTE: This package by default does not depend on franka_ros or libfranka, however using it with [this plugin](https://github.com/smihael/panda_sim_hw) (thanks to [@smihael](https://github.com/smihael)!) allows using similar interfaces as the real robot. This allows using the Gazebo simulator for running the controller examples in franka_ros, and writing other controller codes using the same interfaces as the real robot.**

**NOTE: For a more complex simulator allowing transfer of code from sim-to-real, see [PandaSimulator](https://github.com/justagist/panda_simulator).**

## Dependencies

- [franka_panda_description](https://github.com/justagist/franka_panda_description)

## Interface Details

- Hardware interface: hardware_interface/EffortJointInterface
- Transmission interface: transmission_interface/SimpleTransmission
- Controllers:
  - gazebo_panda/effort_joint_position_controller: effort_controllers/JointGroupPositionController
  - gazebo_panda/effort_joint_torque_controller: effort_controllers/JointGroupEffortController
  - gazebo_panda/panda_gripper_controller: effort_controllers/JointGroupPositionController
