# Awesome-Autonomous-Driving [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

Author: 牛肉咖喱饭(PeterJaq)

Update：2022/06/26

This project will be periodically updated with quality projects and papers related to autonomous driving.

Now I am re-orging this project.

## Contents
- [Contents](#contents)
- [1. Autonomous Driving Midleware and Integrated Solutions(中间件与解决方案)](#1-autonomous-driving-midleware-and-integrated-solutions)
  - [1.1 Midelware(中间件)](#11-midelware)
  - [1.2 Integrated Solutions(解决方案)](#12-integrated-solutions)
- [2. Sensor and Calibration Tools(传感器与参数标定)](#2-sensor-and-calibration-tools)
  - [2.1 Sensor Hardware(传感器硬件)](#21-sensor-hardware)
  - [2.2 Calibration Tools(参数标定工具)](#22-calibration-tools)
- [3. Perception](#3-perception)
  - [3.1 Detection](#31-detection)
    - [3.1.1 Vision based](#311-vision-based)
    - [3.1.2 Lidar based](#312-lidar-based)
    - [3.1.3 Radar based](#313-radar-based)
    - [3.1.4 Multimodal Fusion](#314-multimodal-fusion)
  - [3.2 Tracking](#32-tracking)
- [4. Prediction](#4-prediction)
- [5. Localization and SLAM(定位与SLAM)](#5-localization-and-slam)
- [6. Planning](#6-planning)
- [7. Control](#7-control)
- [8. Dataset and Competition(数据集与竞赛)](#8-Dataset-and-Competition)
- [9. Visualization(可视化工具)](#9-Visualization)
- [10. Data Loop(数据闭环)](#10-Data-Loop)
- [11. Simulation(仿真)](#11-Simulation)
- [12. Others(其他更好的)](#12-Others)

## 1. Autonomous Driving Midleware and Integrated Solutions

### 1.1 Midelware
*中间件*
- [ROS](https://github.com/ros) - A set of software libraries and tools that help you build robot applications. 
- [ROS-2](https://github.com/ros2) - A set of software libraries and tools that help you build robot applications. 
- [Cyber](https://github.com/storypku/CyberRT) - High performance runtime framework designed specifically for autonomous driving (AD) scenarios from [baidu](www.baidu.com).
### 1.2 Integrated Solutions
*解决方案*

- [Apollo](https://github.com/ApolloAuto/apollo) - The intergrated solution from [baidu](www.baidu.com).
- [Autoware.ai](https://github.com/Autoware-AI/) - Open-source software for self-driving vehicles known as Autoware-1.
- [Autoware.auto](https://gitlab.com/autowarefoundation/autoware.auto) - Open-source software for self-driving vehicles known as Autoware-2.
- [AutowareArchitectureProposal.proj](https://github.com/tier4/AutowareArchitectureProposal.proj) - Manages several projects related to self-driving vehicles. 
- [self-driving-ish_computer_vision_system](https://github.com/iwatake2222/self-driving-ish_computer_vision_system) - This project generates images you've probably seen in autonomous driving demo.
- [Aslan](https://github.com/project-aslan/Aslan) - An open-source full-stack software based on ROS framework.
- [AutoC2X-AW](https://github.com/esakilab/AutoC2X-AW) - Extension for Autoware and OpenC2X.

## 2. Sensor and Calibration Tools
### 2.1 Sensor Hardware
*传感器硬件*

  **LiDAR** 
  
  - [velodyne](https://github.com/ros-drivers/velodyne) - velodyne lidar driver for ros.
  - [livox_ros_driver](https://github.com/Livox-SDK/livox_ros_driver) - livox (a low cost lidar form [DJI](https://www.dji.com/cn)) lidar driver.
  - [rslidar_sdk](https://github.com/RoboSense-LiDAR/rslidar_sdk) - lidar driver from [Robosense](https://www.robosense.ai).
  - [ros2_ouster_drivers](https://github.com/ros-drivers/ros2_ouster_drivers) - ROS2 Drivers for the [Ouster](https://www.ouster.com) OS-0, OS-1, and OS-2 Lidars. 

 **Camera** 
 
  - [miivii_gmsl_camera](https://github.com/MiiViiDynamics/miivii_gmsl_camera) - [米文](https://www.miivii.com/)摄像头
  - [sensing](https://www.sensing-world.com/) - [森云](https://www.sensing-world.com/) - 森云摄像头
  - [Hikvision](https://www.hikvision.com) - You can download [SDK](https://www.hikvision.com/en/support/download/sdk/).
  - [usb_cam](https://github.com/ros-drivers/usb_cam) - all most ros1 usb camera driver you can buy from Taobao/Aliexpress.
  - [ros2_usb_camera](https://github.com/klintan/ros2_usb_camera) - all most ros2 usb camera driver you can buy from Taobao/Aliexpress.

 **GPS/IMU** 
 
  - [huace](https://www.huace.cn) - 华测组合导航产品
  - [novatel_gps_driver](https://github.com/swri-robotics/novatel_gps_driver) - C++ ROS driver for NovAtel GPS / GNSS Receivers.
 
 **MCU**
 
  - [STM32Cube_MCU_Overall_Offer](https://github.com/STMicroelectronics/STM32Cube_MCU_Overall_Offer) - The open source offer for the STM32 MCU products.


### 2.2 Calibration Tools
*参数标定工具*

- [OpenCalib](https://github.com/PJLab-ADG/SensorsCalibration) - 
**ALL in One** 商汤开源的自动驾驶多传感器的一个开源标定工具箱，基本涵盖了大部分的自动驾驶标定场景。
- [camera-calibration](https://github.com/LittleAprilFool/camera-calibration) -
能够比较好的阐述相机标定具体步骤和原理的
- [CameraCalibration](https://github.com/dyfcalid/CameraCalibration) - 
这个项目集合了相机标定相关的多个脚本工具，便于完成完整的车载环视相机标定流程
- [ros-camera-lidar-calibration](https://github.com/swyphcosmo/ros-camera-lidar-calibration) -
相机内参标定与相机lidar外参标定
- [lidar_IMU_calib](https://github.com/APRIL-ZJU/lidar_IMU_calib) -
Lidar IMU 的标定工具
- [sync_gps_lidar_imu_cam](https://github.com/nkliuhui/sync_gps_lidar_imu_cam) -
lidar-imu-cam-GPS时间戳硬件同步方案

## 3. Perception
### 3.1 Detection

*检测与分割*

### 3.1.1 Vision based
*基于视觉*

  **Lane Detection**
   
  - [Advanced-Lane-Detection](https://github.com/uranus4ever/Advanced-Lane-Detection) - 一个非常适合新人的车道检测任务的小demo
  - [RESA](https://github.com/ZJULearning/resa)
  - [LaneDet](https://github.com/Turoad/lanedet)
  - [CondLaneNet](https://github.com/aliyun/conditional-lane-detection)
  - [Focus on Local: Detecting Lane Marker from Bottom Up via Key Point](https://openaccess.thecvf.com/content/CVPR2021/papers/Qu_Focus_on_Local_Detecting_Lane_Marker_From_Bottom_Up_via_CVPR_2021_paper.pdf)
  - [LaneNet-Lane-Detection](https://github.com/MaybeShewill-CV/lanenet-lane-detection)
  - [urban_road_filter](https://github.com/jkk-research/urban_road_filter) 一种实时的道路边缘检测分割工具
  - [Cam2BEV](https://github.com/ika-rwth-aachen/Cam2BEV) - Cam2BEV一个将多路周视摄像头的语义分割结果融合在一个鸟瞰图的工具，并且该方法不需要手工对鸟瞰图进行标注通过合成的数据进行训练。
  - [YOLOP](https://github.com/hustvl/YOLOP) - 来自华中科技大学的作品，也是yolo系列的另一力作，本项目提出额一种高效的多任务网络，可以联合处理自动驾驶中的多个任务（目标检测，可行驶区域分割与车道检测三个关键任务），值得注意的是在BDD100K中该方法实现了SOTA的情况下还保持了嵌入式友好。
 
  **Object Detection**
  
  - [YOLOR](https://github.com/WongKinYiu/yolor) - 提出了在网络模型中引入隐知识的概念，将隐知识和显知识同时作用于模型训练，通过核函数对齐，预测精修以及多任务同时学习，让网络表征出一种统一化的特征。
  - [YOLOX](https://github.com/Megvii-BaseDetection/YOLOX) - Anchor-free 版本的YOLO，堆砌了解耦头，simOTA等，达到了SOTA
  - [3D-BoundingBox](https://github.com/skhadem/3D-BoundingBox)
  - [Pseudo_Lidar_V2](https://github.com/mileyan/Pseudo_Lidar_V2) - Accurate Depth for 3D Object Detection in Autonomous Driving.
  - [Pseudo_lidar](https://github.com/mileyan/pseudo_lidar.git) - Pseudo-LiDAR from Visual Depth Estimation: Bridging the Gap in 3D Object Detection for Autonomous Driving.

### 3.1.2 Lidar based

*基于激光雷达*

  **Object Detection**
  
  - [Voxelnet](https://github.com/steph1793/Voxelnet)
  - [Complex-YOLO](https://github.com/maudzung/Complex-YOLOv4-Pytorch)
  - [PointRCNN](https://github.com/sshaoshuai/PointRCNN) 
  - [CenterPoint](https://github.com/tianweiy/CenterPoint) - 3D Object Detection and Tracking using center points in the bird-eye view.
  - [PartA2-Net](https://github.com/sshaoshuai/PartA2-Net) - From Points to Parts: 3D Object Detection from Point Cloud with Part-aware and Part-aggregation Network.
  - [CIA-SSD](https://github.com/Vegeta2020/CIA-SSD) - Confident IoU-Aware Single Stage Object Detector From Point Cloud.
  - [3DIoUMatch-PVRCNN](https://github.com/THU17cyz/3DIoUMatch-PVRCNN) - 3DIoUMatch: Leveraging IoU Prediction for Semi-Supervised 3D Object Detection.
  - [SFA3D](https://github.com/maudzung/SFA3D) - Super Fast and Accurate 3D Object Detection based on 3D LiDAR Point Clouds.

### 3.2 Tracking
*追踪算法*
- [SimpleTrack](https://github.com/TuSimple/SimpleTrack) - Simple yet Effective 3D Multi-object Tracking.
- [ImmortalTracker](https://github.com/ImmortalTracker/ImmortalTracker) - Our mismatch ratio is tens of times lower than any previously published method.
- [Yolov5_DeepSort_Pytorch](https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch) - 基于yolo-v5的目标追踪

### 3.3 High Performance Inference
*高性能推理*

**视觉系列**
- [Lite.ai](https://github.com/DefTruth/lite.ai) -
该项目提供了一系列轻量级的目标检测语义分割任务的整合框架支持 YOLOX🔥, YoloR🔥, YoloV5, YoloV4, DeepLabV3, ArcFace, CosFace, RetinaFace, SSD, etc.
- [multi-attention -> onnx](https://github.com/liudaizong/CSMGAN/blob/51348c805e83cf4b1c791592d329851a8e2186aa/code/modules_/multihead_attention.py) -   
提供了一个多头注意力机制支持onnx部署的方式

**LiDAR Pillars系列**

- [CUDA-PointPillars](https://github.com/NVIDIA-AI-IOT/CUDA-PointPillars) - NV官方PointPillars部署方案
- [nutonomy_pointpillars](https://github.com/SmallMunich/nutonomy_pointpillars) - PointPillars
- [mmdet3d_onnx_tools](https://github.com/speshowBUAA/mmdet3d_onnx_tools) - PointPillars
- [CenterPoint](https://github.com/CarkusL/CenterPoint) - CenterPoint-PonintPillars 
- [PointPillars_MultiHead_40FPS](https://github.com/hova88/PointPillars_MultiHead_40FPS) - MultiHead PointPillars
- [我自己的 ROS Lidar Perception TensorRT部署](https://github.com/PeterJaq/lidar_perception)
- [CenterPoint](https://github.com/Abraham423/CenterPoint) - CenterPoint 推理方案 ROS

## 4. Prediction

- [An Auto-tuning Framework for Autonomous Vehicles] (https://arxiv.org/pdf/1808.04913.pdf)
- [VectorNet](https://github.com/Liang-ZX/VectorNet.git) -
来自[VectorNet: Encoding HD Maps and Agent Dynamics from Vectorized Representation](https://arxiv.org/abs/2005.04259)利用高精地图 -与目标物信息进对目标进行行为预测。apollo在7.0版本的行为预测部分的encoder利用了这个vectornet.
- [TNT](https://github.com/Henry1iu/TNT-Trajectory-Predition) - TNT是一种基于历史数据（即多代理和环境之间交互）生成目标的轨迹状态序列方法，并基于似然估计得到紧凑的轨迹预测集。
- [DESIRE](https://github.com/tdavchev/DESIRE) - DESIRE: Distant Future Prediction in Dynamic Scenes with Interacting Agents 
- [TNT: Target-driveN Trajectory Prediction](https://arxiv.org/pdf/2008.08294.pdf) apollo在7.0版本的行为预测模块inter-TNT的轨迹生成利用了TNT的方法.
- [MultiPath++](https://github.com/stepankonev/waymo-motion-prediction-challenge-2022-multipath-plus-plus) - Efficient Information Fusion and Trajectory Aggregation for Behavior Prediction.
- [MotionCNN](https://github.com/kbrodt/waymo-motion-prediction-2021) - A Strong Baseline for Motion Prediction in Autonomous Driving.
- [WAT](https://github.com/wei-mao-2019/wat) - Weakly-supervised Action Transition Learning for Stochastic Human Motion Prediction.
- [BEVerse](https://github.com/zhangyp15/beverse) - Unified Perception and Prediction in Birds-Eye-View for Vision-Centric Autonomous Driving.
- [ParkPredict+](https://github.com/xushenlz/parksim) - Vehicle simualtion and behavior prediction in parking lots.
- [HiVT](https://github.com/ZikangZhou/HiVT) - Hierarchical Vector Transformer for Multi-Agent Motion Prediction


## 5 Localization and SLAM
  *Localization*
  
  - [hdl_localization](https://github.com/koide3/hdl_localization) - **Lidar + IMU** 基于卡尔曼滤波的位置估计使用了激光雷达，IMU, 可以做到实时估计。
  
  *SLAM*
  
- [AVP-SLAM](https://arxiv.org/abs/2007.01813)来自2020IROS的AVP定位方案：AVP-SLAM: Semantic Visual Mapping and Localization for Autonomous Vehicles in the Parking Lot(IROS 2020),主要是通过BEV视角对停车场中的车道线车库线以及标识进行检测并利用其进行稀疏定位。
最近有两位大佬提供了仿真和定位的开源方案：[AVP-SLAM-SIM](https://github.com/TurtleZhong/AVP-SLAM-SIM) [AVP-SLAM-PLUS](https://github.com/liuguitao/AVP-SLAM-PLUS)
- [DeepLIO](https://github.com/ArashJavan/DeepLIO) - **Lidar + IMU** 一款基于深度学习的lidar IMU融合里程计
- [hdl_graph_slam](https://github.com/koide3/hdl_graph_slam) - **Lidar + IMU + GPS** 它基于三维图形SLAM，具有基于NDT扫描匹配的测距估计和循环检测。它还支持几个约束，如GPS、IMU。
- [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM) - **Lidar + IMU + GPS** 基于激光雷达，IMU和GPS多种传感器的因子图优化方案，以及在帧图匹配中使用帧-局部地图取代帧-全局地图。
- [LVI-SAM](https://github.com/TixiaoShan/LVI-SAM) - **Lidar + Camera** 基于视觉+激光雷达的惯导融合
- [LeGO-LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM) - **Lidar** LeGO-LOAM是以LOAM为框架而衍生出来的新的框架。其与LOAM相比，更改了特征点的提取形式，添加了后端优化，因此，构建出来的地图就更加的完善。
- [SC-LeGO-LOAM](https://github.com/irapkaist/SC-LeGO-LOAM) - **Lidar** LeGO-LOAM的基于全局描述子Scan Context的回环检测
- [SC-LIO-SAM](https://github.com/gisbi-kim/SC-LIO-SAM) - **Lidar + Camera** LIO-SAM的基于全局描述子Scan Context的回环检测
- [Livox-Mapping](https://github.com/PJLab-ADG/Livox-Mapping) - **Livox + IMU + SC  ** 一款基于Livox的mapping工具包，在先前的工具上添加了SC和Fastlio的一些特性 
- [Fast-LIO](https://github.com/hku-mars/FAST_LIO) - 目前最好用的前端里程计之一，几乎同时兼具速度与鲁棒性
- [Faster-LIO](https://github.com/gaoxiang12/faster-lio) - 比Fast LIO快1-1.5倍的前端里程计
- [SC-A-LOAM](https://github.com/gisbi-kim/SC-A-LOAM) - Scancontext + 现在的SOTA里程计(Lego-loam, fast lio, a loam etc.)
- 
## 6. Planning
*规划*
- [自动驾驶中的决策规划算法概述](https://www.jiqizhixin.com/articles/2019-07-22)
- [有限状态机](https://en.wikipedia.org/wiki/Finite-state_machine)
- [MPC](https://en.wikipedia.org/wiki/Model_predictive_control)
- [PathPlanning](https://github.com/zhm-real/PathPlanningt)
- [pacmod](https://github.com/astuff/pacmod) -  Designed to allow the user to control a vehicle with the PACMod drive-by-wire system.
- [rrt](https://github.com/RoboJackets/rrt) - C++ RRT (Rapidly-exploring Random Tree) implementation.
- [HypridAStarTrailer](https://github.com/AtsushiSakai/HybridAStarTrailer) - A path planning algorithm based on Hybrid A* for trailer truck.
- [path_planner](https://github.com/karlkurzer/path_planner) - Hybrid A* Path Planner for the KTH Research Concept Vehicle.
- [fastrack](https://github.com/HJReachability/fastrack) - A ROS implementation of Fast and Safe Tracking (FaSTrack).
- [commonroad](https://commonroad.in.tum.de/) - Composable benchmarks for motion planning on roads.
- [traffic-editor](https://github.com/osrf/traffic-editor) - A graphical editor for robot traffic flows.
- [steering_functions](https://github.com/hbanzhaf/steering_functions) - Contains a C++ library that implements steering functions for car-like robots with limited turning radius.
- [moveit](https://moveit.ros.org/) - Easy-to-use robotics manipulation platform for developing applications, evaluating designs, and building integrated products.
- [flexible-collision-library](https://github.com/flexible-collision-library/fcl) - A library for performing three types of proximity queries on a pair of geometric models composed of triangles.
- [aikido](https://github.com/personalrobotics/aikido) - Artificial Intelligence for Kinematics, Dynamics, and Optimization.
- [casADi](https://github.com/casadi/casadi) - A symbolic framework for numeric optimization implementing automatic differentiation in forward and reverse modes on sparse matrix-valued computational graphs.
- [ACADO Toolkit](https://github.com/acado/acado) - A software environment and algorithm collection for automatic control and dynamic optimization.
- [CrowdNav](https://github.com/vita-epfl/CrowdNav) - Crowd-aware Robot Navigation with Attention-based Deep Reinforcement Learning.
- [ompl](https://github.com/ompl/ompl) - Consists of many state-of-the-art sampling-based motion planning algorithms.
- [openrave](https://github.com/rdiankov/openrave) - Open Robotics Automation Virtual Environment: An environment for testing, developing, and deploying robotics motion planning algorithms.
- [teb_local_planner](https://github.com/rst-tu-dortmund/teb_local_planner) - An optimal trajectory planner considering distinctive topologies for mobile robots based on Timed-Elastic-Bands.
- [pinocchio](https://github.com/stack-of-tasks/pinocchio) - A fast and flexible implementation of Rigid Body Dynamics algorithms and their analytical derivatives.
- [rmf_core](https://github.com/osrf/rmf_core) - The rmf_core packages provide the centralized functions of the Robotics Middleware Framework (RMF).
- [global_racetrajectory_optimization](https://github.com/TUMFTM/global_racetrajectory_optimization) - This repository contains multiple approaches for generating global racetrajectories.
- [toppra](https://github.com/hungpham2511/toppra) - A library for computing the time-optimal path parametrization for robots subject to kinematic and dynamic constraints.
- [tinyspline](https://github.com/msteinbeck/tinyspline) - TinySpline is a small, yet powerful library for interpolating, transforming, and querying arbitrary NURBS, B-Splines, and Bézier curves.
- [dual quaternions ros](https://github.com/Achllle/dual_quaternions_ros) - ROS python package for dual quaternion SLERP.
- [mb planner](https://github.com/unr-arl/mbplanner_ros) - Aerial vehicle planner for tight spaces. Used in DARPA SubT Challenge.
- [ilqr](https://github.com/anassinator/ilqr) - Iterative Linear Quadratic Regulator with auto-differentiatiable dynamics models.
- [EGO-Planner](https://github.com/ZJU-FAST-Lab/ego-planner) - A lightweight gradient-based local planner without ESDF construction, which significantly reduces computation time compared to some state-of-the-art methods.
- [pykep](https://github.com/esa/pykep) - A scientific library providing basic tools for research in interplanetary trajectory design.
- [am_traj](https://github.com/ZJU-FAST-Lab/am_traj) - Alternating Minimization Based Trajectory Generation for Quadrotor Aggressive Flight.
- [GraphBasedLocalTrajectoryPlanner](https://github.com/TUMFTM/GraphBasedLocalTrajectoryPlanner) - Was used on a real race vehicle during the Roborace Season Alpha and achieved speeds above 200km/h.
- [Ruckig](https://ruckig.com) - Instantaneous Motion Generation. Real-time. Jerk-constrained. Time-optimal.

## 7. Control
*控制*
- [PID](https://en.wikipedia.org/wiki/PID_controller)
- [Open Source Car Control](https://github.com/PolySync/oscc) -  An assemblage of software and hardware designs that enable computer control of modern cars in order to facilitate the development of autonomous vehicle technology.
- [control-toolbox](https://github.com/ethz-adrl/control-toolbox) - An efficient C++ library for control, estimation, optimization and motion planning in robotics.
- [mpcc](https://github.com/alexliniger/MPCC) - Model Predictive Contouring Controller for Autonomous Racing.
- [open_street_map](https://github.com/ros-geographic-info/open_street_map) - ROS packages for working with Open Street Map geographic information.
- [autogenu-jupyter](https://github.com/mayataka/autogenu-jupyter) - This project provides the continuation/GMRES method (C/GMRES method) based solvers for nonlinear model predictive control (NMPC) and an automatic code generator for NMPC.
- [OpEn](https://github.com/alphaville/optimization-engine) - A solver for Fast & Accurate Embedded Optimization for next-generation Robotics and Autonomous Systems.

## 9.  Dataset and Competition
*数据集与竞赛*

- [KITTI](http://www.cvlibs.net/datasets/kitti/)
- [BDD100k](https://www.bdd100k.com/)
- [UrbanNav](https://github.com/weisongwen/UrbanNavDataset) - 一个在亚洲城市峡谷（包括东京和香港）收集的开源本地化数据集,主要用于解决定位算法的各种问题。
- [ONCE](https://once-for-auto-driving.github.io)
- [SODA10M](https://soda-2d.github.io/)
- [OPV2V](https://mobility-lab.seas.ucla.edu/opv2v/) - 首个大型自动驾驶协同感知数据集 + banchmark代码框架, 由UCLA提供

## 10. Data Loop
*数据闭环*

**主动学习**

- [Discriminative Active Learning](https://github.com/dsgissin/DiscriminativeActiveLearning)

## 11. Visualization
*可视化工具*

- [Carla-birdeye-view](https://github.com/deepsense-ai/carla-birdeye-view) - 可以对接carla的自动驾驶鸟瞰图组件。
- [Uber AVS](https://avs.auto/#/) - 自动驾驶可视化前端组件 xviz 与 streetscape.gl 
- [Cruise](https://webviz.io/worldview/#/) - Cruise 开源的一款自动驾驶前端可视化套件


## 12. Others
*其他更好的分享*
- [awesome-3D-object-detection](https://github.com/Tom-Hardy-3D-Vision-Workshop/awesome-3D-object-detection)
- [3D-ObjectDetection-and-Pose-Estimation](https://github.com/littlebearsama/3D-ObjectDetection-and-Pose-Estimation) -物体检测与位姿估计
