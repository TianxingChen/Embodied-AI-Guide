<h1 align="center">Embodied-AI-Guide<br>控制篇</h1>

> 这一章并不是为了让你“立刻跑一个模型”，而是为具身智能系统提供**稳定性、可解释性与工程底座**。控制论保证系统在高频下不崩溃，机器人学提供几何与动力学约束，SLAM 与状态估计让机器人“知道自己在哪里”，ROS 与工程库则把理论变成可复现的系统。

## (1) Control and Robotics —— 控制论与机器人学基础

这一章覆盖的是具身智能中**最底层、也最容易被跳过的能力层**。  
控制与机器人学本身并不会直接提高 benchmark 分数，但它们决定了系统是否**稳定、可解释、可调试、可部署**。如果说算法篇解决的是“我想让机器人做什么”，那么这一章回答的是：机器人**凭什么**能连续、安全、可控地做到。

---

### (1.1) 经典课程

推荐把学习路线收敛到两门课程即可，其它材料作为补充参考：

- **Modern Robotics（Northwestern）**：[link](https://www.bilibili.com/video/BV1GJ411k7fE)  
  系统覆盖坐标系、自由度、FK/IK、旋量与运动学，是机器人学入门的首选。
- **Advanced Robotics（Berkeley, Abbeel）**：[link](https://www.bilibili.com/video/BV1h7411A7B9)  
  从控制、规划到 RL / IL / Sim2Real，强调真实系统与决策问题。

> 推荐顺序：**Modern Robotics → Advanced Robotics**  
> 前者解决“机器人是什么”，后者解决“机器人如何在真实世界中做决策”。

---

## (2) 控制理论基础（Control Foundations）

控制论的目标不是“聪明”，而是**稳定、可预测与可调试**。  
在具身系统中，学习策略通常建立在控制系统之上：控制负责高频稳定，学习负责复杂决策。

### (2.1) 经典控制（Classical Control）

这一部分帮助你建立对“反馈系统”的直觉：系统建模、反馈回路、时域与频域分析、传递函数，以及前馈与反馈的区别。

**PID 控制是必须掌握的最低配工具**：  
原理直觉：[link](https://blog.csdn.net/name_longming/article/details/115093338)，视频讲解：[link](https://www.bilibili.com/video/BV1B54y1V7hp)。  
在真实机器人调试中，PID 往往是你**第一个、也是最常用的工具**。

---

### (2.2) 现代控制（线性系统与最优控制）

现代控制将问题表述为优化问题，关注系统的整体行为而非单一参数调节。核心包括状态空间模型、状态反馈以及最优控制（如 LQR）。

推荐材料包括：  
Modern Control Systems（Bishop & Dorf）：[link](http://103.203.175.90:81/fdScript/RootOfEBooks/E%20Book%20collection%20-%202024/EEE/Modern_control_systems_Robert_H_Bishop_Richard_C_Dorf_z_lib_org.pdf)，  
LQR 直观讲解：[link](https://www.bilibili.com/video/BV1Ng4y1V7JQ)，  
以及 **CMU 16-745 Optimal Control**（非常推荐）：  
Website：[link](https://optimalcontrol.ri.cmu.edu/)，YouTube：[link](https://www.youtube.com/playlist?list=PLZnJoM76RM6IAJfMXd1PgGNXn3dxhkVgI)，Bilibili：[link](https://space.bilibili.com/504273533/lists/6271656?type=season)。

---

### (2.3) 先进控制（Advanced Control）

在操作与交互任务中，以下方法尤为关键：鲁棒控制（应对模型不准）、阻抗/导纳/力位混合控制（[link](https://blog.csdn.net/a735148617/article/details/108564836)）、模型预测控制（MPC）以及基于学习的控制方法。

> 在真实系统中，**力控 + MPC + 学习策略** 是非常常见且实用的组合。

---

## (3) 机器人学导论（Robotics Foundations）

机器人学解决的是“**几何 + 物理 + 结构**”问题，是控制与感知能够落地的前提。

### (3.1) 推荐教材与材料

核心课程与教材包括：  
现代机器人学课程：[link](https://www.youtube.com/watch?v=29LhXWjn7Pc&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx)，  
以及《现代机器人学：机构、规划与控制》（Kevin Lynch）、《机构学与机器人学的几何基础与旋量代数》（戴建生）、《机器人学的现代数学理论基础》（丁希仑）。

---

### (3.2) 运动学与动力学（Kinematics & Dynamics）

运动学关注“能不能到达”，动力学关注“能不能稳住、能不能用力”。

快速建立直觉可参考：  
IK/FK 直觉视频：[link](https://www.bilibili.com/video/BV18E411v7F9)，原理概览：[link](https://blog.csdn.net/Dwzsa/article/details/142386529)。

系统学习可参考：  
IK 视频：[link](https://www.bilibili.com/video/BV1PD4y1t7xP)、[link](https://www.bilibili.com/video/BV1Tt4y1T79Z)，  
FK 视频：[link](https://www.bilibili.com/video/BV1Ve4y127Uf)、[link](https://www.bilibili.com/video/BV1a14y157uL)，  
IK 理论参考：[link](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html)。

动力学中尤其重要的是斜对称矩阵、Twist、Exponential of Twist 与旋量代数——操作机器人、力控、MPC 与 whole-body control 都离不开这些概念。

---

### (3.3) 里程计与 SLAM（State Estimation）

状态估计决定了机器人是否“知道自己在哪里”。  
常见方法基于 EKF 或优化，融合 IMU、相机、雷达、轮速计等传感器，形成 VIO / LIO / LIVO 等体系。

代表系统包括：  
VINS-Mono：[link](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)，ORB-SLAM3：[link](https://github.com/UZ-SLAMLab/ORB_SLAM3)，VINS-Fusion：[link](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)，LOAM：[link](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf)，FAST-LIO：[link](https://github.com/hku-mars/FAST_LIO)，FAST-LIVO：[link](https://github.com/hku-mars/FAST-LIVO2)。

SLAM 进一步将定位与建图结合，推荐参考：  
SLAM Handbook：[link](https://github.com/SLAM-Handbook-contributors/slam-handbook-public-release)，经典综述：[link](https://arxiv.org/abs/1606.05830)，《视觉 SLAM 十四讲》：[link](https://github.com/gaoxiang12/slambook2)，以及端到端方法 DROID-SLAM：[link](https://arxiv.org/abs/2108.10869)。

---

### (3.4) 工程生态与工具（Engineering Stack）

ROS 是把理论变成系统的关键纽带：  
ROS1 入门：[link](http://www.autolabor.com.cn/book/ROSTutorials/)，ROS2 入门：[link](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)，ROS2 Humble 3h 教程：[link](https://discourse.openrobotics.org/t/ros2-humble-3h-tutorial-for-beginners/28500/)，Open Robotics 官网：[link](https://openrobotics.org/)。

常用机器人库包括：  
cuRobo（CUDA 加速 IK / 碰撞 / 规划）：[link](https://curobo.org/)，  
IKFast：[link](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html)，  
mplib：[link](https://github.com/haosulab/mplib)。

其他工程细节如多传感器时间同步：[link](https://blog.csdn.net/qq_43495930/article/details/125649446)，以及 LeRobot SO-100 实践：[link](https://huggingface.co/lerobot)。
