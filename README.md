# ros2_camera_calibration
ros2的相机标定工具

参考文档https://blog.csdn.net/qq_64079631/article/details/136423941

1.安装工具
```
  sudo apt install ros-humble-camera-calibration-parsers
```
```
  sudo apt install ros-humble-camera-info-manager
```
```
  sudo apt install ros-humble-launch-testing-ament-cmake
```
2.clone该仓库，解压压缩包

3.打开camera/src/image_pipeline

4.在该目录下打开终端colcon build

5.运行相机节点

6.运行标定工具
```
  ros2 run camera_calibration cameracalibrator --size 6x5 --square 0.024 image:=/image_raw  camera:=/camera --no-service-check
```

  参数：
  
  --size表示棋盘格角点数量，如8x9个格子的棋盘格，角点个数为7x8个，size参数就要写7x8  
  
  --square表示 棋盘格一个小格子的宽度（注意单位为m）

  image:=表示：图像话题名称为/image_raw 相机标定节点将从该话题接收图像进行标定
  
  camera:=表示：指定相机名称/camera

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/qq_64079631/article/details/136423941
