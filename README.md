# pmb2_robot

The `pmb2_robot` repository provides launch files and configuration files for the PMB2 robot. It includes tools for bringing up the robot's sensors, teleoperation, and configuration for various components.

## Table of Contents

- [Nodes/Scripts](#nodesscripts)
- [Params - Config](#params-config)
- [Library/Module Overview](#librarymodule-overview)
- [Launch Files](#launch-files)
- [Example Usage](#example-usage)
- [Dependencies](#dependencies)

---

## Nodes/Scripts

This repository does not include standalone ROS nodes or scripts but focuses on configuration and launch files necessary for bringing up and controlling the PMB2 robot.

---

## Params - Config

The `pmb2_bringup` package includes several YAML configuration files for various components:

- **Config Files**:
  - **sensor_to_cloud**:
    - `bumper_to_cloud.yaml`: Configuration for converting bumper sensor data to point cloud.
    - `sonar_to_cloud.yaml`: Configuration for converting sonar sensor data to point cloud.

  - **twist_mux**:
    - `joystick.yaml`: Configuration for joystick input.
    - `twist_mux_locks.yaml`: Configuration for locking mechanisms in twist mux.
    - `twist_mux_topics.yaml`: Configuration for twist mux topics.

  - `joy_teleop.yaml`: Configuration for joystick teleoperation.
  - `pmb2_hardware.yaml`: Configuration for the PMB2 robot's hardware.

These files define parameters and configurations for sensors, hardware interfaces, and teleoperation setups.

---

## Library/Module Overview

The `pmb2_bringup` package does not include any C++ libraries or modules. Instead, it focuses on providing configuration and launch files necessary for deploying and controlling the PMB2 robot.

---

## Launch Files

The repository includes several launch files to bring up different aspects of the PMB2 robot:

- **`joystick_teleop.launch`**: Launches the joystick teleoperation system.
- **`pmb2.launch`**: General launch file for bringing up the PMB2 robot.
- **`pmb2_bringup.launch`**: Main launch file for initializing the PMB2 robot's bringup sequence.
- **`twist_mux.launch`**: Launches the twist multiplexer for handling multiple input sources.

These launch files integrate various configurations and nodes for operating the PMB2 robot.

---

## Example Usage

To bring up the PMB2 robot with all configurations and launch files, you can use the following command:

```bash
roslaunch pmb2_bringup pmb2_bringup.launch
```

For joystick teleoperation, use:

```bash
roslaunch pmb2_bringup joystick_teleop.launch
```

These commands will start the robot with the appropriate configurations and setups as defined in the respective launch files.

---

## Dependencies

The `pmb2_bringup` package depends on the following:

- **ROS**: This package requires a working ROS environment.
- **Catkin**: Required for building and installing the package.

For detailed information on ROS and Catkin, refer to the [ROS Wiki](https://wiki.ros.org/).
