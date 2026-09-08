![](./files/Embodied-AI-Guide-logo.png)

<h1 align="center">具身智能技术指南 Embodied-AI-Guide</h1>

<p align="center">
  <b>国内最热门的具身智能技术指南</b><br>
  一份偏「百科全书」定位的具身智能中文知识库与资料索引
</p>

<p align="center">
  <a href="#start">从这里开始</a> ·
  <a href="#robotwin">动手学习</a> ·
  <a href="#info">认知资料</a> ·
  <a href="#algorithm">算法篇</a> ·
  <a href="#infrastructure">基础设施篇</a> ·
  <a href="#control">控制篇</a> ·
  <a href="#hardware">硬件篇</a>
</p>

<p align="center"><img src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide?style=flat-square" alt="GitHub repo stars" height="20"/>  <img src="https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FTianxingChen%2FEmbodied-AI-Guide&label=Total%20Visitors&labelColor=%232ccce4&countColor=%23d9e3f0" alt="Visitors" height="20"/>  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square" alt="PRs Welcome" height="20"/>  <img src="https://img.shields.io/badge/License-Non--Commercial-blue?style=flat-square" alt="License" height="20"/></p>

> 📚 本项目希望帮助新人**快速建立领域认知**：以一个实践项目带大家动手入门具身智能，同时以百科全书的形式梳理当前具身智能涉及的主要技术，让大家清楚不同技术能解决什么问题，未来想深入时有头绪。
>
> 欢迎 **Star / 分享 / 提 PR**。合作与交流可邮件联系 [lumina.embodiedai@gmail.com](mailto:lumina.embodiedai@gmail.com)，或添加[项目发起人](https://tianxingchen.github.io/)微信 `TianxingChen_2002`（请备注：机构 + 姓名 + 来意）。

### 📢 News｜项目进展

📷 *2026-01-15: Embodied-AI-Guide 完成内容重组*<br>
⭐️ *2025-12-18: GitHub Stars 突破 10,000*<br>
❤️ *2025-03-15: Embodied-AI-Guide 正式开源*

### 🧑‍💻 Related Projects｜相关开源项目

⭐️ Lumina Call（具身智能招聘）：[Website](https://lumina-embodied.ai/lumina-call)<br>
⭐️ Datawhale Easy-Embodied（具身智能入门教程）：[Repo](https://github.com/datawhalechina/every-embodied)

## 🦉 Lumina 具身智能社区

社区主页：[lumina-embodied.ai](https://lumina-embodied.ai)｜扫描下方二维码即可加入社区交流群：

![Lumina 具身智能社区](./files/images/Lumina.png)

<a id="start"></a>

## 🐣 (1) Start From Here - 从这里开始

> 具身智能是指一种基于物理实体进行感知和行动的智能系统，其通过智能体与环境的交互获取信息、理解问题、做出决策并实现行动，从而产生智能行为和适应性。

### (1.1) How - 如何使用这份指南

本项目的设计理念是「一条主线 + 一张全景图」：

- **一条主线**：用[第 2 章](#robotwin)的实践教程，让你在一周内亲手跑通一个操作策略的完整流程；
- **一张全景图**：用[第 3 ~ 7 章](#info)以百科全书的形式覆盖算法、基础设施、控制与硬件，帮助你判断每项技术解决什么问题、值不值得深入。

建议的阅读顺序：**先动手跑通第 2 章，再按兴趣检索后续章节**，不必按顺序通读。

### (1.2) 学习路线建议（按背景选择起点）

不同背景的读者不必从同一处入手，可参考下表选择起点：

| 你的背景                | 建议起点                    | 推荐路径                                               |
| ------------------- | ----------------------- | -------------------------------------------------- |
| 完全新手 / 在校本科生        | [第 2 章](#robotwin) 动手教程 | (2) 跑通流程 → (3) 建立认知 → (4) 算法篇 → 按兴趣深入              |
| 有 CV / NLP / 深度学习基础 | [第 4 章](#algorithm) 算法篇 | (4) 重点看 Robot Learning 与 VLA → (5) 基础设施 → (2) 动手验证 |
| 有自动化 / 机器人学背景       | [第 4 章](#algorithm) 算法篇 | (3) 了解版图 → (4) 补齐学习与决策 → (5) 熟悉仿真与数据生态             |
| 偏硬件 / 嵌入式           | [第 7 章](#hardware) 硬件篇  | (7) 硬件篇 → (6) 控制篇 → (2) 动手教程                       |
| 想快速了解行业与选题          | [第 3 章](#info) 认知资料     | (3.1) 方法论 → (3.5) 论文列表 → (3.6) 年度趋势                |

### (1.3) 术语速查表

阅读论文与本指南时高频出现的概念，先建立字面认知即可，细节留给对应章节。

<details>
<summary><b>展开术语速查表（20 条）</b></summary>

| 术语                              | 一句话解释                               |
| ------------------------------- | ----------------------------------- |
| **Manipulation / Locomotion**   | 操作（用手臂改变环境）与移动（用腿或轮子移动本体），具身智能的两条主线 |
| **Policy（策略）**                  | 从观测到动作的映射，也就是日常所说的「模型」              |
| **IL / BC（模仿学习 / 行为克隆）**        | 从人类演示数据中以监督方式学习动作                   |
| **RL（强化学习）**                    | 通过与环境交互并依据奖励信号来优化策略                 |
| **VLA（Vision-Language-Action）** | 直接把图像与语言指令映射为机器人动作的端到端模型            |
| **VA（Vision-Action）**           | 只用视觉、不接受语言指令的策略；任务固定时比 VLA 更轻更快      |
| **World Model（世界模型）**          | 学习「当前状态 + 动作 → 下一步观测」的模型，可用来在脑内推演      |
| **WAM（World-Action Model）**     | 先用世界模型预测接下来会看到什么，再从预测中解出动作的一类策略       |
| **Teleoperation（遥操作）**          | 人通过手柄、动捕或主从设备操控机器人，是真机数据采集的主要手段     |
| **Demonstration（演示 / 轨迹）**      | 一次完整的任务执行记录，通常包含观测、动作与时间戳           |
| **Sim2Real Gap**                | 仿真与真实世界在物理、渲染、噪声上的差异，会导致策略迁移掉点      |
| **Real2Sim**                    | 把真实场景与物体重建进仿真，用于缩小 Sim2Real Gap     |
| **Affordance（可操作性）**            | 物体上「可以被怎样操作」的区域或方式，如把手可抓、按钮可按       |
| **DoF（自由度）**                    | 机器人可独立运动的关节数量                       |
| **End-effector（末端执行器）**         | 机械臂末端的执行部件，如夹爪、吸盘、灵巧手               |
| **FK / IK（正 / 逆运动学）**           | 由关节角求末端位姿 / 由末端位姿反解关节角              |
| **URDF**                        | 描述机器人连杆、关节与惯量的 XML 格式，是仿真与控制的通用输入   |
| **MPC（模型预测控制）**                 | 在滚动时域内反复求解优化问题来生成控制量                |
| **WBC（全身控制）**                   | 把控制目标从机械臂末端扩展到躯干、腿、头等整个身体，人形机器人方向常用  |
| **SLAM**                        | 同时定位与建图，让机器人知道「自己在哪、周围长什么样」         |

</details>

### (1.4) About Us - 关于我们

我们是一个由具身智能初学者组成的团队，希望以自己的学习经验为后来者提供帮助，加快具身智能的普及。欢迎更多朋友加入项目，也欢迎交友与学术合作。有任何问题可联系邮箱 [chentianxing2002@gmail.com](mailto:chentianxing2002@gmail.com)。

![Contributors](https://contrib.rocks/image?repo=TianxingChen/Embodied-AI-Guide)

<a id="robotwin"></a>

## ⚒️ (2) 动手学习具身智能操作

> **目标**：以 **RoboTwin 2.0** 为例，完整走通一次操作策略的「生命周期」——读论文建立认知、装环境、拿数据、训练 ACT、跑评测。这条链路本身是通用的，换成别的平台也是同样几步。
>
> **前置条件**：一块显存不低于 16GB 的显卡（ACT 训练约需 12GB）。官方建议数据采集与策略评测**避开 A / H / V 系列显卡**，详见 [Common Issue](https://robotwin-platform.github.io/doc/common-issue/)。

### (2.1) 为什么选择这个教程

具身智能操作是一个复杂的系统问题，可以拆成三个核心环节：

- **数据从哪来**：常见来源包括真机采集、人类视频、仿真合成与世界模型合成，各有短板——真机采集成本高、人类视频信息含量低、仿真合成面临 Sim2Real Gap 与 Scale-up 难题、世界模型合成存在幻觉；
- **策略怎么设计**：网络架构的选择直接影响模型表现、收敛效果与推理速度；
- **怎么评测性能**：没有科学的评测，就无法判断模型好坏，也难以推动技术进步。

面对以上问题，[RoboTwin 2.0](https://robotwin-platform.github.io/)（ICML 2026）提供了一个很好的学习平台。它基于易配置的 [SAPIEN](https://sapien.ucsd.edu/) 仿真平台开发，提供 50 个双臂任务的自动化数据合成与统一评测系统，并已开源 **10 万条以上预采集轨迹**——这意味着新手可以跳过最耗时的数据采集环节，直接从训练开始。

需要注意的是，策略侧的代码现在放在 [XPolicyLab](https://github.com/XPolicyLab/XPolicyLab) 这个子模块里，训练和评测脚本都从那里调用，所以下面的步骤会用到它。它把不同策略的训练与评测收敛到了同一套接口，对学习者的实际好处是：走完一遍 ACT 之后，想换成 π0、RDT-1B 这类 VLA 试试，主要改的是策略名和配置文件，不用从头再理解一套工程。

过程中建议多看合成数据与评测回放视频，以建立对数据分布和策略失败模式的直觉。

### (2.2) 学习流程

**RoboTwin 2.0**：[代码](https://github.com/RoboTwin-Platform/RoboTwin)｜[主页](https://robotwin-platform.github.io/)｜[文档](https://robotwin-platform.github.io/doc/)｜[论文](https://arxiv.org/abs/2506.18088)<br>
**XPolicyLab（策略侧代码）**：[代码](https://github.com/XPolicyLab/XPolicyLab)｜[文档](https://robotwin-platform.github.io/doc/usage/xpolicylab.html)<br>
**任务与榜单**：[50 个双臂任务说明](https://robotwin-platform.github.io/doc/tasks/)｜[Leaderboard](https://robotwin-platform.github.io/leaderboard)<br>
**跑完之后可以看看**：[RoboDojo](https://robodojo-benchmark.com/)（仿真 + 真机统一评测）｜[RMBench](https://rmbench.github.io/)（记忆依赖操作）

#### (2.2.1) 了解 RoboTwin 2.0 做了什么（约 1 天）

阅读 [RoboTwin 2.0 论文](https://arxiv.org/pdf/2506.18088)，了解仿真数据合成的方案，深入理解合成一条机器人数据需要哪些信息、机器人可以完成什么任务，并了解 [Aloha](https://www.bilibili.com/video/BV1vU421d7BJ/) 硬件。

#### (2.2.2) 安装平台（约 0.5 天）

按[安装文档](https://robotwin-platform.github.io/doc/usage/robotwin-install.html)配置环境，整个过程约 20 分钟。**注意 XPolicyLab 现在是 RoboTwin 的 Git 子模块**，克隆时必须递归拉取，否则后续训练与评测会缺文件：

```bash
# 全新克隆
git clone --recurse-submodules https://github.com/RoboTwin-Platform/RoboTwin.git
cd RoboTwin

# 若此前已克隆过，补拉子模块即可
git submodule update --init --recursive XPolicyLab
```

#### (2.2.3) 准备数据（约 0.5 天）

官方已开源 10 万条以上轨迹，**推荐直接下载**，可以省掉数小时的采集时间。下面只取本教程用到的 `beat_block_hammer` 任务：

```bash
# 只下载指定任务；不传参数则下载全部任务
bash scripts/download_xpolicylab_data.sh beat_block_hammer
```

数据会落在 `data/demo_clean/<task_name>/aloha_agilex/data/`。

只有当你需要自定义任务配置、域随机化或更换机器人本体时，才需要自己采集。采集脚本会先搜索能成功完成任务的随机种子，再回放种子录制轨迹：

```bash
bash collect_data.sh ${task_name} ${task_config} ${gpu_id}

# Clean Data Example
bash collect_data.sh beat_block_hammer demo_clean 0

# Randomized Data Example
bash collect_data.sh beat_block_hammer demo_randomized 0
```

自采数据落在 `data/<task_config>/<task_name>/<embodiment>/data/`，已经是 XPolicyLab 轨迹格式，不需要额外转换。想理解 `demo_clean` 与 `demo_randomized` 的差别，可读[域随机化文档](https://robotwin-platform.github.io/doc/usage/domain-randomization.html)。

> ⚠️ 读取 HDF5 里的图像时**只能**用 `XPolicyLab.utils.process_data.decode_image_bit`。自己写 `cv2.imdecode` 或 PIL 解码会因为历史数据版本的布局差异而静默颠倒 RGB 通道，这是最容易踩、也最难排查的坑。

#### (2.2.4) 训练 ACT 策略（约 1 天）

ACT 是非常经典的操作策略算法，适合作为第一个复现对象，训练大约需要 12GB 显存。策略适配器位于 `XPolicyLab/policy/ACT/`，XPolicyLab 里所有策略都遵循同一套生命周期脚本：

```bash
cd XPolicyLab/policy/ACT
bash install.sh                                  # 安装策略侧运行环境
bash process_data.sh <bench_name> <ckpt_name> <env_cfg_type> <action_type>
bash train.sh <bench_name> <ckpt_name> <env_cfg_type> <action_type> <seed> <gpu_id>
```

同一套参数命名会贯穿数据处理、训练与评测，中途不需要改名：`bench_name` 取 `RoboTwin`；`ckpt_name` 是本次训练的简称，例如 `act_demo`；`env_cfg_type` 用 `arx_x5`（对应 RoboTwin 默认的 aloha-agilex 布局）；`action_type` 一般取 `joint` 或 `ee`。权重会落在 `checkpoints/<bench_name>-<ckpt_name>-<env_cfg_type>-<action_type>-<seed>/`。具体参数与显存要求以 [ACT 适配器 README](https://github.com/XPolicyLab/XPolicyLab/blob/main/policy/ACT/README.md) 为准。

#### (2.2.5) 评测策略并对照榜单（约 1 天）

RoboTwin 的所有评测都统一走 `scripts/eval_policy.sh`。调度器会为每个任务各起一个策略服务端和一个仿真器，任务列表与 GPU 配置写在 `env_cfg/eval/all_tasks.yml`——只想评单个任务的话，把 `tasks` 裁成一条即可：

```bash
bash scripts/eval_policy.sh multitask \
  --config env_cfg/eval/all_tasks.yml \
  --policy-name ACT \
  --ckpt-name <checkpoint> \
  --env-cfg-type arx_x5 \
  --policy-conda-env <policy_env> \
  --eval-env-conda-env <robotwin_env> \
  --action-type joint
```

加 `--dry-run` 可以只校验调度计划而不真正启动，结果默认写到 `eval_result/multitask/`。如果本机显卡不够，还可以把策略服务端放在远程机器、仿真器留在本地，用 `--enable-remote` 搭配 `--policy-server-ip / --policy-server-port` 连接，详见 [XPolicyLab 文档](https://robotwin-platform.github.io/doc/usage/xpolicylab.html)。

跑完后把自己的成功率与 [Leaderboard](https://robotwin-platform.github.io/leaderboard) 上 ACT 的官方成绩对照（`demo_clean` 下约 56%）。差距过大通常说明数据量、训练轮数或 `action_type` 没对齐。

至此你已经完整走过一遍操作策略的生命周期。**下一步最划算的动作是换个策略再跑一遍**：把 `--policy-name` 换成 `Pi_0`、`RDT_1B`、`GR00T_N17`、`X_VLA` 中的任意一个，其余流程完全一致，这样能直观感受不同架构在同一任务上的差异。完整策略清单见 [XPolicyLab 文档](https://robotwin-platform.github.io/doc/usage/xpolicylab.html)。

<a id="info"></a>

## 📄 (3) Useful Info - 有利于搭建认知的资料

这一章用于**快速建立对具身智能领域的整体认知**，适合在系统学习算法、工程或硬件之前，用来了解技术版图、社区生态与研究脉络。

### (3.1) 方向性与方法论资料

- 具身智能基础技术路线（Yunlong Dong）：[PDF](./files/具身智能基础技术路线-YunlongDong.pdf)｜[bilibili](https://www.bilibili.com/video/BV1d5ukedEsi)
- 斯坦福机器人学导论：[website](https://www.bilibili.com/video/BV17T421k78T)
- Cyber Nachos（偏系统与工程思维）：[website](https://cybernachos.github.io/)

### (3.2) 社区与自媒体（长期跟进价值高）

**中文（微信公众号）**  
石麻日记、Lumina 具身智能、机器之心、新智元、量子位、具身智能研究室、具身纪元、Human Five、Xbot 具身知识库、具身智能之心、自动驾驶之心、3D 视觉工坊、将门创投、RLCN 强化学习研究、CVHub

**中文（小红书博主）**  
WhynotTV、TianxingChen（陈天行）、穆尧_YaoMarkMu、许华哲 Harry、周博宇、高飞、李弘扬、朱政、丁琰、YY 硕、Mango-Man、RHOSLab #PI-李永露、正合时宜、心言任永亮、York Yang-Dyna Robotics、哲伦班长

**社区与 wiki**

- Simulately（社区维护的仿真器 wiki，选仿真器时的第一站）：[website](https://simulately.wiki/)
- 巨神研习社：[website](http://www.jushenyanxishe.com/)

**英文 newsletter / 媒体 / 播客**

- Import AI（Jack Clark，偏政策与产业视角）：[newsletter](https://jack-clark.net/)
- The Batch（DeepLearning.AI，综述性强、门槛低）：[newsletter](https://www.deeplearning.ai/the-batch/)
- Ahead of AI（Sebastian Raschka，训练与实现细节）：[newsletter](https://magazine.sebastianraschka.com/)
- Humanoid Daily（人形机器人行业日更）：[website](https://johnkoetsier.com/humanoid-daily/)｜Machine Dawn：[website](https://machinedawn.ai/)
- IEEE Spectrum Robotics：[website](https://spectrum.ieee.org/topic/robotics/)｜The Robot Report（偏商业化与供应链）：[website](https://www.therobotreport.com/)
- TWIML AI Podcast：[podcast](https://twimlai.com/podcast/twimlai/)｜The Robot Brains（Pieter Abbeel 主持）：[podcast](https://www.therobotbrains.ai/)

### (3.3) 实验室与学术生态

- Robotics 实验室总结：[zhihu link1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608)｜[zhihu link2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)
- 具身智能华人高引榜：[repo](https://github.com/Will-Gao/Embodied_Intelligence)
- Lumina 具身智能社区：[website](https://lumina-embodied.ai)

### (3.4) 高质量会议与期刊（论文检索时重点关注）

**机器人**：Science Robotics, TRO, IJRR, JFR, RSS, RAL, IROS, ICRA, CoRL<br>
**计算机视觉**：CVPR, ICCV, ECCV｜**机器学习**：NeurIPS, ICML, ICLR｜**AI 与 NLP**：AAAI, ACL

### (3.5) 论文列表（长期跟进研究进展与选题调研）

- Awesome Humanoid Robot Learning（Yanjie Ze）：[repo](https://github.com/YanjieZe/awesome-humanoid-robot-learning)
- Paper Reading List（DeepTimber Community）：[repo](https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List)
- Paper List（Yanjie Ze）：[repo](https://github.com/YanjieZe/Paper-List)
- RoboScholar / Embodied AI Paper List（Tianxing Chen）：[repo](https://github.com/TianxingChen/Paper-List-For-EmbodiedAI)
- Awesome LLM Robotics：[repo](https://github.com/GT-RIPL/Awesome-LLM-Robotics)
- Awesome Video Robotic Papers：[repo](https://github.com/H-Freax/Awesome-Video-Robotic-Papers)
- Awesome Embodied Robotics and Agent：[repo](https://github.com/zchoi/Awesome-Embodied-Robotics-and-Agent)
- awesome-embodied-vla / va / vln：[repo](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln)
- Awesome Affordance Learning：[repo](https://github.com/hq-King/Awesome-Affordance-Learning)
- Embodied AI Paper TopConf：[repo](https://github.com/Songwxuan/Embodied-AI-Paper-TopConf)
- Awesome **RL-VLA** for Robotic Manipulation（Haoyuan Deng）：[repo](https://github.com/Denghaoyuan123/Awesome-RL-VLA)
- Awesome **Efficient-VLA** for Robotic Manipulation（Weifan Guan）：[repo](https://github.com/guanweifan/awesome-efficient-vla)
- Awesome Embodied Data：[project](https://jasper-aaa.github.io/embodied-data-pyramid/)｜[repo](https://github.com/worldbench/awesome-embodied-data-pyramid)｜[arXiv](https://arxiv.org/abs/2607.24744v1)

### (3.6) 年度趋势总结

- State of Robot Learning（Dec 2025）：[website](https://vedder.io/misc/state_of_robot_learning_dec_2025.html)
- 许华哲 - 具身智能：2025 回望：[website](https://zhuanlan.zhihu.com/p/1983661736180589668)
- 林天威 - 具身 VLA 的 2025：从 Demo 到通用的距离：[website](https://zhuanlan.zhihu.com/p/1989799567177307432)

<a id="algorithm"></a>

## 🍎 (4) Algorithm - 算法篇

> 完整内容：[topics/algorithm.md](./topics/algorithm.md)

这一篇把具身智能中最常用的「算法能力栈」从下往上串了起来：**底层**是工程工具与几何、标定、控制这类决定系统能否稳定运行的基础；**中层**是视觉与多模态表征（2D/3D/4D、prompting、affordance），负责把复杂世界压缩成可泛化、可对齐、可被策略利用的中间表示；**上层**则是学习与决策（RL/IL、VLA、LLM + Planner、快慢系统），把感知与任务目标转成可执行动作，并逐步走向更长程、更通用、更可部署的系统形态。

- [(1) Common Tools —— 常用工程工具](./topics/algorithm.md#common-tools)
- [(2) Vision Foundation Models —— 视觉基础模型](./topics/algorithm.md#foundation-models)
- [(3) Robot Learning —— 机器人学习](./topics/algorithm.md#robot-learning)
- [(4) LLM for Robotics —— LLM + 机器人](./topics/algorithm.md#llm_robot)
- [(5) VLA —— Vision-Language-Action Models](./topics/algorithm.md#vla)
  - [(5.0) 参考与综述](./topics/algorithm.md#vla)
  - [(5.1) 经典工作](./topics/algorithm.md#vla)
  - [(5.2) 分层双系统 VLA](./topics/algorithm.md#vla)
  - [(5.3) 最新 VLA 工作](./topics/algorithm.md#vla)
- [(6) Computer Vision —— 计算机视觉](./topics/algorithm.md#cv)
  - [(6.1) 2D / 3D / 4D Vision](./topics/algorithm.md#cv)
  - [(6.2) Visual Prompting & Affordance](./topics/algorithm.md#cv)
- [(7) Computer Graphics —— 计算机图形学](./topics/algorithm.md#cg)
- [(8) Multimodal Models —— 多模态模型](./topics/algorithm.md#mm)
- [(9) Robot Navigation —— 机器人导航](./topics/algorithm.md#navigation)
- [(10) Embodied AI for X —— 具身智能 + X](./topics/algorithm.md#embodied-ai-4-x)
  - [(10.1) Healthcare —— 具身医疗](./topics/algorithm.md#medical)
  - [(10.2) UAV —— 无人机](./topics/algorithm.md#uav)
  - [(10.3) Autonomous Driving —— 自动驾驶](./topics/algorithm.md#ad)

<a id="infrastructure"></a>

## 🏋️‍♂️ (5) Infrastructure - 软件基础设施篇

> 完整内容：[topics/infrastructure.md](./topics/infrastructure.md)

这一章关注的不是「具体某个模型」，而是**支撑具身智能研究与系统落地的软件基础设施（Infrastructure）**。仿真器决定你能构建怎样的世界，基准集决定你如何比较方法优劣，数据集决定模型最终学到什么样的行为分布。它们共同构成了具身智能中**最容易被忽视、但最影响上限与复现性的部分**。

- [(1) Simulators —— 仿真器](./topics/infrastructure.md#simulators)
- [(2) Benchmarks —— 基准集](./topics/infrastructure.md#benchmarks)
- [(3) Datasets —— 数据集](./topics/infrastructure.md#datasets)
- [(4) 工具链 —— 数据格式与策略部署](./topics/infrastructure.md#policy-serving)

<a id="control"></a>

## 🎮 (6) Control - 控制篇

> 完整内容：[topics/control.md](./topics/control.md)

这一章并不是为了让你「立刻跑一个模型」，而是为具身智能系统提供**稳定性、可解释性与工程底座**。控制论保证系统在高频下不崩溃，机器人学提供几何与动力学约束，SLAM 与状态估计让机器人「知道自己在哪里」，ROS 与工程库则把理论变成可复现的系统。

- [(1) Control and Robotics —— 控制论与机器人学基础](./topics/control.md#control-robotics)
  - [(1.1) 经典课程](./topics/control.md#control-courses)
- [(2) Control Foundations —— 控制理论基础](./topics/control.md#control-foundations)
  - [(2.1) 经典控制（Classical Control）](./topics/control.md#classical-control)
  - [(2.2) 现代控制（最优控制）](./topics/control.md#modern-control)
  - [(2.3) 先进控制（Advanced Control）](./topics/control.md#advanced-control)
- [(3) Robotics Foundations —— 机器人学导论](./topics/control.md#robotics-foundations)
  - [(3.1) 推荐教材与材料](./topics/control.md#robotics-books)
  - [(3.2) 运动学与动力学](./topics/control.md#kinematics-dynamics)
  - [(3.3) 里程计与 SLAM](./topics/control.md#slam)
  - [(3.4) 工程生态与工具](./topics/control.md#engineering-stack)

<a id="hardware"></a>

## 🦾 (7) Hardware - 硬件篇

> 完整内容：[topics/hardware.md](./topics/hardware.md)

具身智能硬件涵盖多个技术栈：嵌入式软硬件、机械设计、机器人系统集成与传感器等。它们知识面很杂，但共同目标只有一个：把「算法」变成真实世界里稳定可复现的系统。关于硬件学习，最有效的方式几乎永远是 **从实践出发**——先做出一个能跑起来的最小系统，再逐步扩展复杂度与可靠性。

- [(1) Embedded —— 嵌入式](./topics/hardware.md#embedded)
- [(2) Mechanical Design —— 机械设计](./topics/hardware.md#mechanical)
- [(3) Robot System Design —— 机器人系统设计](./topics/hardware.md#robosystem)
- [(4) Sensors —— 传感器](./topics/hardware.md#sensors)
  - [(4.1) 深度相机（Depth Camera）](./topics/hardware.md#sensors)
- [(5) Tactile Sensing —— 触觉感知](./topics/hardware.md#tactile)
  - [(5.1) 视触觉传感器](./topics/hardware.md#tactile)
  - [(5.2) 电子皮肤](./topics/hardware.md#tactile)
  - [(5.3) 触觉应用与算法](./topics/hardware.md#tactile)
  - [(5.4) 传感器购买](./topics/hardware.md#tactile)
- [(6) Data Collection —— 数据采集硬件](./topics/hardware.md#data_collection)
- [(7) Companies —— 公司与硬件生态](./topics/hardware.md#companies)

## 🤝 Contributing - 参与贡献

本项目由社区共同维护，欢迎任何形式的参与：

- **补充资料**：在对应篇章的 `topics/*.md` 中按现有条目格式追加，并尽量补上一句话说明这份资料解决什么问题；
- **修正内容**：发现失效链接、过时结论或表述错误，欢迎直接提 PR 或开 Issue；
- **改进结构**：对章节组织与学习路线有想法，欢迎在 Issue 中讨论。

提交 PR 前请确认：条目放在了语义最贴近的章节、链接可正常访问、格式与相邻条目保持一致。

## 👍 Citation - 引用

如果这个仓库对你有帮助，欢迎引用：

```bibtex
@misc{embodiedaiguide2025,
  title = {Embodied-AI-Guide},
  author = {Embodied-AI-Guide-Contributors, Lumina-Embodied-AI-Community, Tianxing Chen},
  month = {January},
  year = {2025},
  url = {https://github.com/tianxingchen/Embodied-AI-Guide},
}
```

## 🏷️ License - 许可协议

本项目采用 **非商业使用（Non-Commercial Use）** 协议：

- **允许**：个人学习、学术研究与其他非盈利用途；
- **禁止**：任何形式的商业使用，包括但不限于公司/企业内部使用、集成到收费产品或服务中，或用于任何营利目的。

详情请查看仓库中的 [LICENSE](./LICENSE) 文件。如需商业授权（例如在公司产品或商业项目中使用），请联系项目负责人：[chentianxing2002@gmail.com](mailto:chentianxing2002@gmail.com)。

## ⭐️ Star History - Star 历史

![Star History Chart](https://star-history.dera.page/svg?repos=TianxingChen/Embodied-AI-Guide&type=Date)

## 🤝 Sponsors - 支持机构

感谢 **无界智航**、**超维动力**、**香港大学 MMLab**、**地瓜机器人**、**松灵机器人** 对本项目的支持。

![Sponsors](./files/images/sponsor.png)