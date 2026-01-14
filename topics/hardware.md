<h1 align="center">Embodied-AI-Guide<br>硬件篇</h1>

> 具身智能硬件涵盖多个技术栈：嵌入式软硬件、机械设计、机器人系统集成与传感器等。它们知识面很杂，但共同目标只有一个：把“算法”变成真实世界里稳定可复现的系统。  
> 关于硬件学习，最有效的方式几乎永远是 **从实践出发**：先做出一个能跑起来的最小系统，再逐步扩展复杂度与可靠性。

<section id="embedded"></section>

## (1) Embedded —— 嵌入式

嵌入式决定了机器人“神经系统”的下限：通信是否稳定、控制是否实时、驱动是否安全。建议按 **入门单片机 → STM32 工程 → 电机驱动 → 嵌入式 Linux** 的顺序推进。

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
做具身硬件时，嵌入式的价值不在“写出更炫的代码”，而在“系统能稳定跑、延迟可控、驱动可靠”。很多项目后期的崩溃都不是算法问题，而是控制链路与工程细节问题。

---

<section id="mechanical"></section>

## (2) Mechanical Design —— 机械设计

机械设计决定了机器人“身体”的能力边界：可达空间、刚度、负载、布线与维护成本等。对于算法同学来说，机械最关键的产出通常是 **可制造的 CAD** 与 **可用于仿真/控制的 URDF**。

| 主题 | 资源 | 链接 | 说明 |
|---|---|---|---|
| CAD 入门 | SolidWorks 教学 | [link](https://www.bilibili.com/video/BV1iw411Z7HZ) | 面向装配体与工程制图 |
| 工程衔接 | 从 SolidWorks 生成 URDF | [link](https://blog.csdn.net/weixin_45168199/article/details/105755388) | 用装配体导出机器人模型并进入仿真/控制 |

---

<section id="robosystem"></section>

## (3) Robot System Design —— 机器人系统设计

系统设计关注的是“把多个模块拼成一个可维护系统”：硬件接口、软件架构、标定流程、调试策略、日志与安全机制。建议把系统设计当作“把机器人做成产品”的第一步。

| 资源 | 链接 | 说明 |
|---|---|---|
| 《机器人学简介》（教材 PDF） | [link](./files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf) | 质量高，适合系统性阅读 |
| Robotic Systems（Illinois） | [link](https://motion.cs.illinois.edu/RoboticSystems/) | 偏“系统化机器人学”的组织方式 |

---

<section id="sensors"></section>

## (4) Sensors —— 传感器

具身系统里常见传感器包括相机、深度相机、IMU、力/力矩、触觉等。建议从“能直接用于闭环”的传感器开始（相机/深度/IMU），再逐步引入触觉等高难度模态。

### (4.1) 深度相机（Depth Camera）

| 设备/生态 | 链接 | 说明 |
|---|---|---|
| RealSense + ROS | [link](https://github.com/IntelRealSense/realsense-ros/tree/ros1-legacy) | 工程中常见深度相机生态 |

---

<section id="tactile"></section>

## (5) Tactile Sensing —— 触觉感知（接触、力与精细操作）

触觉是“接触世界”的关键模态，尤其在装配、柔性物体、精细抓取和遮挡严重的场景中，触觉往往比视觉更可靠。整体上触觉硬件路线常见两类：**视触觉（Vision-based tactile）** 与 **电子皮肤（E-skin）**。

### (5.1) 视触觉传感器（Vision-Based Tactile Sensors）

视触觉通过摄像头观测弹性介质/标记点的形变，把“触觉”转化为视觉信号来估计接触力、形变与接触几何。它的关键设计点通常包括：传感器形状、标记点布局、材料（硅胶/弹性体）以及光照与成像系统。

- 优点：高分辨率、非侵入、易与视觉系统融合  
- 缺点：依赖视觉计算、易受光照影响、光学与封装设计复杂

两篇综述覆盖“算法视角”和“结构视角”，建议作为起点：  
算法综述：[link](https://ieeexplore.ieee.org/document/10563188)  
结构综述：[link](https://link.springer.com/article/10.1007/s10846-021-01431-0)

### (5.2) 电子皮肤（Electronic Skin）

电子皮肤通常用柔性材料（压力薄膜、纳米传感网络等）实现大面积触觉，目标是让机器人拥有类似“全身触觉”的能力，用于安全、人机协作与全身接触交互。

- 优点：可大面积覆盖、高灵敏度、可伸缩适配复杂表面  
- 缺点：制造与成本较高、数据规模大带来处理挑战、长期稳定性与漂移问题

综述入口：[link](https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00049)

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

### (5.4) 传感器购买（从研究到落地）

市面上已有成熟视触觉传感器产品，例如 GelSight：[link](https://gelsight.com/)

---

<section id="data_collection"></section>

## (6) Data Collection —— 数据采集硬件

| 采集范式                          | 代表系统 / 资源                | 链接                                                                                              | 动机与特点                                                                            |
| ----------------------------- | ------------------------ | ----------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 双臂遥操作（Teleoperation）          | ALOHA                    | [video](https://www.bilibili.com/video/BV1vU421d7BJ/?spm_id_from=333.337.search-card.all.click) | 通过主从机械臂映射，直接采集**高精度 action + 多视角观测**，动机是为复杂 manipulation（双臂、装配、工具）提供可直接用于控制学习的数据 |
| 第一人称数据（Ego-centric Video）     | Ego-centric Manipulation | —                                                                                               | 放弃精确动作标注，换取**低成本与大规模**，主要动机是学习人类操作的视觉先验与高层行为结构                                   |
| 可穿戴示教（Wearable / Retargeting） | UMI                      | [video](https://www.bilibili.com/video/BV17w4m1f7Ti/?spm_id_from=333.337.search-card.all.click) | 直接利用人体动作进行示教，强调**示教效率与自然性**，需要额外的动作映射（retargeting）                               |
| 数据采集手套（Data Gloves）           | 手部动作采集                   | [Zhihu](https://zhuanlan.zhihu.com/p/635065768)                                                 | 面向灵巧手与精细操作，动机是**缩小人手与机器人手之间的表示差距**，常用于 in-hand manipulation                      |


<section id="companies"></section>

## (7) Companies —— 公司与硬件生态

| 公司 | 主营产品 | Others |
|---|---|---|
| [松灵 AgileX](https://www.agilex.ai/) | [pipper 六轴机械臂](https://www.agilex.ai/chassis/16)<br>[PIKA 数采方案](https://www.agilex.ai/chassis/22)<br>[Cobot Magic 双臂遥操作平台](https://www.agilex.ai/chassis/27)<br>移动底盘 | 面向教育科研 |
| [宇树 Unitree](https://www.unitree.com/cn) | [四足机器人开发指南](https://www.yuque.com/ironfatty/nly1un/luo9gb)<br>[Go2 机器狗](https://www.unitree.com/cn/go2)<br>[AlienGo 机器狗](https://www.yuque.com/ironfatty/nly1un/dqcz3u)<br>[通用人形 H1](https://www.unitree.com/cn/h1)<br>[通用人形 G1](https://www.unitree.com/cn/g1) | 许多产出使用宇树的机器人作为硬件基础 |
| [方舟无限 ARX](https://www.arx-x.com/?product/) | [X5 机械臂](https://www.arx-x.com/?product/21.html)<br>[X7 双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5 机械臂](https://www.arx-x.com/?product/22.html) | 适合复现很多经典工作，例如 [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin 松灵底盘 + 方舟臂](https://github.com/TianxingChen/RoboTwi) |
| [波士顿动力 Boston Dynamics](https://bostondynamics.com/) | [Spot 机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas 通用人形](https://bostondynamics.com/atlas/) | 具身智能本体制造商，从液压驱动转向电机驱动 |
| [灵心巧手](https://www.linkerbot.cn/index) | [Linker Hand L30（健绳驱动）](https://www.linkerbot.cn/product?page=L30)<br>[Linker Hand L20（连杆驱动）](https://www.linkerbot.cn/product?page=L20) | 主攻各类灵巧手 |
| [灵巧智能 DexRobot](https://www.dex-robot.com/) | [Dexhand 021 灵巧手](https://www.dex-robot.com/productionDexhand) | 19 自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) | [GALBOT G1](https://www.galbot.com/g1) | 专注于具身智能多模态大模型通用机器人研发 |
| [星海图 Galaxea](https://galaxea.ai/) | [A1 六轴机械臂](https://galaxea.ai/A1)<br>[R1-Pro 仿人形机器人](https://galaxea.ai/R1-Pro) | 软硬件产品均自主研发，专注于打造“一脑多型” |
| [World Labs](https://www.worldlabs.ai/) |  | 专注于空间智能，致力于打造大型世界模型（LWM），以感知、生成并与 3D 世界进行交互。<br>[相关介绍](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1 人形](https://www.robotera.com/goods/1.html)<br>[XHAND1 灵巧手](https://www.robotera.com/goods/2.html) |  |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1 人形](https://boosterobotics.com/zh/store/) |  |
| [人形机器人（上海）有限公司](https://www.openloong.net/) | [青龙机器人](https://www.openloong.org.cn/cn) | 全尺寸通用人形机器人，提供开源硬件设计图纸、软件框架代码、算法包和全链仿真工具。 |
| [云深处科技](https://www.deeprobotics.cn/) | [绝影 X30 四足机器人](https://www.deeprobotics.cn/robot/index/product3.html)<br>[Dr.01 人形机器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | 具身智能仿真平台供应商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能数据平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [远征 A2 人形机器人](https://www.zhiyuan-robot.com/products/A2)<br>[远征 A2-W 轮式人形](https://www.zhiyuan-robot.com/products/A2_W)<br>[灵犀 X1 人形机器人](https://www.zhiyuan-robot.com/products/X1)<br>[精灵 G1 轮式人形](https://www.zhiyuan-robot.com/products/A2_D) |  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://airbots.online/) | [TOK2 移动主从臂平台](https://airbots.online/zh/tok)<br>[MMK2 移动升降双臂平台](https://airbots.online/zh/mmk2)<br>Play 六轴机械臂 |  |
| [穹彻智能](https://www.noematrix.ai/) |  |  |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) |  |  |
| [具身风暴](https://www.robotstorm.tech) |  | 落地具身智能通用按摩机器人 |
| [众擎机器人](https://engineai.com.cn/) | [SE 01](https://engineai.com.cn/product_one)<br>[PM 01](https://engineai.com.cn/product_fore) |  |
| [魔法原子](https://www.magiclab.top/) | [MagicBot](https://www.magiclab.top/human)<br>[MagicDog](https://www.magiclab.top/dog) |  |
| [帕西尼](https://www.paxini.com/) | [PX-6AX GEN2 触觉传感器](https://www.paxini.com/ax/gen2)<br>[DexH13 GEN2 灵巧手](https://www.paxini.com/dex/gen2)<br>[TORA-ONE 人形机器人](https://www.paxini.com/robot) |  |
