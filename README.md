Kinova_DualArm 设备文档库
该仓库包含移动双臂操作机器人的交付文档，旨在方便团队成员共享设备相关的技术资料、驱动程序及使用说明，助力设备调试与开发工作。
文档结构说明
仓库主要涵盖机械臂、底盘、升降电机、俯仰电机等核心部件的相关文档，具体结构如下：

机械臂：包含 Kinova-kortex2_Gen3_G3L 系列相关文档，如许可证（LICENSE）、下载链接（readme.md）、C++ API 示例及配置文件等，涉及固件、API 的下载与使用，以及示例代码的编译构建说明。
底盘：提供 rpp_driver 驱动库的说明文档，包括协议参考、SDK 简介、CMakeLists.txt 等配置文件，支持多种类型底盘（两轮差速、四轮差速等）。
升降电机：包含驱动包的目录结构、技术支持信息、故障排除方法、SDK 及 ROS2 驱动包的配置与编译说明等。
俯仰电机：提供驱动包的目录结构、协议文档参考、SDK 及 ROS2 驱动包的相关信息与使用方法。
各部件文档使用指引
机械臂
固件与 API 下载：参考 Kinova-kortex2_Gen3_G3L/readme.md 中的下载链接，根据机械臂类型（如 Gen3 lite）获取对应版本的固件、发布说明及 API。
C++ 环境搭建：可考虑使用 Docker 环境，详情参考 api_cpp/examples/readme.md。
示例代码编译：按照 api_cpp/examples/CMakeLists.txt 中的说明，根据不同操作系统（Linux、Windows）进行编译构建。
底盘
协议参考：协议文档详见 语雀文档。
SDK 简介：rpp_driver 是通用底盘的新版协议 C++ 驱动库，支持多种底盘类型，参考 sdk使用说明.md 和 rpp_driver/README.md。
升降电机
驱动包结构：包含基础 SDK 包（motor_lift_sdk）和 ROS2 驱动包（motor_lift_ros），目录结构详见 升降电机/README.md。
编译与运行：
SDK 编译：进入 motor_lift_sdk 目录，执行如下命令
bash
mkdir build && cd build
cmake ..
make
./rpp_keyboard_teleoperate  # 运行键盘控制示例

ROS2 驱动包：参考 motor_lift_ros/CMakeLists.txt 进行编译，配置文件可查看 config/config.yaml。
故障排除：遇到设备识别、通信失败等问题，参考 升降电机/README.md 中的常见问题及解决方法。
俯仰电机
驱动包结构：包含基础 SDK 包（motor_pitch_sdk）和 ROS2 驱动包（motor_pitch_ros），目录结构详见 俯仰电机/README.md。
协议与使用：协议说明参考 俯仰电机协议.xlsx，各包的具体使用方法见对应目录下的 README.md。
编译运行：进入 motor_pitch_sdk 目录，执行如下命令
bash
mkdir build
cd build/
cmake ..
make
./rpp_keyboard_teleoperate

许可证说明
机械臂相关部分遵循 Kinova inc. 及 Google Inc. 的许可证，详见 Kinova-kortex2_Gen3_G3L/LICENSE。
第三方库 cxxopts 遵循 MIT 许可证，详见 api_cpp/examples/thirdParty/cxxopts/LICENSE。
其他部分许可证信息请参考各对应目录下的说明文件。
技术支持
各部件详细技术参数、维护说明及使用方法，请参考对应目录下的手册、协议文档及 README.md 文件：

升降电机：升降电机手册.pdf 及各包的 README.md
俯仰电机：俯仰电机协议.xlsx 及各包的 README.md
底盘：协议文档及 rpp_driver 相关说明文档
机械臂：API 文档及示例代码说明

如有其他问题，可联系各部件维护人员。
