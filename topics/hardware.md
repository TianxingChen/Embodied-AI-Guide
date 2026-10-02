<h1 align="center">Embodied-AI-Guide<br>硬件篇</h1>

> 具身智能硬件涵盖多个技术栈：嵌入式软硬件、机械设计、机器人系统集成与传感器等。它们知识面很杂，但共同目标只有一个：把「算法」变成真实世界里稳定可复现的系统。  
> 关于硬件学习，最有效的方式几乎永远是 **从实践出发**——先做出一个能跑起来的最小系统，再逐步扩展复杂度与可靠性。

<section id="embedded"></section>

## (1) Embedded —— 嵌入式

嵌入式决定了机器人「神经系统」的下限：通信是否稳定、控制是否实时、驱动是否安全。建议按 **入门单片机 → STM32 工程 → 电机驱动 → 嵌入式 Linux** 的顺序推进。

| 路线/主题 | 资源 | 链接 | 说明 |
|---|---|---|---|
| 总览路线 | 嵌入式学习路线 | [link](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452) | 用于建立学习路径与关键词地图 |
| 入门 | 51 单片机 | [link](https://www.bilibili.com/video/BV1Mb411e7re) | 江科大自动协经典入门 |
| 主流工程 | STM32 单片机 | [link](https://www.bilibili.com/video/BV1th411z7sn) | 从外设到工程结构 |
| 驱动关键 | STM32 电机驱动（野火） | [link](https://www.bilibili.com/video/BV1AZ4y1V7wt) | 控制闭环常见落点 |
| 工程体系 | 野火 STM32 标准库 | [link](https://www.bilibili.com/video/BV1yW411Y7Gw) | 更贴近工程写法 |
| 工程体系 | 正点原子 STM32 | [link](https://www.bilibili.com/video/BV1Lx411Z7Qa) | 资料全，适合查漏补缺 |
| 上位平台 | 韦东山嵌入式 Linux | [link](https://www.bilibili.com/video/BV1w4411B7a4) | 走向系统级开发与部署 |

**小结**：  
做具身硬件时，嵌入式的价值不在「写出更炫的代码」，而在「系统能稳定跑、延迟可控、驱动可靠」。很多项目后期的崩溃都不是算法问题，而是控制链路与工程细节问题。

---

<section id="mechanical"></section>

## (2) Mechanical Design —— 机械设计

机械设计决定了机器人「身体」的能力边界：可达空间、刚度、负载、布线与维护成本等。对于算法同学来说，机械最关键的产出通常是 **可制造的 CAD** 与 **可用于仿真/控制的 URDF**。

| 主题 | 资源 | 链接 | 说明 |
|---|---|---|---|
| CAD 入门 | SolidWorks 教学 | [link](https://www.bilibili.com/video/BV1iw411Z7HZ) | 面向装配体与工程制图 |
| 工程衔接 | 从 SolidWorks 生成 URDF | [link](https://blog.csdn.net/weixin_45168199/article/details/105755388) | 用装配体导出机器人模型并进入仿真/控制 |

---

<section id="robosystem"></section>

## (3) Robot System Design —— 机器人系统设计

系统设计关注的是「把多个模块拼成一个可维护系统」：硬件接口、软件架构、标定流程、调试策略、日志与安全机制。建议把系统设计当作「把机器人做成产品」的第一步。

| 资源 | 链接 | 说明 |
|---|---|---|
| 《机器人学简介》（教材 PDF） | [link](../files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf) | 质量高，适合系统性阅读 |
| Robotic Systems（Illinois） | [link](https://motion.cs.illinois.edu/RoboticSystems/) | 偏「系统化机器人学」的组织方式 |

---

<section id="sensors"></section>

## (4) Sensors —— 传感器

传感器决定了策略「能看到什么」，因此也直接决定了任务的上限：**数据里没有的信息，再大的模型也变不出来**。具身系统常见的传感器可以按用途分成四类：

| 类别 | 典型器件 | 回答什么问题 | 新人优先级 |
|---|---|---|---|
| 视觉 | RGB 相机、深度相机 | 目标在哪、场景长什么样 | ⭐️⭐️⭐️ 必备 |
| 本体感知 | 关节编码器、IMU | 我自己现在是什么姿态 | ⭐️⭐️⭐️ 通常由本体自带 |
| 力觉 | 关节力矩、六维力/力矩传感器 | 我碰到东西了吗、用了多大力 | ⭐️⭐️ 做接触任务时必需 |
| 触觉 | 视触觉传感器、电子皮肤 | 接触点在哪、是否打滑 | ⭐️ 精细操作与研究方向 |

> 🌱 建议从「能直接用于闭环」的传感器开始（RGB / 深度 / IMU），把流程跑通后再逐步引入触觉这类高难度模态。触觉数据的采集、标定与泛化难度都远高于视觉，不适合作为第一个项目。

<section id="depth-camera"></section>

### (4.1) 深度相机（Depth Camera）

深度相机是具身操作里出镜率最高的传感器。按成像原理主要分三类，选型时的核心权衡是**精度、工作距离与对材质的适应性**：

| 原理 | 特点 | 常见型号 |
|---|---|---|
| 双目 / 主动立体（Active Stereo） | 近距离精度好、室外也能用；对无纹理表面靠投射散斑补救 | RealSense D4xx 系列 |
| 结构光（Structured Light） | 近距离精度最高；怕强光，室外基本不可用 | RealSense SR300、Orbbec Gemini 系列 |
| 飞行时间（ToF / iToF） | 帧率高、受纹理影响小；边缘易飞点，对反光和吸光材质不友好 | Kinect Azure、Orbbec Femto 系列 |

| 设备/生态 | 链接 | 说明 |
|---|---|---|
| Intel RealSense | [SDK](https://github.com/IntelRealSense/librealsense)｜[ROS 2 驱动](https://github.com/IntelRealSense/realsense-ros) | 事实上的研究标准，绝大多数开源代码默认支持 |
| Orbbec 奥比中光 | [SDK](https://github.com/orbbec/OrbbecSDK)｜[ROS 2 驱动](https://github.com/orbbec/OrbbecSDK_ROS2) | 国内供货与售后更方便，型号覆盖三种原理 |
| Luxonis OAK-D | [文档](https://docs.luxonis.com/) | 板载算力，可在相机端直接跑神经网络，省主机资源 |

> ⚠️ **深度相机的三个常见坑**：**透明与高反光物体**（玻璃杯、不锈钢）几乎必然测不到深度，这是原理性限制而非标定问题；**最小工作距离**通常在 20~40 厘米，末端相机装太近会全是空洞；**RGB 与深度需要对齐**（align），否则你按彩色图像素取到的深度值对应的是别的位置。

<section id="force-proprioception"></section>

### (4.2) 力觉与本体感知

- **关节力矩感知**：现在不少协作臂与人形本体通过电流估计或串联弹性驱动（SEA）提供关节力矩反馈，这是实现阻抗控制与碰撞检测的前提，详见[控制篇](./control.md#advanced-control)。
- **六维力/力矩传感器**：装在腕部，直接测量末端受到的三轴力与三轴力矩，精度远高于电流估计，插拔、打磨、装配类任务常用，代表厂商有 ATI、宇立仪器、坤维科技等。
- **IMU**：提供角速度与加速度，是腿式机器人与无人机姿态估计的核心输入；单独使用会随时间漂移，必须与视觉或激光融合（见[控制篇的 VIO / LIO 部分](./control.md#slam)）。

---

<section id="tactile"></section>

## (5) Tactile Sensing —— 触觉感知（接触、力与精细操作）

触觉是「接触世界」的关键模态，尤其在装配、柔性物体、精细抓取和遮挡严重的场景中，触觉往往比视觉更可靠。整体上触觉硬件路线常见两类：**视触觉（Vision-based tactile）** 与 **电子皮肤（E-skin）**。

<section id="vision-tactile"></section>

### (5.1) 视触觉传感器（Vision-Based Tactile Sensors）

视触觉通过摄像头观测弹性介质/标记点的形变，把「触觉」转化为视觉信号来估计接触力、形变与接触几何。它的关键设计点通常包括：传感器形状、标记点布局、材料（硅胶/弹性体）以及光照与成像系统。

- 优点：高分辨率、非侵入、易与视觉系统融合  
- 缺点：依赖视觉计算、易受光照影响、光学与封装设计复杂

两篇综述覆盖「算法视角」和「结构视角」，建议作为起点：  
[算法综述](https://ieeexplore.ieee.org/document/10563188)  
[结构综述](https://link.springer.com/article/10.1007/s10846-021-01431-0)

<section id="electronic-skin"></section>

### (5.2) 电子皮肤（Electronic Skin）

电子皮肤通常用柔性材料（压力薄膜、纳米传感网络等）实现大面积触觉，目标是让机器人拥有类似「全身触觉」的能力，用于安全、人机协作与全身接触交互。

- 优点：可大面积覆盖、高灵敏度、可伸缩适配复杂表面  
- 缺点：制造与成本较高、数据规模大带来处理挑战、长期稳定性与漂移问题

[综述入口](https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00049)

<section id="tactile-applications"></section>

### (5.3) 触觉应用与算法（把触觉变成能力）

触觉算法常见落点可以理解为四类：**姿态/接触估计、识别与分类、触觉操控技能、统一表征/大模型**。

| 方向 | 代表工作 | 链接 |
|---|---|---|
| 姿态/接触估计（in-hand） | 3D Shape Perception from Monocular Vision, Touch, and Shape Priors | [link](https://arxiv.org/abs/1808.03247) |
| 姿态/接触估计（in-scene） | Fast Model-Based Contact Patch and Pose Estimation… | [link](https://ieeexplore.ieee.org/document/8936859) |
| 分类/识别 | Understanding Dynamic Tactile Sensing for Liquid Property Estimation | [link](https://arxiv.org/abs/2205.08771) |
| 分类/识别 | Multimode Fusion Perception for Transparent Glass Recognition | [link](https://www.semanticscholar.org/paper/Multimode-fusion-perception-for-transparent-glass-Zhang-Shan/90109f2eabba717d152a599fc8d8d5a3677c85e5) |
| 触觉操控（装配） | Active Extrinsic Contact Sensing: Peg-in-Hole Insertion | [link](https://ieeexplore.ieee.org/abstract/document/9812017) |
| 触觉操控（技能库） | Building a Library of Tactile Skills Based on Fingervision | [link](https://ieeexplore.ieee.org/abstract/document/9035000) |
| 触觉操控（线缆） | Cable Manipulation with a Tactile-Reactive Gripper | [link](https://arxiv.org/abs/1910.02860) |
| 触觉操控（精细手部） | Manipulation by Feel: Touch-Based Control with Deep Predictive Models | [link](https://arxiv.org/abs/1903.04128) |
| 触觉操控（visuotactile） | NeuralFeels with Neural Fields… | [link](https://www.science.org/doi/10.1126/scirobotics.adl0628) |
| 触觉大模型/统一表征 | Binding Touch to Everything… (CVPR 2024) | [link](https://openaccess.thecvf.com/content/CVPR2024/papers/Yang_Binding_Touch_to_Everything_Learning_Unified_Multimodal_Tactile_Representations_CVPR_2024_paper.pdf) |

**数据工具与标准化**：TLabel（[GitHub](https://github.com/liesliy/tlabel)）是一个开源的触觉数据标注与处理工具包（`pip install tlabel`），提供统一的触觉数据格式标准，支持 GelSight、PaXini、Daimon、UniVTAC 等 10+ 传感器适配器，已被 FTP-1 官方推荐。

#### 触觉的「基础模型」时刻

触觉一直有一个比视觉严重得多的结构性问题：**不同厂商的传感器输出格式完全不同**（有的是弹性体形变图像，有的是压阻阵列，有的是六维力读数），**在一种传感器上训练的模型换个硬件就完全失效**。视觉领域有 ImageNet 和统一的 RGB 格式，触觉领域长期没有。

2026 年出现的几项工作正是冲着这一点去的——共同思路是**先把异构信号投影到一个与硬件无关的共享表征，再在其上训练策略**：

| 工作 | 链接 | 一句话看点 |
|---|---|---|
| FTP-1（Foundation Tactile Policy） | [paper](https://arxiv.org/abs/2606.13102)｜[主页](https://ftp1-policy.github.io/)｜[repo](https://github.com/michaelyuancb/ftp1-policy) | 用约 3000 小时、跨 21 种传感器的数据预训练；不同原理的传感器各用一套编码器，再投影到共享的触觉 Transformer，**能迁移到训练时没见过的传感器** |
| 𝒩₀-Foundation | [repo](https://github.com/neoteai/N0-Foundation) | 把每一帧触觉统一表示成传感面上的三轴力场以屏蔽硬件差异；配套开放了数千小时的 OpenNeoData 数据集 |

仿真侧也开始跟进：Genesis 已内置基于 FOTS 的视触觉传感器仿真，这是主流仿真器第一次把触觉当作一等功能提供。

> 🌱 **给想入坑触觉的新人**：硬件仍以 GelSight Mini 与 DIGIT 为主流研究选择，两者都有成熟的开源生态。但请做好心理准备——触觉的**标定、老化与个体差异**都比视觉严重（同型号的两个传感器数据都可能对不上，弹性体用久了还会变形），这也是为什么统一表征会成为这个方向的核心议题。

<section id="tactile-products"></section>

### (5.4) 传感器购买（从研究到落地）

市面上已有成熟视触觉传感器产品，例如 [GelSight](https://gelsight.com/)

---

<section id="data_collection"></section>

## (6) Data Collection —— 数据采集硬件

真机数据是目前具身智能最贵的资源，而**采集方式直接决定了数据的规模上限与可用性**。所有方案本质上都在同一个权衡上取舍：

> **动作标注越精确，采集成本越高；采集设备越轻便，越需要额外的动作映射（Retargeting）才能给机器人用。**

| 采集范式 | 代表系统 | 链接 | 动机与特点 |
|---|---|---|---|
| 主从遥操作（Teleoperation） | ALOHA / Mobile ALOHA | [ALOHA](https://tonyzhaozh.github.io/aloha/)｜[Mobile ALOHA](https://mobile-aloha.github.io/)｜[视频](https://www.bilibili.com/video/BV1vU421d7BJ/) | 人操作一套「主臂」，从臂实时复现。动作标注**最精确、可直接训练**，但需要一人一机实时操作，规模难上去 |
| VR / 动捕遥操作 | Open-TeleVision | [project](https://robot-tv.github.io/) | 用 VR 头显获得第一人称立体视觉与手部追踪，可远程操作人形；沉浸感好，适合双臂与灵巧手 |
| 手持式采集 | UMI（Universal Manipulation Interface） | [project](https://umi-gripper.github.io/)｜[视频](https://www.bilibili.com/video/BV17w4m1f7Ti/) | 手持一个带相机的夹爪直接在真实环境演示，**脱离机器人本体采集**，成本低、场景多样；代价是要处理本体与视角差异 |
| 外骨骼示教 | AirExo | [project](https://airexo.tech/) | 穿戴与机器人同构的低成本外骨骼，关节角可直接映射，兼顾精度与便携 |
| 灵巧手采集 | DexUMI / 数据手套 | [DexUMI](https://dex-umi.github.io/)｜[数据手套介绍](https://zhuanlan.zhihu.com/p/635065768) | 面向灵巧手与 in-hand 操作，核心难点是**缩小人手与机器人手之间的形态差距** |
| 第一人称人类视频 | Ego4D / EPIC-KITCHENS | [Ego4D](https://ego4d-data.org/)｜[EPIC-KITCHENS](https://epic-kitchens.github.io/) | 放弃精确动作标注，换取**极低成本与超大规模**，用于学习视觉先验与高层行为结构，通常作为预训练数据 |

> 🌱 **新人怎么选**：如果只是想复现论文、验证算法，**优先用公开数据集**（见[基础设施篇](./infrastructure.md#datasets)），不要一上来就自建采集系统——搭一套能用的采集平台通常比训练一个策略更花时间。真要自己采，最低成本的起点是 [LeRobot](https://github.com/huggingface/lerobot) 生态的 SO-101 主从臂（整套千元级），先跑通「采 50 条 → 训练 → 评测」的闭环，再考虑扩展。

---

<section id="companies"></section>

## (7) Companies —— 公司与硬件生态

| 公司 | 主营产品 | 说明 |
|---|---|---|
| [松灵 AgileX](https://www.agilex.ai/) | [PIPER 六轴机械臂](https://global.agilex.ai/products/piper)<br>[PIKA 数采方案](https://global.agilex.ai/products/pika)<br>[Cobot Magic 双臂遥操作平台](https://global.agilex.ai/products/cobot-magic)<br>[全部产品（含移动底盘）](https://global.agilex.ai/collections/all) | 面向教育科研；[开源仓库](https://github.com/agilexrobotics) |
| [宇树 Unitree](https://www.unitree.com/cn) | [四足机器人开发指南](https://www.yuque.com/ironfatty/nly1un/luo9gb)<br>[Go2 机器狗](https://www.unitree.com/cn/go2)<br>[AlienGo 机器狗](https://www.yuque.com/ironfatty/nly1un/dqcz3u)<br>[通用人形 H1](https://www.unitree.com/cn/h1)<br>[通用人形 G1](https://www.unitree.com/cn/g1) | 许多产出使用宇树的机器人作为硬件基础 |
| [方舟无限 ARX](https://www.arx-x.com/?product/) | [X5 机械臂](https://www.arx-x.com/?product/21.html)<br>[X7 双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5 机械臂](https://www.arx-x.com/?product/22.html) | 适合复现很多经典工作，例如 [Mobile ALOHA](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin 松灵底盘 + 方舟臂](https://github.com/RoboTwin-Platform/RoboTwin) |
| [波士顿动力 Boston Dynamics](https://bostondynamics.com/) | [Spot 机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas 通用人形](https://bostondynamics.com/atlas/) | 具身智能本体制造商，从液压驱动转向电机驱动 |
| [灵心巧手](https://www.linkerbot.cn/index) | [Linker Hand L30（腱绳驱动）](https://www.linkerbot.cn/product?page=L30)<br>[Linker Hand L20（连杆驱动）](https://www.linkerbot.cn/product?page=L20) | 主攻各类灵巧手 |
| [灵巧智能 DexRobot](https://www.dex-robot.com/) | [Dexhand 021 灵巧手](https://www.dex-robot.com/productionDexhand) | 19 自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) | [GALBOT G1](https://www.galbot.com/g1) | 专注于具身智能多模态大模型通用机器人研发 |
| [星海图 Galaxea](https://galaxea.ai/) | [A1 六轴机械臂](https://galaxea.ai/A1)<br>[R1-Pro 仿人形机器人](https://galaxea.ai/R1-Pro) | 软硬件产品均自主研发，专注于打造「一脑多型」 |
| [World Labs](https://www.worldlabs.ai/) |  | 专注于空间智能，致力于打造大型世界模型（LWM），以感知、生成并与 3D 世界进行交互 |
| [星动纪元](https://www.robotera.com) | [Star1 人形](https://www.robotera.com/goods/1.html)<br>[XHAND1 灵巧手](https://www.robotera.com/goods/2.html) |  |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1 人形](https://boosterobotics.com/zh/store/) |  |
| [人形机器人（上海）有限公司](https://www.openloong.net/) | [青龙机器人](https://www.openloong.org.cn/cn) | 全尺寸通用人形机器人，提供开源硬件设计图纸、软件框架代码、算法包和全链仿真工具。 |
| [云深处科技](https://www.deeprobotics.cn/) | [绝影 X30 四足机器人](https://www.deeprobotics.cn/robot/index/product3.html)<br>[Dr.01 人形机器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | 具身智能仿真平台供应商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能数据平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [远征 A2 人形机器人](https://www.zhiyuan-robot.com/products/A2)<br>[远征 A2-W 轮式人形](https://www.zhiyuan-robot.com/products/A2_W)<br>[灵犀 X1 人形机器人](https://www.zhiyuan-robot.com/products/X1)<br>[精灵 G1 轮式人形](https://www.zhiyuan-robot.com/products/A2_D) |  |
| [NVIDIA](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://airbots.online/) | [TOK4 移动主从臂平台](https://airbots.online/products/tok4)<br>[MMK2 移动升降双臂平台](https://airbots.online/products/mmk2)<br>[AIRBOT Play 六轴机械臂](https://airbots.online/products/airbot-play) | [开发者文档](https://docs.airbots.online/) |
| [穹彻智能](https://www.noematrix.ai/) |  |  |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) |  |  |
| [具身风暴](https://www.robotstorm.tech) |  | 落地具身智能通用按摩机器人 |
| [众擎机器人](https://engineai.com.cn/) | [SE01](https://engineai.com.cn/product-se01.html)<br>[PM01](https://engineai.com.cn/product-pm01.html)<br>[T800](https://engineai.com.cn/product-t800.html) |  |
| [魔法原子](https://www.magiclab.top/) | [MagicBot](https://www.magiclab.top/human)<br>[MagicDog](https://www.magiclab.top/dog) |  |
| [帕西尼](https://www.paxini.com/) | [PX-6AX GEN2 触觉传感器](https://www.paxini.com/ax)<br>[DexH13 GEN2 灵巧手](https://www.paxini.com/dex)<br>[TORA-ONE 人形机器人](https://www.paxini.com/robot) |  |
