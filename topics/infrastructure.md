<h1 align="center">Embodied-AI-Guide<br>软件基础设施篇</h1>

> 这一章关注的不是「具体某个模型」，而是**支撑具身智能研究与系统落地的软件基础设施（Infrastructure）**。  
> 仿真器决定你能构建怎样的世界，基准集决定你如何比较方法优劣，数据集决定模型最终学到什么样的行为分布。它们共同构成了具身智能中**最容易被忽视、但最影响上限与复现性的部分**。

软件部分可以理解为三层，外加一层工具链：  
**Simulators（仿真环境）** 决定你能「跑什么物理世界」；**Benchmarks（评测基准）** 决定你用什么任务衡量方法优劣；**Datasets（数据集）** 决定你能训练出怎样的策略分布；最后的**工具链**则关系到你把策略接到环境上要付多少工程成本。建议优先跑通「一个仿真器 + 一个基准 + 一个数据集」的最小闭环，再逐步扩展到多平台与多模态。

<section id="simulators"></section>

## (1) Simulators —— 仿真器

仿真器是具身研究里最先要做的一个选择，也是最容易选错的一个——**换仿真器的迁移成本往往比换模型高得多**。好消息是，选型主要看两件事：**你做的是操作还是运动**，以及**你需要并行采样还是高保真渲染**。

| 你要做什么 | 推荐起点 | 原因 |
|---|---|---|
| 双臂/单臂操作，想尽快跑通全链路 | **SAPIEN 系**（RoboTwin 2.0、ManiSkill） | 装起来快、任务现成、有预采集数据，本指南[第 2 章教程](../README.md#robotwin)即基于此 |
| 四足 / 人形运动控制（RL） | **Isaac Lab** 或 **MuJoCo Playground** | GPU 上数千环境并行采样，RL 训练必需 |
| 需要精确接触动力学、做控制研究 | **MuJoCo** | 接触求解稳定，学术界事实标准 |
| 需要照片级渲染、大规模场景 | **Isaac Sim** | 基于 Omniverse 的光追渲染，Sim2Real 视觉差距更小 |
| 要和 ROS 打通、做移动机器人 | **Gazebo** | 与 ROS/ROS 2 深度集成，传感器插件生态成熟 |

> 🌱 **新人最常见的误区**：以为「物理越真实越好」。实际上早期最该优化的是**迭代速度**——一个能在十分钟内跑完一轮训练与评测的仿真环境，价值远高于一个物理完美但配置三天都跑不起来的环境。等你要做 Sim2Real 迁移时，再去关心接触参数与渲染保真度。

选型时的第一站推荐社区维护的仿真器 wiki：[Simulately](https://simulately.wiki/)，它按物理引擎、渲染、并行能力等维度做了横向对比。

| 仿真器 | 典型生态 / 对应基准与工具链 |
|---|---|
| IsaacGym | [legged-gym](https://github.com/leggedrobotics/legged_gym)<br>[parkour（含蒸馏与真机部署）](https://github.com/ZiwenZhuang/parkour)<br>[extreme-parkour](https://github.com/chengxuxin/extreme-parkour) |
| Isaac Sim | [BEHAVIOR-1K](https://behavior.stanford.edu/) + [OmniGibson（工具链）](https://github.com/StanfordVL/OmniGibson)<br>[ARNOLD](https://arnold-benchmark.github.io/)<br>[GarmentLab](https://garmentlab.github.io/)｜[DexGarmentLab](https://wayrise.github.io/DexGarmentLab/)<br>⚠️ 早期的 iGibson 已停止维护，新项目请直接用 OmniGibson |
| MuJoCo | [robosuite](https://robosuite.ai/docs/overview.html) + [robomimic（工具链）](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics](https://robotics.farama.org/)<br>[RoboCasa](https://github.com/robocasa/robocasa?tab=readme-ov-file)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| OmniSim | [平台](https://github.com/omnilink-tech/omnisim)<br>Apache-2.0 机器人仿真器，提供 URDF 导入、HTTP/MCP Agent 控制、Newton CPU/GPU 物理、合成数据与可复现实验基准；Windows 提供 beta 安装包，Linux 为源码构建，macOS 物理尚未验证 |
| SAPIEN | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin 2.0](https://github.com/RoboTwin-Platform/RoboTwin)｜[文档](https://robotwin-platform.github.io/doc/) |
| CoppeliaSim | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| PyBullet | [CALVIN](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| Genesis | [主页](https://genesis-embodied-ai.github.io/)<br>[代码](https://github.com/Genesis-Embodied-AI/genesis-world)（注意仓库已由 `Genesis` 更名为 `genesis-world`）<br>跨平台（NVIDIA / AMD / Apple），已支持 LiDAR、深度与触觉传感器 |
| SOFA | [框架](https://github.com/sofa-framework/sofa/)<br>常用于软体机器人仿真 |
| GenieSim | [框架](https://github.com/AgibotTech/genie_sim)<br>[评测与文档](http://agibot-world.com/sim-evaluation/docs) |
| Gazebo | [平台](https://gazebosim.org)<br>[Open Robotics 维护](https://openrobotics.org/)<br>与 ROS / ROS 2 深度集成，适合移动机器人、仓储物流等场景 |

教程：[Isaac 101（Blog）](https://axi404.top/tags/isaac%20101)

### (1.1) 正在发生的变化：物理后端在重新洗牌 ⭐

读 2024 年之前的教程时要注意，这一层最近换了一轮，**很多老教程里的安装命令已经跑不通了**：

- **IsaacGym 已被 Isaac Lab 取代**。经典的 legged-gym、parkour 等仓库仍基于 IsaacGym，可以读代码学思路，但新项目请直接用 [Isaac Lab](https://github.com/isaac-sim/IsaacLab)。Isaac Lab 目前 2.x 是稳定线，3.0 仍在 beta，且新的 Newton 后端尚未覆盖全部功能（可变形体、吸盘夹爪等仍需 PhysX），**追求可复现就留在 2.x**。
- **[Newton](https://github.com/newton-physics/newton)**：由 NVIDIA、Google DeepMind 与 Disney Research 共同贡献给 Linux Foundation 的开源物理引擎，基于 Warp 与 OpenUSD，2026 年已发布正式版。它把刚体、布料、颗粒等多种求解器收进同一框架，正在成为多个仿真器共同的物理底座。
- **[MuJoCo Warp](https://github.com/google-deepmind/mujoco_warp)**：MuJoCo 的 GPU 并行实现，相比早期的 MJX 在接触密集场景下快出一到两个数量级，MuJoCo Playground 已将其设为默认。注意两个限制：**自由度较高（约 60 以上）时性能会明显下降，且暂不支持自动微分**——需要求梯度时仍要用 MJX 的 JAX 实现。
- **[mjlab](https://github.com/mujocolab/mjlab)**：把 Isaac Lab 那套 manager-based 接口搬到 MuJoCo Warp 上，**不依赖 Isaac Sim，安装轻量**，是 2026 年人形 / 四足 RL 值得考虑的新选项。

> 🌱 一句话总结：**做操作看 SAPIEN / MuJoCo，做运动控制看 Isaac Lab / mjlab，物理后端正在向 Newton 与 MuJoCo Warp 收敛。** 选定后就别频繁换，迁移成本很高。

---

<section id="benchmarks"></section>

## (2) Benchmarks —— 基准集

基准集通常定义了三件事：**任务集合 + 评测协议 +（可选）参考实现**。它的价值是让不同方法在同一套任务与指标上可复现对比——**没有共同的基准，「我的方法更好」就只是一句话**。

读基准的成功率数字时，请务必同时确认三个前提，否则数字之间没有可比性：**(1) 训练用了多少条演示**、**(2) 评测跑了多少个 episode、用了几个随机种子**、**(3) 初始状态是固定的还是随机的**。同一个模型在这三项上换一种设置，成功率相差二三十个百分点是常事。

| 基准 | 链接 | 一句话定位 |
|---|---|---|
| RoboTwin 2.0 | [link](https://github.com/RoboTwin-Platform/RoboTwin)<br>[link](https://robotwin-platform.github.io/doc/) | 程序化生成双臂任务数据与 50 个双臂评测任务（偏「双臂 + 规模化生成」） |
| RoboDojo | [link](https://robodojo-benchmark.com/) | 同时提供仿真与真机任务，评测维度覆盖泛化、精度、长程与记忆（偏「统一评测」） |
| RMBench | [link](https://rmbench.github.io/) | 专门考察记忆能力的操作基准，任务按记忆复杂度分级（偏「记忆依赖任务」） |
| SimplerENV | [link](https://github.com/simpler-env/SimplerEnv) | 轻量化、可快速对比策略在操作任务上的表现 |
| LIBERO | [link](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[link](https://libero-project.github.io/intro.html) | 程序化生成管道 + 终身学习设置（偏「终身/顺序学习」）；是 VLA 论文最常报的数字，但已接近饱和 |
| LIBERO-Plus | [link](https://arxiv.org/abs/2510.13626) | 给 LIBERO 加七类扰动、扩成上万任务并分五档难度，用来检验成功率是不是「刷」出来的 |
| VLA-Arena | [link](https://arxiv.org/abs/2512.22539) | 在静态桌面任务之外补上动态场景与安全约束 |
| RoboArena | [link](https://robo-arena.github.io/)<br>[paper](https://arxiv.org/abs/2506.18123) | **真机分布式评测**：不统一任务，由多所机构的评测者自选场景做双盲两两对比再聚合排名 |
| CALVIN | [link](https://github.com/mees/calvin)<br>[link](http://calvin.cs.uni-freiburg.de/) | 语言条件 + 多模态输入 + 长视野操纵（偏「长程任务与规划」） |
| Meta-World | [link](https://meta-world.github.io/) | 50 个操作任务，经典多任务/元强化学习基准（偏「多任务泛化」） |
| Embodied Agent Interface | [link](https://embodied-agent-interface.github.io/) | 评测 LLM 在具身决策链路（理解/分解/序列化）上的能力，不涉及低层执行 |
| RoboGen | [link](https://github.com/Genesis-Embodied-AI/RoboGen)<br>[link](https://robogen-ai.github.io/) | 生成任务/场景/带标注数据（偏「生成数据而非直接生成 policy」） |
| RescueBench | [repo](https://github.com/UnrealZoo/RescueBench)｜[paper](https://arxiv.org/abs/2606.01848) | 基于 Unreal Engine / UnrealZoo 的四阶段搜救基准，含五级难度与统一评测（偏「多模态探索、救援交互与空间记忆」） |

> 🌱 **怎么报结果才可信**：2026 年的共识是**至少报一个仿真基准 + 一个真机或第三方榜单**。只报单一仿真数字越来越难被接受，因为老基准已经出现明显的饱和与过拟合。相关讨论见[算法篇的「评测正在变严」](./algorithm.md#vla)。

---

<section id="datasets"></section>

## (3) Datasets —— 数据集

数据集决定了策略的「经验分布」——模型最终只会做它在数据里见过的事。挑数据集时建议先问四个问题：  
**(1) 真实还是仿真**（决定有没有 Sim2Real Gap）、**(2) 机器人同构还是异构**（同构好训，异构才谈得上跨本体泛化）、**(3) 有哪些模态**（RGB / RGB-D / 语言 / 触觉 / 声音）、**(4) 有没有配套的训练代码与采集流程**（决定你能不能复现，而不只是下载）。

| 数据集 | 链接 | 关键特点（紧凑版） |
|---|---|---|
| Open X-Embodiment（RT-X） | [link](https://robotics-transformer-x.github.io/) | 22 种机器人平台、百万级真实轨迹，覆盖大量技能与任务（大规模、跨本体） |
| AgiBot World Datasets（智元） | [link](https://agibot-world.com/) | 百万级轨迹、同构机器人采集、多级质检与人工在环流程（工业化采集流程） |
| RoboMIND | [link](https://x-humanoid-robomind.github.io/) | 10.7 万真实演示、96 类物体、四种协作臂、任务按类别组织（真实多任务） |
| ARIO（All Robots in One） | [link](https://imaei.github.io/project_pages/ario/) | 2D/3D/文本/触觉/声音五模态；操作 + 导航；仿真 + 真实；统一格式且规模大 |
| MimicGen | [link](https://github.com/NVlabs/mimicgen)<br>[link](https://mimicgen.github.io/) | 基于 robosuite + MuJoCo 的数据生成框架；少量真人演示扩增为大量仿真数据 |
| RoboCasa | [link](https://github.com/robocasa/robocasa)<br>[link](https://robocasa.ai/) | MuJoCo 厨房高保真平台；多环境多物体；原子任务 + 组合任务（偏家居厨房） |
| DexMimicGen | [link](https://github.com/NVlabs/dexmimicgen/)<br>[link](https://dexmimicgen.github.io/) | 面向双臂桌面操作；增强版 Real2Sim2Real 数据生成；少量演示生成大量轨迹 |
| FUSE Dataset | [link](https://fuse-model.github.io/) | 遥操作轨迹；语言指令 + 复杂遮挡；多任务设置（多传感器融合研究友好） |
| BiPlay Dataset | [link](https://dit-policy.github.io/) | 双臂轨迹；随机物体与背景；长视频切片成带语言描述的剪辑（泛化导向） |
| DROID | [link](https://droid-dataset.github.io/) | 7.6 万轨迹、350 小时、564 场景、86 任务；附硬件与训练代码（真实大规模） |
| BridgeData V2 | [link](https://rail-berkeley.github.io/bridgedata/) | 6 万轨迹；多环境多技能；目标图像/语言指令；包含遥操作与脚本执行 |
| Ego4D Sounds | [link](https://ego4dsounds.github.io/) | 第一人称视频 + 环境声音；强调动作与声音对齐（声音模态很有价值） |
| RH20T | [link](https://rh20t.github.io/) | 人机交互数据；含人脸与语音等敏感信息；体量大且提供缩减版（注意隐私与合规） |
| 白虎数据集 | [link](https://www.openloong.org.cn/cn/) | 异构机器人；多场景多任务；面向跨平台评测与训练（本体覆盖面广） |
| RoboTwin 2.0 Dataset | [link](https://robotwin-platform.github.io/doc/usage/collect-data.html) | 10 万条以上仿真轨迹；50 个双臂任务；clean / randomized 两档域随机化；可按任务单独下载 |

---

<section id="policy-serving"></section>

## (4) 工具链 —— 数据格式与策略部署

前三节解决的是「在哪跑、比什么、用什么数据训」，还剩一件很占时间但不太被写进论文的事：**把一个策略真正接到环境上跑起来**。麻烦主要来自不统一——每个模型的依赖库、观测格式、动作空间都不一样，换一个仿真器常常要重写一遍胶水代码。下面两个项目分别从「统一数据格式」和「统一部署接口」两个角度减少这部分工作量。

| 项目 | 链接 | 一句话定位 |
|---|---|---|
| LeRobot | [repo](https://github.com/huggingface/lerobot)｜[文档](https://huggingface.co/docs/lerobot/) | Hugging Face 的机器人学习栈，提供统一的数据集格式和多个策略的训练代码；它的数据格式目前基本是通用底座 |
| XPolicyLab | [repo](https://github.com/XPolicyLab/XPolicyLab) | 把多个策略收敛到同一套部署接口，策略与环境可以各用自己的依赖环境、跨机器通信；适合在同一批任务上横向对比多个模型 |

LeRobot 的策略库已经相当全（π0 / π0.5 / π0-FAST、SmolVLA、GR00T、X-VLA、WALL-X 等），另外三个功能对实际项目很有用：

- **LoRA / PEFT 微调**已是一等公民（[文档](https://huggingface.co/docs/lerobot/main/en/peft_training)），显存不够时不必放弃微调大基座；
- **Real-Time Chunking（RTC）** 可以作为开关加在任意 flow matching 策略上，用于缓解推理延迟；
- 支持从 Hugging Face Hub 直接加载仿真环境，省去本地配置。

> ⚠️ LeRobot 迭代很快，**升级版本时请先看 release note**：例如它已移除对 GR00T N1.5 的支持、只保留 N1.7，旧 checkpoint 需要锁定老版本才能加载。这类破坏性变更在本领域的工具链里相当常见。
>
> 🌱 新手不必一开始就纠结这一层。只跑一个策略时，直接用该策略仓库自带的脚本最省事；等你需要**在同一套任务上比较多个模型**，或者撞上「策略要一个 torch 版本、仿真器要另一个」这类依赖冲突时，再回来看它们的价值会明显得多。
