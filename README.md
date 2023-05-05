# FDI_IMU_ROS

ROS SDK for FDIsystems IMU

## 安装 ROS2 的串口软件包

下载 serial 软件包

```bash
git clone git@github.com:ZhaoXiangBox/serial.git
```

切换目录

```bash
cd serial
mkdir build
cd build
```

编译

```bash
cmake ..
make
```

安装

```bash
sudo make install
```

## 编译 IMU ROS2 SDK

编译

```bash
colcon build --packages-select fdilink_ahrs
```

启动 IMU 节点

```bash
source install/setup.bash
ros2 launch fdilink_ahrs ahrs_driver.launch.py
```

## 设置串口节点

```bash
sudo ./wheeltec_udev.sh
```
