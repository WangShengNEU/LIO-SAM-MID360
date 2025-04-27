# LIO-SAM-MID360

本代码为LIO-SAM适配Livox MID360版本。
支持使用六轴和九轴IMU。

## Dependency

- 与LIO-SAM有相同依赖 ( [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM/) ）
- 请安装LIVOX ROS包用于发布点云数据 ( [览沃 ROS 驱动程序](https://github.com/Livox-SDK/livox_ros_driver/) )

如果使用Livox-ros-driver2 驱动可以切换分支为 [Livox-ros-driver2](https://github.com/nkymzsy/LIO-SAM-MID360/tree/Livox-ros-driver2) 。

## Prepare lidar data

Livox MID360雷达数据请使用览沃自定义点云数据`CustomMsg`，即LIVOX ROS驱动请运行`livox_lidar_msg.launch`。

## Run

使用自带的6轴IMU请运行

```
roslaunch lio_sam run6axis.launch
```

使用9轴IMU请运行

```
roslaunch lio_sam run9axis.launch
```
## Acknowledgement

- [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM/)
- [LIO-SAM-DetailedNote](https://github.com/smilefacehh/LIO-SAM-DetailedNote)
- [LIO_SAM_6AXIS](https://github.com/JokerJohn/LIO_SAM_6AXIS)

# 保存地图： rosservice call [service] [resolution] [destination]
# source devel/setup.bash
rosservice call /lio_sam/save_map 0.2 "work/LIO-SAM/save_pcd/"


