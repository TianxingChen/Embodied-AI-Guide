<h1 align="center">Embodied-AI-Guide<br>软件基础设施篇</h1>

> 这一章关注的不是“具体某个模型”，而是**支撑具身智能研究与系统落地的软件基础设施（Infrastructure）**。  
> 仿真器决定你能构建怎样的世界，基准集决定你如何比较方法优劣，数据集决定模型最终学到什么样的行为分布。它们共同构成了具身智能中**最容易被忽视、但最影响上限与复现性的部分**。

软件部分可以理解为三层：  
**Simulators（仿真环境）** 决定你能“跑什么物理世界”；**Benchmarks（评测基准）** 决定你用什么任务衡量方法优劣；**Datasets（数据集）** 决定你能训练出怎样的策略分布。建议优先跑通“一个仿真器 + 一个基准 + 一个数据集”的最小闭环，再逐步扩展到多平台与多模态。

<section id="simulators"></section>

## (1) Simulators - 仿真器

常见仿真器 wiki：[link](https://simulately.wiki/)

| 仿真器 | 典型生态 / 对应基准与工具链 |
|---|---|
| IsaacGym | legged-gym：[link](https://github.com/leggedrobotics/legged_gym)<br>parkour（含蒸馏与真机部署）：[link](https://github.com/ZiwenZhuang/parkour)<br>extreme-parkour：[link](https://github.com/chengxuxin/extreme-parkour) |
| IsaacSim | BEHAVIOR-1K：[link](https://behavior.stanford.edu/behavior-1k) + OmniGibson（工具链）：[link](https://behavior.stanford.edu/omnigibson/)<br>ARNOLD：[link](https://arnold-benchmark.github.io/)<br>GarmentLab：[link](https://garmentlab.github.io/) / DexGarmentLab：[link](https://wayrise.github.io/DexGarmentLab/) |
| MuJoCo | robosuite：[link](https://robosuite.ai/docs/overview.html) + robomimic（工具链）：[link](https://robomimic.github.io/)<br>LIBERO：[link](https://libero-project.github.io/main.html)<br>MetaWorld：[link](https://meta-world.github.io/)<br>Gymnasium-Robotics：[link](https://robotics.farama.org/)<br>RoboCasa：[link](https://github.com/robocasa/robocasa?tab=readme-ov-file)<br>RoboHive：[link](https://github.com/vikashplus/robohive) |
| SAPIEN | ManiSkill：[link](https://maniskill.readthedocs.io/en/latest/index.html)<br>RoboTwin：[link](https://github.com/TianxingChen/RoboTwin) |
| CoppeliaSim | RLBench：[link](https://github.com/stepjam/RLBench)<br>PerAct2：[link](https://bimanual.github.io/)<br>COLOSSEUM：[link](https://robot-colosseum.github.io/) |
| PyBullet | CALVIN：[link](https://github.com/mees/calvin?tab=readme-ov-file)<br>Ravens：[link](https://github.com/google-research/ravens)<br>VimaBench：[link](https://github.com/vimalabs/VimaBench) |
| Genesis | 入口：[link](https://genesis-embodied-ai.github.io/) |
| SOFA | 框架：[link](https://github.com/sofa-framework/sofa/)<br>常用于软体机器人仿真 |
| GenieSim | 框架：[link](https://github.com/AgibotTech/genie_sim)<br>评测与文档：[link](http://agibot-world.com/sim-evaluation/docs) |
| Gazebo | 平台：[link](https://gazebosim.org)<br>Open Robotics 维护：[link](https://openrobotics.org/)<br>与 ROS / ROS 2 深度集成，适合移动机器人、仓储物流等场景 |

教程：Isaac 101（Blog）：[link](https://axi404.top/tags/isaac%20101)

---

<section id="benchmarks"></section>

## (2) Benchmarks - 基准集

基准集通常定义了：**任务集合 + 评测协议 +（可选）参考实现**。它们的价值是让不同方法在同一套任务与指标上可复现对比。下面列的是你当前条目中最常见、且各自定位清晰的基准。

| 基准 | 链接 | 一句话定位 |
|---|---|---|
| RoboTwin 2.0 | [link](https://github.com/robotwin-Platform/RoboTwin) | 程序化生成双臂任务数据与 50 个双臂评测任务（偏“双臂+规模化生成”） |
| SimplerENV | [link](https://github.com/simpler-env/SimplerEnv) | 轻量化、可快速对比策略在操作任务上的表现 |
| LIBERO | [link](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[link](https://libero-project.github.io/intro.html) | 程序化生成管道 + 视觉运动策略架构与终身学习设置（偏“终身/顺序学习”） |
| CALVIN | [link](https://github.com/mees/calvin)<br>[link](http://calvin.cs.uni-freiburg.de/) | 语言条件 + 多模态输入 + 长视野操纵（偏“长程任务与规划”） |
| Meta-World | [link](https://meta-world.github.io/) | 50 操作任务，经典多任务/元强化学习基准（偏“多任务泛化”） |
| Embodied Agent Interface | [link](https://embodied-agent-interface.github.io/) | 评测 LLM 在具身决策链路（理解/分解/序列化），不强调低层执行 |
| RoboGen | [link](https://github.com/Genesis-Embodied-AI/RoboGen)<br>[link](https://robogen-ai.github.io/) | 生成任务/场景/带标注数据（偏“生成数据而非直接生成 policy”） |

---

<section id="datasets"></section>

## (3) Datasets - 数据集

数据集决定了策略的“经验分布”。阅读数据集时建议关注四件事：  
**(1) 真实 vs 仿真**、**(2) 机器人同构 vs 异构**、**(3) 模态（RGB/RGB-D/语言/触觉/声音等）**、**(4) 是否附带训练代码与硬件搭建/采集流程**。下面把你的条目统一成一个紧凑表，避免过长的散点描述。

| 数据集 | 链接 | 关键特点（紧凑版） |
|---|---|---|
| Open X-Embodiment（RT-X） | [link](https://robotics-transformer-x.github.io/) | 22 种机器人平台、百万级真实轨迹，覆盖大量技能与任务（大规模、跨本体） |
| AgiBot World Datasets（智元） | [link](https://agibot-world.com/) | 百万级轨迹、同构机器人采集、多级质检与人工在环流程（工业化采集流程） |
| RoboMIND | [link](https://x-humanoid-robomind.github.io/) | 10.7 万真实演示、96 类物体、四种协作臂、任务按类别组织（真实多任务） |
| ARIO（All Robots in One） | [link](https://imaei.github.io/project_pages/ario/) | 2D/3D/文本/触觉/声音五模态；操作+导航；仿真+真实；统一格式且规模大 |
| MimicGen | [link](https://github.com/NVlabs/mimicgen)<br>[link](https://mimicgen.github.io/) | 基于 robosuite+MuJoCo 的数据生成框架；少量真人演示扩增为大量仿真数据 |
| RoboCasa | [link](https://github.com/robocasa/robocasa)<br>[link](https://robocasa.ai/) | MuJoCo 厨房高保真平台；多环境多物体；原子任务+组合任务（偏家居厨房） |
| DexMimicGen | [link](https://github.com/NVlabs/dexmimicgen/)<br>[link](https://dexmimicgen.github.io/) | 面向双臂桌面操作；增强版 real2sim2real 数据生成；少量演示生成大量轨迹 |
| FUSE Dataset | [link](https://fuse-model.github.io/) | 远程操控轨迹；语言指令 + 复杂遮挡；多任务设置（多传感器融合研究友好） |
| BiPlay Dataset | [link](https://dit-policy.github.io/) | 双臂轨迹；随机物体与背景；长视频切片成带语言描述的剪辑（泛化导向） |
| DROID | [link](https://droid-dataset.github.io/) | 7.6 万轨迹、350 小时、564 场景、86 任务；附硬件与训练代码（真实大规模） |
| BridgeData V2 | [link](https://rail-berkeley.github.io/bridgedata/) | 6 万轨迹；多环境多技能；目标图像/语言指令；包含远程操控与脚本执行 |
| Ego4D Sounds | [link](https://ego4dsounds.github.io/) | 第一人称视频 + 环境声音；强调动作与声音对齐（声音模态很有价值） |
| RH20T | [link](https://rh20t.github.io/) | 人机交互数据；含人脸与语音等敏感信息；体量大且提供缩减版（注意隐私与合规） |
| 白虎数据集 | [link](https://www.openloong.org.cn/cn/dataset) | 异构机器人；多场景多任务；面向跨平台评估与训练（本体覆盖面广） |
