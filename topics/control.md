<h1 align="center">Embodied-AI-Guide<br>控制篇</h1>

> 这一章并不是为了让你「立刻跑一个模型」，而是为具身智能系统提供**稳定性、可解释性与工程底座**。控制论保证系统在高频下不崩溃，机器人学提供几何与动力学约束，SLAM 与状态估计让机器人「知道自己在哪里」，ROS 与工程库则把理论变成可复现的系统。

<section id="control-robotics"></section>

## (1) Control and Robotics —— 控制论与机器人学基础

这一章覆盖的是具身智能中**最底层、也最容易被跳过的能力层**。控制与机器人学本身并不会直接提高 benchmark 分数，但它们决定了系统是否**稳定、可解释、可调试、可部署**。如果说算法篇解决的是「我想让机器人做什么」，那么这一章回答的是：机器人**凭什么**能连续、安全、可控地做到。

### (1.0) 先说清楚：要学到什么程度

控制理论是一个能读一辈子的领域，新人最容易犯的错是**一头扎进去补三个月数学，却迟迟没碰过真机**。实际上，不同目标需要的深度差别很大：

| 你的目标 | 需要掌握的程度 | 建议投入 |
|---|---|---|
| 训练 VLA / 操作策略，机器人由厂商 SDK 驱动 | 知道 FK/IK 在做什么、关节空间与末端空间的区别、阻抗控制为什么比位置控制安全 | 一周，够用即可 |
| 自己搭真机、调机械臂、做力控任务 | 上面全部，再加 PID 调参、坐标变换、手眼标定、实时性与延迟 | 一个月，边调边学 |
| 做人形 / 四足运动控制、全身控制 | 再加刚体动力学、旋量代数、最优控制（LQR / MPC）、接触与摩擦建模 | 三个月以上，需要系统学 |
| 做移动机器人、需要自主定位导航 | 再加状态估计、EKF、图优化与 SLAM | 两个月以上 |

> 🌱 **给新人的建议**：先按第一行的标准过一遍，尽快去[第 2 章的实战教程](../README.md#robotwin)把策略跑通；等你真的被某个问题卡住（机械臂抖、抓取时把物体捏碎、末端到不了目标点），再回头精读对应章节，效率会高得多。**控制是「按需补课」最划算的一章。**

---

<section id="control-courses"></section>

### (1.1) 经典课程

材料很多，但真正需要从头看完的只有两门，其余当工具书查即可：

- **Modern Robotics（Northwestern，Kevin Lynch）**：[bilibili](https://www.bilibili.com/video/BV1GJ411k7fE)｜[课程主页](https://hades.mech.northwestern.edu/index.php/Modern_Robotics)  
  系统覆盖坐标系、自由度、FK/IK、旋量与运动学，是机器人学入门的首选。配套教材与 Python 库可直接跑，边看边验证。
- **Advanced Robotics（Berkeley，Pieter Abbeel）**：[bilibili](https://www.bilibili.com/video/BV1h7411A7B9)  
  从控制、规划到 RL / IL / Sim2Real，强调真实系统与决策问题，是连接「控制」与「学习」两套语言的桥梁。

> 推荐顺序：**Modern Robotics → Advanced Robotics**。前者解决「机器人是什么」，后者解决「机器人如何在真实世界中做决策」。

---

<section id="control-foundations"></section>

## (2) Control Foundations —— 控制理论基础

控制论的目标不是「聪明」，而是**稳定、可预测与可调试**。在具身系统中，学习策略几乎总是建立在控制系统之上：**控制负责高频稳定，学习负责复杂决策**。你训练出来的 VLA 通常以 10~50 Hz 输出目标位姿，而真正把电机拧到那个位置的，是底下以 500~1000 Hz 运行的控制器。

<section id="classical-control"></section>

### (2.1) 经典控制（Classical Control）

这一部分帮助你建立对「反馈」的直觉：系统建模、反馈回路、时域与频域分析、传递函数，以及前馈与反馈的区别。一句话概括反馈：**测量实际值与目标值的差，再按这个差去调整输出**。

**PID 是必须掌握的最低配工具**——它只有三个参数（比例、积分、微分），却能解决真实调试中相当一部分问题：

- 原理直觉：[博客](https://blog.csdn.net/name_longming/article/details/115093338)｜[视频讲解](https://www.bilibili.com/video/BV1B54y1V7hp)

> 🌱 **新人最常遇到的三个现象**：机械臂到位后来回抖（P 太大或 D 太小）、始终差一点点到不了目标（缺积分项或存在静摩擦）、启动时猛冲一下（积分饱和，需要加 anti-windup）。认出这三种现象，比背下传递函数推导更有用。

---

<section id="modern-control"></section>

### (2.2) 现代控制（线性系统与最优控制）

经典控制一次调一个回路，现代控制则把整个系统写成**状态空间模型**，并把控制问题表述成一个**优化问题**：给定代价函数（例如「既要快速到达目标，又不要用太大力矩」），求最优的控制序列。LQR 是其中最经典的解析解，也是后面 MPC 的基础。

| 材料 | 链接 | 适合什么时候看 |
|---|---|---|
| LQR 直观讲解 | [bilibili](https://www.bilibili.com/video/BV1Ng4y1V7JQ) | 想先建立直觉、不想啃公式时 |
| CMU 16-745 Optimal Control ⭐ | [主页](https://optimalcontrol.ri.cmu.edu/)｜[YouTube](https://www.youtube.com/playlist?list=PLZnJoM76RM6IAJfMXd1PgGNXn3dxhkVgI)｜[bilibili](https://space.bilibili.com/504273533/lists/6271656?type=season) | 想系统学最优控制与轨迹优化，作业含 Julia 代码，强烈推荐 |
| Modern Control Systems（Dorf & Bishop） | 经典教材，按书名检索正版即可 | 当工具书查概念 |

---

<section id="advanced-control"></section>

### (2.3) 先进控制（Advanced Control）

真实机器人和教科书里的模型总是不一样——负载会变、关节有摩擦、接触瞬间力会突变。先进控制就是处理这些「不理想」的：

| 方法 | 解决什么问题 | 在具身智能里的典型场景 |
|---|---|---|
| 鲁棒 / 自适应控制 | 模型参数不准或会变化 | 机械臂抓起未知重量的物体后仍能稳住 |
| 阻抗 / 导纳控制（[参考](https://blog.csdn.net/a735148617/article/details/108564836)） | 让机器人「软」下来，控制的是力与位移的关系而非硬位置 | 插拔、擦拭、人机协作；也是不把物体捏碎的关键 |
| 力位混合控制 | 某些方向控位置、某些方向控力 | 打磨平面：法向控力、切向控位置 |
| 模型预测控制（MPC） | 在滚动时域内反复求解优化，能显式处理约束 | 四足 / 人形的步态生成、移动底盘避障 |

> 在真实系统中，**阻抗控制 + MPC + 学习策略**是非常常见且实用的组合：学习策略给目标，MPC 保证约束与可行性，阻抗控制保证接触时的安全。
>
> 🌱 如果你只打算记一件事：**做接触类任务时，把机械臂从位置控制切到阻抗/力控模式**。这一条能避免绝大多数「策略看起来没问题，但一碰到物体就报错或损坏」的事故。

---

<section id="robotics-foundations"></section>

## (3) Robotics Foundations —— 机器人学导论

机器人学解决的是「**几何 + 物理 + 结构**」问题，是控制与感知能够落地的前提。

<section id="robotics-books"></section>

### (3.1) 推荐教材与材料

- **《现代机器人学：机构、规划与控制》（Kevin Lynch & Frank Park）**：[课程视频](https://www.youtube.com/watch?v=29LhXWjn7Pc&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx)｜[主页与配套代码](https://hades.mech.northwestern.edu/index.php/Modern_Robotics)  
  有中文版，是目前最推荐的入门教材：用旋量（screw theory）统一处理运动学，比传统 DH 参数法更直观，配套 Python 库能直接验证公式。
- 进阶数学：《机构学与机器人学的几何基础与旋量代数》（戴建生）、《机器人学的现代数学理论基础》（丁希仑）——只在你需要推导时再翻。

---

<section id="kinematics-dynamics"></section>

### (3.2) 运动学与动力学（Kinematics & Dynamics）

一句话区分：**运动学关注「能不能到达」，动力学关注「能不能稳住、能不能用力」**。

- **正运动学 FK**：已知每个关节转了多少度，求末端夹爪在空间中的位置姿态。解唯一，算起来简单。
- **逆运动学 IK**：已知想让夹爪去哪，反求各关节该转多少度。**可能无解（够不着）、也可能有无穷多解（七自由度冗余臂）**，因此工程上常用数值求解器并加入关节限位、避障、平滑性等额外约束。

这正是为什么策略输出「关节角」还是「末端位姿」（即 RoboTwin 教程里的 `action_type` 选 `joint` 还是 `ee`）会带来实际差异：前者绕开 IK 但难以跨本体迁移，后者更通用但依赖一个可靠的 IK 求解器。

| 主题 | 材料 |
|---|---|
| FK / IK 快速直觉 | [视频](https://www.bilibili.com/video/BV18E411v7F9)｜[原理概览](https://blog.csdn.net/Dwzsa/article/details/142386529) |
| IK 系统讲解 | [视频一](https://www.bilibili.com/video/BV1PD4y1t7xP)｜[视频二](https://www.bilibili.com/video/BV1Tt4y1T79Z)｜[理论参考](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html) |
| FK 系统讲解 | [视频一](https://www.bilibili.com/video/BV1Ve4y127Uf)｜[视频二](https://www.bilibili.com/video/BV1a14y157uL) |

动力学中尤其重要的是斜对称矩阵、Twist（旋量速度）、Exponential of Twist 与旋量代数——操作机器人、力控、MPC 与全身控制都离不开这些概念。它们的共同作用是：**用一套统一的代数描述「旋转 + 平移」，避免欧拉角带来的万向节死锁与数值问题**。

---

<section id="slam"></section>

### (3.3) 里程计与 SLAM（State Estimation）

状态估计决定了机器人是否「知道自己在哪里」。做桌面操作时这一层往往被相机外参代替，但只要机器人开始移动（移动操作、四足、无人机），它就变成必修课。

常见做法是用 EKF 或图优化融合 IMU、相机、雷达、轮速计，按传感器组合分成几个体系：**VIO**（视觉 + IMU）、**LIO**（激光 + IMU）、**LIVO**（激光 + 视觉 + IMU）。

| 体系 | 代表系统 | 链接 | 特点 |
|---|---|---|---|
| VIO | VINS-Mono / VINS-Fusion | [Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)｜[Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion) | 成本低、依赖纹理；无人机与手持设备常用 |
| 视觉 SLAM | ORB-SLAM3 | [repo](https://github.com/UZ-SLAMLab/ORB_SLAM3) | 特征点法经典实现，支持单目/双目/RGB-D |
| LIO | LOAM / FAST-LIO | [LOAM](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf)｜[FAST-LIO](https://github.com/hku-mars/FAST_LIO) | 精度高、对光照不敏感，室外与大场景首选 |
| LIVO | FAST-LIVO2 | [repo](https://github.com/hku-mars/FAST-LIVO2) | 激光与视觉互补，退化场景更鲁棒 |
| 端到端 | DROID-SLAM | [paper](https://arxiv.org/abs/2108.10869) | 学习式稠密 SLAM，纹理弱时表现好但吃显存 |

系统学习推荐：[SLAM Handbook](https://github.com/SLAM-Handbook-contributors/slam-handbook-public-release)（社区编写，覆盖面新且全）、[《视觉 SLAM 十四讲》](https://github.com/gaoxiang12/slambook2)（中文入门首选，代码可跑）、[经典综述](https://arxiv.org/abs/1606.05830)（理解领域脉络）。

---

<section id="engineering-stack"></section>

### (3.4) 工程生态与工具（Engineering Stack）

**ROS 是把理论变成系统的关键纽带**。它本质上是一套进程间通信规范加一堆现成工具：相机、机械臂、雷达各自跑一个节点，通过话题（topic）互发消息，你就不用自己写驱动和通信。新项目请直接学 ROS 2，ROS 1 已停止维护。

| 资源 | 链接 | 说明 |
|---|---|---|
| ROS 2 入门（中文） | [link](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/) | 中文教程，从话题服务讲到工程组织 |
| ROS 2 官方教程 | [link](https://docs.ros.org/en/humble/Tutorials.html) | 官方文档，遇到概念不清时的权威来源 |
| ROS 2 三小时速成 | [link](https://discourse.openrobotics.org/t/ros2-humble-3h-tutorial-for-beginners/28500/) | 时间紧时先过一遍 |
| ROS 1 入门（仅供维护老项目） | [link](http://www.autolabor.com.cn/book/ROSTutorials/) | 很多经典代码库仍是 ROS 1 |

常用机器人库：

| 库 | 链接 | 用途 |
|---|---|---|
| cuRobo | [link](https://curobo.org/) | CUDA 加速的 IK、碰撞检测与运动规划，实时性好 |
| MoveIt 2 | [link](https://moveit.picknik.ai/main/index.html) | ROS 生态里最通用的运动规划框架 |
| mplib | [link](https://github.com/haosulab/mplib) | 轻量规划库，不依赖 ROS，SAPIEN / RoboTwin 常用 |
| IKFast | [link](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html) | 为特定机械臂生成解析 IK，速度极快 |
| Pinocchio | [link](https://github.com/stack-of-tasks/pinocchio) | 高效刚体动力学库，MPC 与全身控制的常用底座 |

其他工程细节：[多传感器时间同步](https://blog.csdn.net/qq_43495930/article/details/125649446)（数据对不齐会让训练出的策略莫名其妙地差）、[LeRobot](https://github.com/huggingface/lerobot)（SO-100 / SO-101 等低成本机械臂的软硬件实践，是目前最便宜的真机入门路径）。

---

<section id="wbc"></section>

## (4) Whole-Body Control —— 全身控制与人形运动 ⭐

前三节讲的大多以机械臂为例：机械臂固定在桌上，只要末端到位就算成功。**人形与四足机器人不一样——它没有被固定住，用力过猛就会摔倒。** 全身控制（Whole-Body Control, WBC）要解决的正是这个问题：把控制目标从「机械臂末端」扩展到躯干、腿、手臂、头的整个身体，在完成任务的同时维持平衡。

它的难点可以归结为一句话：**机器人只能通过脚与地面的接触来给自己施力，而这个接触是单向的（只能推不能拉）、有摩擦上限的、还随时可能断开。** 所以人形控制的本质是在一堆接触约束下做实时优化。

### (4.1) 模型式与学习式两条路线

| 路线 | 做法 | 优势 | 代价 |
|---|---|---|---|
| **模型式**（MPC + WBC） | 用简化模型（如线性倒立摆）在线做优化，求解满足接触约束的关节力矩 | 可解释、可加硬约束、不需要训练 | 依赖准确建模，复杂地形与富接触场景难写 |
| **学习式**（仿真中 RL） | 在 GPU 上并行几千个环境跑强化学习，再迁移到真机 | 能学出手工难以设计的动态行为（跑、跳、翻滚） | 奖励函数难调，且必须跨越 Sim2Real Gap |

2025 年之后，**学习式路线在人形与四足上已经成为主流**，模型式方法更多作为安全层或对照基线保留。

### (4.2) 入门路径

新人从零做人形运动控制，最快的路线不是先读论文，而是**先跑通一个现成仓库看到机器人在仿真里走起来**，再回头理解每一项奖励在做什么。

| 顺序 | 项目 | 链接 | 为什么放在这个位置 |
|---|---|---|---|
| 1 | **GMT**（General Motion Tracking） | [paper](https://arxiv.org/abs/2506.14770)｜[repo](https://github.com/zixuan417/humanoid-general-motion-tracking) | 上手门槛最低：只依赖 MuJoCo、附预训练权重，笔记本就能看到 Unitree G1 跟着动捕数据动起来 |
| 2 | **Unitree RL Lab / unitree_rl_gym** | [rl_lab](https://github.com/unitreerobotics/unitree_rl_lab)｜[rl_gym](https://github.com/unitreerobotics/unitree_rl_gym) | 厂商官方，本体模型与真机部署链路最可靠；有 G1 / H1 的话从这里开始 |
| 3 | **ASAP** | [repo](https://github.com/LeCAR-Lab/ASAP) | 讲清楚 Sim2Real Gap 怎么补：先在仿真训练，再用真机数据学一个「残差动作」模型去补偿物理误差 |
| 4 | **BeyondMimic** | [paper](https://arxiv.org/abs/2508.08241)｜[主页](https://beyondmimic.github.io/)｜[repo](https://github.com/HybridRobotics/whole_body_tracking) | 目前动作跟踪质量的标杆（后空翻、冲刺、侧手翻），并已成为多个公开 RL 仓库的默认方法 |
| 5 | **HOVER** | [repo](https://github.com/NVlabs/HOVER) | NVIDIA 的通用神经全身控制器，理解「一个策略支持多种控制接口」的思路 |

### (4.3) 训练框架与工具

| 工具 | 链接 | 定位 |
|---|---|---|
| Isaac Lab | [repo](https://github.com/isaac-sim/IsaacLab) | 目前最主流的机器人 RL 框架，GPU 并行环境数最多 |
| mjlab | [paper](https://arxiv.org/abs/2601.22074)｜[repo](https://github.com/mujocolab/mjlab)｜[文档](https://mujocolab.github.io/mjlab/) | 把 Isaac Lab 的接口搬到 MuJoCo Warp 上，去掉了 Isaac Sim 依赖，装起来轻得多 |
| HumanoidVerse | [repo](https://github.com/LeCAR-Lab/HumanoidVerse) | 支持 Isaac Gym / Isaac Sim / MuJoCo 多后端，ASAP 的训练底座 |
| MuJoCo Playground | [主页](https://playground.mujoco.org/) | 现成的运动控制环境集合，适合快速验证算法 |

### (4.4) 动作重定向与遥操作

人形 RL 的主流做法是**让机器人模仿人类动作**，而人类动捕数据（骨骼比例、自由度）和机器人本体对不上，中间必须做一步**重定向（Retargeting）**。这一步几乎是所有人形动作跟踪工作的共同前置：

- **GMR**（General Motion Retargeting）：[repo](https://github.com/YanjieZe/GMR) —— 实时把 AMASS / SMPL-X、动捕 BVH / FBX 等格式的人体动作转到 17 种以上人形本体上，且特意调过参数使下游 RL 跟踪策略能训得动，是目前的事实标准。
- **TWIST**：[repo](https://github.com/YanjieZe/TWIST) —— 用「教师-学生」蒸馏做实时全身遥操作，人穿动捕设备即可直接驱动人形机器人，可用于采数据。

> 🌱 **给新人的提醒**：人形运动控制对**仿真并行采样**高度依赖，一次训练动辄需要几千个并行环境跑上亿步——这意味着它比操作方向更吃显卡，且**几乎不可能在没有仿真的情况下做**。如果你手上只有一块消费级显卡，建议从四足（自由度更少、训练更快）或本指南[算法篇的操作方向](./algorithm.md#robot-learning)入手。
>
> 另外注意，人形领域的产品宣传视频常常来自遥操作或高度特化的策略，**看到惊艳的演示时先确认它是自主还是遥操**。
