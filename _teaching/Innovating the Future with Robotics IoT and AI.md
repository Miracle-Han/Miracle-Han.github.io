---
title: "帝国理工学院 - 暑校： Innovating the Future with Robotics IoT and AI"
collection: teaching
type: "Research"
permalink: /projects/SummerSchool
venue: "Fuzhou University, Imperial College"
date: 2022-07-01
location: "Fuzhou, China"
---
<br>

# [基于机器人、物联网和人工智能创新未来](https://www.imperial.ac.uk/continuing-professional-development/short-courses/online-courses/masterclasses/future-with-robotics/) 背景介绍
当下处于一个机器人、人工智能和物联网在塑造未来方面发挥重要作用的时代。这些最先进的应用正在改变行业的技术进步。通过参加此项课程了解这些技术，应用知识和学习经验来设计和开发机器人、人工智能和虚拟现实应用。

<br>

# 课题简介 - 垃圾分类环卫机器人
城市垃圾管理是环境保护的重要组成部分。垃圾分类可以有效减少填埋和焚烧的垃圾量，提高资源的回收利用率。环卫机器人在垃圾分类中的应用有助于实现更精确和高效的分类，从而推动可持续发展。

随着人工智能、机器人技术的发展，垃圾分类环卫机器人得以实现自动识别和分类垃圾。机器人配备的传感器、摄像头和数据处理系统使其能够高效地完成复杂的分类任务，提高垃圾分类的准确性。

在此项目中，我们通过网络摄像头和深度学习，建立了垃圾分类算法模型。然后用常用的公共数据集进行训练，提高识别精度。利用ROS和Gazebo建立虚拟机器人模型和工作场景，编写控制代码控制机器人的自主运动和机械臂的姿态规划。

<br>

# 责任描述
设计垃圾分类环卫机器人结构模型。在Rviz和Gazebo中搭建仿真模型。解算6DoF机械臂正逆运动学，在关节空间下进行机械臂的轨迹设计和运动规划。

<br>

# 成果展示
## 垃圾分类环卫机器人渲染图
<br/><img src='/images/Project/SummerSchool/2.jpg'>

## 垃圾分类环卫机器人结构爆炸图
<br/><img src='/images/Project/SummerSchool/3.jpg'>

## Rviz中的垃圾分类环卫机器人仿真
<br/><img src='/images/Project/SummerSchool/1.jpg'>

## 关节空间轨迹规划原理
### 1. 确定初始和目标位置
- **初始位置：** 机械臂当前的关节角度
- **目标位置：** 机械臂期望姿态下的关节角度

### 2. 关节空间插值
通过插值方法生成从初始位置到目标位置的中间关节角度，确保运动的平滑性。
- **线性插值：** 
对于每个关节，从初始位置到目标位置进行线性插值。
-  **q(t) = q_initial + t/T(q_target - q_initial)** 

### 3. 生成轨迹
将插值后的关节角度序列转换为轨迹点，形成完整的轨迹序列。

### 4. 执行轨迹
将生成的轨迹发送给机械臂的控制器，依次执行每个轨迹点的运动。