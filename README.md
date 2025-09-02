Kinova_DualArm Device Documentation Repository
This repository contains delivery documents for the mobile dual-arm manipulation robot. It aims to facilitate knowledge sharing among team members involved in device debugging and development by providing technical materials, drivers, and usage instructions.
Documentation Structure
The repository covers documentation for core components including robotic arms, chassis, lifting motors, and pitching motors. The structure is as follows:

Robotic Arm: Contains documents related to Kinova-kortex2_Gen3_G3L series, including LICENSE, download links (readme.md), C++ API examples, and configuration files. Covers firmware, API downloads and usage, and compilation instructions for sample code.
Chassis: Provides documentation for the rpp_driver library, including protocol references, SDK introduction, CMakeLists.txt and other configuration files supporting various chassis types (two-wheel differential, four-wheel differential, etc.).
Lifting Motor: Includes driver package structure, technical support information, troubleshooting methods, and configuration/compilation instructions for SDK and ROS2 driver packages.
Pitching Motor: Provides driver package structure, protocol document references, and relevant information/usage methods for SDK and ROS2 driver packages.
Usage Guidelines for Component Documentation
Robotic Arm
Firmware and API Download: Refer to the download links in Kinova-kortex2_Gen3_G3L/readme.md to obtain the corresponding version of firmware, release notes, and API based on the robotic arm type (e.g., Gen3 lite).
C++ Environment Setup: Consider using a Docker environment as detailed in api_cpp/examples/readme.md.
Sample Code Compilation: Follow the instructions in api_cpp/examples/CMakeLists.txt for compilation on different operating systems (Linux, Windows).
Chassis
Protocol Reference: The protocol document is available at Yuque Documentation.
SDK Introduction: rpp_driver is a new protocol C++ driver library for universal chassis, supporting multiple chassis types. Refer to sdk使用说明.md and rpp_driver/README.md.
Lifting Motor
Driver Package Structure: Contains basic SDK package (motor_lift_sdk) and ROS2 driver package (motor_lift_ros). See 升降电机/README.md for directory structure.
Compilation and Execution:
SDK Compilation: Navigate to the motor_lift_sdk directory and execute:
mkdir build && cd build
cmake ..
make
./rpp_keyboard_teleoperate  # Run keyboard control example
ROS2 Driver Package: Compile according to motor_lift_ros/CMakeLists.txt. Configuration files can be found in config/config.yaml.
Troubleshooting: For device recognition, communication failures, etc., refer to common issues and solutions in 升降电机/README.md.
Pitching Motor
Driver Package Structure: Contains basic SDK package (motor_pitch_sdk) and ROS2 driver package (motor_pitch_ros). See 俯仰电机/README.md for directory structure.
Protocol and Usage: Refer to 俯仰电机协议.xlsx for protocol description. See README.md in corresponding directories for specific usage methods.
Compilation and Execution: Navigate to the motor_pitch_sdk directory and execute:
mkdir build
cd build/
cmake ..
make
./rpp_keyboard_teleoperate
License Information
The robotic arm-related parts are subject to the licenses of Kinova inc. and Google Inc., 详见 Kinova-kortex2_Gen3_G3L/LICENSE.
The third-party library cxxopts is subject to the MIT license, 详见 api_cpp/examples/thirdParty/cxxopts/LICENSE.
For license information of other parts, please refer to the documentation in their respective directories.
Technical Support
For detailed technical parameters, maintenance instructions, and usage methods of each component, please refer to the manuals, protocol documents, and README.md files in the corresponding directories:

Lifting Motor: 升降电机手册.pdf and README.md in each package
Pitching Motor: 俯仰电机协议.xlsx and README.md in each package
Chassis: Protocol documents and rpp_driver related documentation
Robotic Arm: API documentation and sample code instructions

For additional questions, please contact the maintenance personnel for each component.
