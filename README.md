# 基于机器视觉和机械臂的分拣系统探索
## 背景
应用在工业生产中的机械臂大多为示教型机械臂，如Delta并联机器人、SCARA装配机器人等。这一类机械臂对工作环境的要求较高，需要提前设置运动轨迹和动作顺序，其通用性能和构建成本较高。  
将机器视觉与传统示教型机械臂结合，在控制成本的前提下进一步拓展传统机械臂适用场景和能力成为一种方向。  
## 项目介绍
本次研究的基于视觉与机械臂的物品分拣系统总体架构主要由3部分组成：Kinect、Dobot机械臂、上位机（PC）。整个系统的图像数据依赖于Kinect采集目标物与周边环境的深度信息，而后提供给上位机进行图像处理和数据计算；上位机接收深度图像及深度信息，通过深度信息检测物品、计算物品尺寸、定位抓取点，规划机械臂运动轨迹，生成各关节电机控制命令；机械臂接收上位机控制命令，执行命令，完成物品的抓取与放置，完成既定工作，再进入伺服状态。  
由于和正常机器视觉项目选用的图像采集设备大相径庭，本项目涉及的具体code与大多数相似项目并不通用。其他开放性思路还包括但不仅限于各种类SURF算子匹配模型、利用深度信息剥离有用图像提升交互体验。
  
  
>>注：利用深度摄像头采集深度信息需要进行一定的预处理，深度信息的数据量远大于传统RGB摄像头采集到的数据，实现动态监测还需进一步优化。
