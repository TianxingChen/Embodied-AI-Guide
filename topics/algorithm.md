<h1 align="center">Embodied-AI-Guide<br>算法篇</h1>


> 这一篇把具身智能中最常用的“算法能力栈”从下往上串了起来：底层是工程工具与几何/标定/控制这类决定系统能否稳定运行的基础；中层是视觉与多模态表征（2D/3D/4D、prompting、affordance），它们把复杂世界压缩成可泛化、可对齐、可被策略利用的中间表示；上层则是学习与决策（RL/IL、VLA、LLM+Planner、快慢系统），把感知与任务目标转成可执行动作，并逐步走向更长程、更通用、更可部署的系统形态。

<section id="common-tools"></section>

## (1) Common Tools —— 具身智能中的常用工程工具

这一部分聚焦于**具身智能项目中高频出现、工程上“绕不开”的工具与技巧**。  
它们往往不是算法论文的核心贡献，但却决定了一个系统能否真正跑起来、跑稳定、跑到可复现。

在大多数真实或仿真 Project 中，你会反复遇到：**点云如何处理、相机和机械臂如何对齐、目标位姿如何转成可执行动作**。这些问题一旦处理不当，会在后续学习或评估阶段持续放大误差。

| 类别 | 工具/主题 | 链接 | 简要说明 |
|---|---|---|---|
| 点云处理 | 点云降采样 | [link](https://zhuanlan.zhihu.com/p/558683732) | 随机 / 均匀 / FPS / 法线空间等方法，直接影响 3D 感知质量 |
| 标定 | 手眼标定 | [link](https://github.com/fishros/handeye-calib) | 确定相机–机械臂 / 相机–相机相对位姿 |
| 控制 / 规划 | IK / 逆动力学 | [link](https://curobo.org) | 从目标位姿求解关节状态，工程中非常常见 |

在真实系统中，**手眼标定几乎是所有项目的起点**。  
无论是眼在手上（Eye-in-Hand）还是眼在手外（Eye-to-Hand），你都需要在“相机坐标系看到的世界”和“机械臂执行的坐标系”之间建立可靠映射。  
常见工具包括 EasyHeC、fishros 的 handeye-calib，它们在工程上足够成熟，适合直接使用。

围绕这些基础问题，社区已经沉淀了一套相对稳定的组件生态：

| 点云 / 几何 | 机器人中间件 / 规划 | 视觉标记 | 配准 |
|---|---|---|---|
| Open3D | ROS 2 | AprilTag | TEASER++ |
| PCL | MoveIt 2 | ArUco（OpenCV） | ICP（Open3D / PCL） |

这些工具本身**不直接“智能”**，但它们构成了具身智能系统的“骨架层”。  
如果这一层不稳定，再强的模型也很难在真实环境中工作。

**小结**：  
Common Tools 并不是为了“提升指标”，而是为了**降低系统不确定性**。在具身智能中，工程可靠性本身就是一种隐含的性能。

---

<section id="foundation-models"></section>

## (2) Vision Foundation Models —— 视觉基础模型在具身智能中的角色

近年来，大规模视觉基础模型已经成为**具身智能系统的重要感知支柱**。  
它们并不直接输出动作，但通过提供**高质量、具有语义一致性的视觉表征**，显著降低了下游任务（检测、分割、跟踪、位姿估计、操作规划）的难度。

| 能力 | 模型 / 工具 | 链接 | 简要说明 |
|---|---|---|---|
| 图文对齐 | CLIP | [link](https://github.com/openai/CLIP) | 图像–文本共享语义空间 |
| 表征学习 | DINO (v1/v2/v3) | [link](https://github.com/facebookresearch/dino) | 高层视觉特征，对 correspondence 很有帮助 |
| 分割 | SAM / SAM2 | [link](https://segment-anything.com) | 点 / 框提示分割，SAM2 支持视频 |
| 分割追踪 | SAM3 | [link](https://ai.meta.com/sam3) | 图像与视频级持续分割 |
| 3D 重建 | SAM3D | [link](https://ai.meta.com/sam3d) | 资产 / 场景 / 人体重建 |
| 开放词表检测 | Grounding-DINO | [link](https://github.com/IDEA-Research/GroundingDINO) | 文本驱动目标检测 |
| 检测 + 分割 | Grounded-SAM | [link](https://github.com/IDEA-Research/Grounded-SAM-2) | 检测后分割，工程友好 |
| 位姿追踪 | FoundationPose | [link](https://github.com/NVlabs/FoundationPose) | 物体 6D 位姿估计 |
| 深度估计 | Depth Anything v1/v2 | [link](https://github.com/LiheYoung/Depth-Anything) | 单目深度预测 |
| 点云表征 | Point Transformer v3 | [link](https://github.com/Pointcept/PointTransformerV3) | 点云特征学习 |
| 生成 | Stable Diffusion | [link](https://github.com/CompVis/stable-diffusion) | 生成目标图像或中间表征 |
| 机器人 FM | RDT-1B | [link](https://rdt-robotics.github.io/rdt-robotics) | 双臂操作基础模型 |
| 图文对齐 | SigLIP | [link](https://huggingface.co/docs/transformers/en/model_doc/siglip) | CLIP 类模型 |

以 DINO 系列为例，它们并不是为“具身智能”设计的，但其学到的高层视觉表征在**跨实例 correspondence、关键点对齐、对象一致性**等问题上表现出很强的泛化性。这种“隐式几何一致性”对操作任务尤其重要。

在开放世界设置下，**开放词表检测与多任务模型**进一步减少了人工标注和任务定制成本：

| 开放词表 / 多任务 | 分割 | 深度 |
|---|---|---|
| OWL-ViT | Mask2Former | MiDaS |
| DETIC | SEEM |  |

这些模型使系统不再局限于“训练时见过的类别”，而是可以通过语言或提示进行动态感知，这一点在长期自主、家庭场景或多任务系统中尤为关键。

**小结**：  
Vision Foundation Models 的核心价值不在于“替代控制”，而在于**将复杂世界压缩成结构化、可泛化的感知表示**。  
它们是当前具身智能从“任务特化系统”走向“通用系统”的关键一环。


<section id="robot-learning"></section>

## (3) Robot Learning —— 机器人学习（从控制到策略）

机器人学习并不是单一方向，而是一条从**经典控制（PID / MPC）**到**学习型策略（RL / IL）**的连续谱。在具身系统中，很多“成功的方案”本质上是混合式：用控制与规划保证稳定性，用学习补足复杂感知与泛化能力。本节给出一组相对系统的入门资源，同时补充工程里最常用的策略基线与仿真/代码生态，方便你快速形成学习路线并落到可跑的实验。

| 模块 | 资源 | 链接 | 说明 |
|---|---|---|---|
| 自主机器人课程 | ETH & TTIC & UdeM Robot Autonomy | 视频：[link](https://www.edx.org/learn/technology/eth-zurich-self-driving-cars-with-duckietown) / 网站：[link](https://duckietown.com/self-driving-cars-with-duckietown-mooc/) | Duckietown 平台贯穿感知-决策-控制闭环 |
| MPC 入门 | 华工机器人实验室：MPC 从公式到代码 | bilibili：[link](https://www.bilibili.com/video/BV1U54y1J7wh) / 代码：[link](https://gitee.com/clangwu/mpc_control.git) | 从 PID 过渡到 MPC，含仿真与代码 |
| RL 入门 | 强化学习的数学原理（西湖大学） | bilibili：[link](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665) / 书+代码：[link](https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning) | 数学推导体系化，适合打地基 |
| DRL 速览 | Abbeel 6 Lectures | [link](https://www.youtube.com/watch?v=2GwBez0D20A) | 六讲概览 DRL，快速建立框架 |
| DRL 系统课 | Berkeley CS285 | 网站：[link](https://rail.eecs.berkeley.edu/deeprlcourse/) / YouTube：[link](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps) | Levine 主讲，内容详尽 |
| DRL 中文课 | 李宏毅强化学习 | [link](https://www.bilibili.com/video/BV1XP4y1d7Bk) | 搭配实践（Gymnasium 等）较友好 |
| 模仿学习 | LAMDA：IL 简洁教程 | [link](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf) | 结构清晰，入门友好 |
| 真实机器人 IL | RSS 2024 Workshop 教程 | [link](https://www.bilibili.com/video/BV1Fx4y1s7if) | 从真实机器人监督学习的角度讲落地问题 |

为了尽快“跑通一个具身学习 pipeline”，工程上经常直接从成熟基线开始改：

| 策略基线（最常用） | 链接 | 说明 |
|---|---|---|
| ACT（Transformer Policy） | [link](https://github.com/tonyzhaozh/act) / [link](https://tonyzhaozh.github.io/aloha/) | 经典模仿学习基线，适合做对照与复现 |
| Diffusion Policy | [link](https://github.com/real-stanford/diffusion_policy) | 扩散式动作生成，实践中效果稳健 |
| DP3（3D Diffusion Policy） | [link](https://github.com/YanjieZe/3D-Diffusion-Policy) | 引入 3D 表征，适配更复杂几何 |

仿真与代码生态决定了你能否低成本迭代：同一算法在不同平台的“可用性”差异非常大。

| 仿真 / 平台 | 链接 | 常用 Codebase | 链接 |
|---|---|---|---|
| MuJoCo Playground | [link](https://playground.mujoco.org/) | legged-gym | [link](https://github.com/leggedrobotics/legged_gym) |
| Isaac Lab | [link](https://isaac-sim.github.io/IsaacLab/main/index.html) |  |  |
| SAPIEN | [link](https://sapien.ucsd.edu/) |  |  |
| Genesis | [link](https://github.com/Genesis-Embodied-AI/Genesis) |  |  |

**小结**：  
Robot Learning 的核心不是“选 RL 还是 IL”，而是用**控制/规划保证稳定**，用**学习提升复杂感知下的泛化**。建议先用成熟基线跑通数据-训练-评估闭环，再逐步替换关键模块。

---

<section id="llm_robot"></section>

## (4) LLM for Robotics —— 大语言模型在机器人中的应用

LLM 在机器人领域的价值，更多体现在**高层语义理解与任务组织**：把自然语言指令转成结构化计划，或者与传统规划器、3D 感知模块协作形成“可执行”的中间表示。需要强调的是：在多数可落地系统中，LLM 并不直接输出低层控制量，而是充当**高层策略/规划器**或**工具调用与代码生成器**。

| 方向 | 代表资源 / 工作 | 链接 | 说明 |
|---|---|---|---|
| 综述 / 入门 | Robotics+LLM 系列 | [link](https://zhuanlan.zhihu.com/p/668053911) | 系列文章，适合快速扫全景 |
| 概念基础 | Embodied Agent | [link](https://en.wikipedia.org/wiki/Embodied_agent) | 具身智能体基本概念 |
| Agent 综述 | Lilian Weng：AI Agent | 中文：[link](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) / 英文：[link](https://lilianweng.github.io/posts/2023-06-23-agent/) | 讲清 Agent 系统常见范式 |
| LLM 做高层规划 | PaLM-E / DIAC / LBYL / EmbodiedGPT | PaLM-E：[link](https://arxiv.org/abs/2303.03378) / DIAC：[link](https://arxiv.org/abs/2204.01691) / LBYL：[link](https://arxiv.org/abs/2311.17842) / EmbodiedGPT：[link](https://arxiv.org/abs/2305.15021) | 用 LLM 做策略/规划或决策 |
| 统一高低层 | RT-2 | [link](https://arxiv.org/abs/2307.15818) | 将语言-视觉与动作更紧密地统一 |
| LLM + Planner | LLM+P / AutoTAMP / Text2Motion | LLM+P：[link](https://arxiv.org/abs/2304.11477) / AutoTAMP：[link](https://arxiv.org/abs/2306.06531) / Text2Motion：[link](https://arxiv.org/abs/2303.12153) | 结合传统规划器提高可执行性 |
| Code 能力 | Code as Policy / Instruction2Act | CaP：[link](https://arxiv.org/abs/2209.07753) / I2A：[link](https://arxiv.org/abs/2305.11176) | 用代码中间层提升可控性 |
| 3D 感知 + LLM | VoxPoser / OmniManip | VoxPoser：[link](https://arxiv.org/abs/2307.05973) / OmniManip：[link](https://arxiv.org/abs/2501.03841) | 3D 表征辅助规划与约束 |
| 多机器人协同 | RoCo / Scalable-Multi-Robot | RoCo：[link](https://arxiv.org/abs/2307.04738) / Scalable：[link](https://arxiv.org/abs/2309.15943) | 多机器人协同规划 |

如果你更关心“离落地更近”的通用策略（而不是纯 LLM 规划），通常会与 VLA / 通用控制模型一起看：

| 更贴近落地的通用策略 | 链接 | 说明 |
|---|---|---|
| OpenVLA | [link](https://openvla.github.io/) / [link](https://arxiv.org/abs/2406.09246) | 通用操控策略代表作之一 |
| Octo | [link](https://octo-models.github.io/) / [link](https://github.com/octo-models/octo) | 强基线与工程化实现较完整 |

**小结**：  
LLM 在机器人里最可靠的定位通常是**高层理解 + 规划 + 工具调用**，与传统规划/约束或 VLA 低层执行配合，系统更可控、更可复现。

---

<section id="vla"></section>

## (5) Vision-Language-Action Models —— VLA 模型

VLA（Vision-Language-Action）可以理解为“把视觉-语言模型的能力直接延伸到动作空间”。与“VLM 做 planning”不同，VLA 的目标是更端到端：输入视觉与语言，输出可执行动作（或动作序列）。实现上通常涉及一个关键步骤：**动作表示（Action Representation）**——把连续控制量或轨迹转成模型可学习的 token / latent，并设计动作头（autoregressive、diffusion、flow 等）完成生成。

从实践角度看，VLA 的差异往往来自三件事：  
（1）动作如何表示与量化（例如 tokenizer / FAST / latent action）  
（2）训练数据与对齐方式（真实/仿真/合成，多机型/多任务）  
（3）系统形态（单模型端到端 vs 分层双系统，是否引入 planner、world model 等）

### (5.0) 参考与综述

| 类型 | 资源 | 链接 | 备注 |
|---|---|---|---|
| Blog | 具身智能 Vision-Language-Action 的思考 | [link](https://zhuanlan.zhihu.com/p/9880769870) |  |
| Blog | 具身智能 VLA 的思考（问答） | [link](https://www.zhihu.com/question/655570660/answer/87040917575) |  |
| Survey | Action Tokenization 视角 VLA Survey | [link](https://arxiv.org/abs/2507.01925) / [link](https://github.com/Psi-Robot/Awesome-VLA-Papers) | 2025.07.02 |
| Survey | VLA for Embodied AI Survey | [link](https://arxiv.org/abs/2405.14093) | 2024.11.28 |

### (5.1) 经典工作

> 这里内容较多，为了不拉长页面，使用折叠。需要时展开即可。

<details>
<summary><b>展开：经典 VLA 工作列表（按方向归类）</b></summary>

| 方向 | 工作 | 链接 | 机构 | 时间 | 备注 |
|---|---|---|---|---|---|
| Autoregressive | RT-1 | [link](https://arxiv.org/abs/2212.06817) |  |  | RT 系列起点 |
| Autoregressive | RT-2 | [link](https://robotics-transformer2.github.io/) / [link](https://arxiv.org/abs/2307.15818) | Google DeepMind | 2023.07 | 55B |
| Autoregressive | RT-Trajectory | [link](https://arxiv.org/pdf/2311.01977) | GDM / UCSD / Stanford | 2023.11 | 轨迹化输出 |
| Autoregressive | AUTORT | [link](https://arxiv.org/abs/2401.12963) | Google DeepMind | 2024.01 |  |
| Autoregressive | RoboFlamingo | [link](https://arxiv.org/abs/2311.01378) / [link](https://github.com/roboflamingo) | ByteDance / THU | 2024.02 |  |
| Autoregressive | OpenVLA | [link](https://arxiv.org/pdf/2406.09246) / [link](https://github.com/openvla) | Stanford | 2024.06 | 7B |
| Autoregressive | TinyVLA | [link](https://arxiv.org/abs/2409.12514) | 上海大学 | 2024.11 |  |
| Autoregressive | TraceVLA | [link](https://arxiv.org/pdf/2412.10345) / [link](https://github.com/umd-huang-lab/tracevla) | Microsoft | 2024.12 | 输入 visual trace |
| Diffusion / Flow | Octo | [link](https://arxiv.org/pdf/2405.12213) / [link](https://octo-models.github.io/) | Stanford / Berkeley | 2024.05 | Octo-base 93M |
| Diffusion / Flow | π0 | [link](https://arxiv.org/pdf/2410.24164) / [link](https://github.com/Physical-Intelligence/openpi) | Stanford / PI |  | 3.3B；flow-based diffusion |
| Diffusion / Flow | CogACT | [link](https://arxiv.org/pdf/2411.19650) / [link](https://github.com/microsoft/CogACT.git) | THU / MSRA | 2024.11 | 7B |
| Diffusion / Flow | Diffusion-VLA | [link](https://arxiv.org/abs/2412.03293) | 华东师范等 | 2024.12 |  |
| 3D Vision | 3D-VLA | [link](https://arxiv.org/pdf/2403.09631) / [link](https://github.com/UMass-Foundation-Model/3D-VLA/tree/main) | UMass | 2024.03 | 3D-based LLM |
| 3D Vision | SpatialVLA | [link](https://arxiv.org/pdf/2501.15830) / [link](https://github.com/SpatialVLA/SpatialVLA) | 上海 AI Lab | 2025.01 | Adaptive Action Grid |
| VLA-related | FAST（π0） | [link](https://arxiv.org/pdf/2410.24164) / [link](https://github.com/Physical-Intelligence/openpi.git) | Stanford / Berkeley / PI | 2025.01 | 动作 tokenizer |
| VLA-related | RLDG | [link](https://generalist-distillation.github.io/static/high_performance_generalist.pdf) | Berkeley | 2024.12 | 用 RL 生成高质数据再蒸馏 |
| VLA-related | BYO-VLA | [link](https://arxiv.org/abs/2410.01971) / [link](https://github.com/irom-princeton/byovla) | Princeton | 2024.10 | 运行时图像干预 |
| 场景扩展 | RDT-1B（双臂） | [link](https://arxiv.org/pdf/2410.07864) / [link](https://github.com/thu-ml/RoboticsDiffusionTransformer) | 清华 |  | 扩散式动作头 |
| 场景扩展 | QUAR-VLA（四足） | [link](https://arxiv.org/pdf/2312.14457) | 西湖 / 浙大 | 2025.02.04 |  |
| 场景扩展 | CoVLA（自动驾驶） | [link](https://arxiv.org/abs/2408.10845) / [link](https://turingmotors.github.io/covla-ad/) | Turing | 2024.12 |  |
| 场景扩展 | Mobility-VLA（导航） | [link](https://arxiv.org/pdf/2407.07775) | Google DeepMind | 2024.07 |  |
| 场景扩展 | NaVILA（腿式导航） | [link](https://arxiv.org/pdf/2412.04453) / [link](https://navila-bot.github.io/) | UCSD | 2024.12 |  |

</details>

### (5.2) 分层双系统 VLA（2025.05 更新）⭐

近一年一个非常强的范式是“分层双系统”：  
**System 2**（慢系统）负责理解与规划（通常是 VLM/LLM），输出语言/符号/latent 的中间表示；  
**System 1**（快系统）负责高频、稳定的低层控制（VLA / policy），将中间表示转成连续动作。  
它的直观优势是：在长任务与复杂场景中，把“推理/规划”与“高频控制”解耦，既提升可解释性，也更易做工程约束与安全策略。

| 维度 | 常见差异点 | 例子 |
|---|---|---|
| 架构形态 | 单模型 vs 双模型 | Hi-Robot（VLM+VLA） vs π 系列（单模型范式） |
| 通信方式 | 指令 / 子目标 / latent vector | 中间表征粒度决定可控性与泛化 |
| 数据来源 | 真实 / 仿真 / 合成 | 不同数据组成直接影响鲁棒性 |
| 关注重点 | 频率、任务跨度、跨本体 | 人形/移动操作/长程任务等 |

同时也出现了不少“产业级 VLA/系统”，强调端到端能力与部署：

| 系统 / 产品 | 链接 | 时间 | 备注 |
|---|---|---|---|
| Figure：Helix | [link](https://www.figure.ai/news/helix) | 2025.02.20 | 上半身全身控制 |
| 智元：GO-1 | [link](https://www.zhiyuan-robot.com/article/189/detail/56.html) | 2025.03.10 | ViLLA：VLM+MoE，vision-language-latent-action |
| Physical Intelligence（openpi） | [link](https://github.com/Physical-Intelligence/openpi) |  |  |
| π0.5 | [link](https://arxiv.org/abs/2504.16054) | 2025.04.22 | 高级任务分解 + 单模型低层执行 |
| Hi Robot | [link](https://arxiv.org/abs/2502.19417) | 2025.02.26 | VLM 推理 + VLA 执行 |
| Nvidia：GROOT-N1 | [link](https://github.com/NVIDIA/Isaac-GR00T) / [link](https://arxiv.org/abs/2503.14734) | 2025.03.27 | 2B，全身控制，强调部署 |
| Psi-R1（灵初智能） | [link](https://www.jiqizhixin.com/articles/2025-03-03-9) | 2025.04.27 | 分层端到端 VLA + RL，test-time scaling |
| Gemini Robotics | [link](https://arxiv.org/pdf/2503.20020) | 2025.03.25 | 50 Hz |
| Gemini Robotics on-device | [link](https://deepmind.google/discover/blog/gemini-robotics-on-device-brings-ai-to-local-robotic-devices/) | 2025.06.24 | 设备端部署导向 |

### (5.3) 最新 VLA 工作（滚动更新）

<details>
<summary><b>展开：2025 年以来的代表工作</b></summary>

| 工作 | 链接 | 机构 | 时间 | 备注 |
|---|---|---|---|---|
| VQ-VLA | [link](https://arxiv.org/pdf/2507.01016) / [link](https://github.com/xiaoxiao0406/VQ-VLA) | 上海 AI Lab 等 | 2025.07.01 | VQ action tokenizer |
| WorldVLA | [link](https://arxiv.org/pdf/2506.21539) / [link](https://github.com/alibaba-damo-academy/WorldVLA) | 阿里达摩院等 | 2025.06.21 | VLA + World Model 统一 |
| BridgeVLA | [link](https://arxiv.org/abs/2506.07961) / [link](https://github.com/BridgeVLA/BridgeVLA) | CASIA / ByteDance Seed 等 | 2025.06.07 | 3D 对齐到 2D |
| TrackVLA | [link](https://arxiv.org/pdf/2505.23189) / [link](https://github.com/wsakobe/TrackVLA) | 北大等 | 2025.05.29 | 实时检测与导航 |
| OneTwoVLA | [link](https://arxiv.org/pdf/2505.11917) / [link](https://github.com/Fanqi-Lin/OneTwoVLA) | 清华等 | 2025.05.17 | 推理与执行协同 |
| UniVLA | [link](https://arxiv.org/pdf/2505.06111) / [link](https://github.com/OpenDriveLab/UniVLA) | 港大等 | 2025.05.09 | 潜在动作表征 |
| MoManipVLA | [link](https://arxiv.org/pdf/2503.13446) / [link](https://gary3410.github.io/momanipVLA/) | 北邮 / NTU 等 | 2025.03.17 | 移动操作 |
| TLA | [link](https://arxiv.org/pdf/2503.08548) / [link](https://sites.google.com/view/tactile-language-action/) | 三星等 | 2025.03.11 | 引入触觉模态 |
| PointVLA | [link](https://arxiv.org/pdf/2503.07511) / [link](https://pointvla.github.io/) | 美的等 | 2025.03.10 | 点云微调 2D VLA |
| SafeVLA | [link](https://arxiv.org/abs/2503.03480) / [link](https://github.com/PKU-Alignment/SafeVLA) | 北大 | 2025.03.05 | 安全对齐 |
| HybridVLA | [link](https://arxiv.org/pdf/2503.10631) / [link](https://github.com/PKU-HMI-Lab/Hybrid-VLA) | 北大 | 2025.03.17 | 扩散 + 自回归统一 |
| DexVLA | [link](https://arxiv.org/pdf/2502.05855) / [link](https://github.com/juruobenruo/DexVLA) | 美的 / 东南 | 2025.02.09 | 多 action head |
| DexGraspVLA | [link](https://arxiv.org/abs/2502.20900) / [link](https://github.com/Psi-Robot/DexGraspVLA) | 北大 | 2025.02.28 | 灵巧手抓取 |
| UP-VLA | [link](https://arxiv.org/pdf/2501.18867) | 清华 | 2025.02.03 | 预测辅助 |
| UniAct | [link](https://arxiv.org/abs/2501.10105) / [link](https://github.com/2toinf/UniAct) | 清华 |  | 通用动作空间 |
| CoT-VLA | [link](https://arxiv.org/pdf/2503.22020) | Nvidia / Stanford |  | CoT 融入 VLA |

</details>

**小结**：  
VLA 的研究正在从“把动作 token 化”走向“更可控、更可部署、更长程”的系统形态：分层架构、world model、3D 表征与安全对齐都在加速融合。做项目时建议优先关注动作表示与数据配方，它们往往比换 backbone 更影响最终表现。

<section id="cv"></section>

## (6) Computer Vision —— 计算机视觉

具身智能几乎所有下游能力（抓取、操作、导航、交互）都建立在视觉之上。和纯 CV 不同，具身更关心的是：**在变化的光照、遮挡、视角、运动模糊与跨域条件下，视觉表征是否稳定**，以及它是否能与几何（深度/点云）和语言（指令/目标）对齐。本节将视觉按“2D → 3D → 4D（视频/时序）→ Prompting/可供性”串起来，便于你形成一条连续的学习路线。

| 课程/资源 | 链接 | 说明 |
|---|---|---|
| CS231n（Stanford） | [link](https://cs231n.stanford.edu/schedule.html) | 深度学习 CV 全景课，适合视频+讲义快速建立体系 |

### (6.1) 2D / 3D / 4D Vision（从图像到时空）

> 为了不把页面拉得太长，这里把 2D/3D/4D 的资源合并成一个“能力栈表”。你可以按需选择深入方向。

| 层级 | 关注点（具身视角） | 代表资源 | 链接 |
|---|---|---|---|
| 2D Vision | 稳定表征与泛化：backbone、对比学习、生成式表征 | CNN 概念 / ResNet / ViT / Swin | CNN：[link](https://easyai.tech/ai-definition/cnn/；ResNet：https://www.bilibili.com/video/BV1P3411y7nn；ViT：https://www.bilibili.com/video/BV15P4y137jb；Swin：https://www.bilibili.com/video/BV13L4y1475U) |
| 2D Vision | 表征学习方法论：对比学习与大规模预训练 | 对比学习综述 | [link](https://www.bilibili.com/video/BV19S4y1M7hm) |
| 2D/4D Gen | 生成式模型（用于表征、合成数据、目标图像等） | 自回归综述 / 扩散综述 / 扩散推导 | 自回归：[link](https://arxiv.org/pdf/2411.05902；扩散：https://arxiv.org/pdf/2209.00796；推导：https://kexue.fm/archives/9119) |
| 3D Vision | 多视几何与三维理解（对重建/位姿/点云感知很关键） | Andreas Geiger 3D Vision | [link](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) |
| 3D Vision | 三维重建与理解（偏工程与应用） | GAMES203 | [link](https://www.bilibili.com/video/BV1pw411d7aS) |
| 3D/Gen | 2D/3D 生成方向梳理 | 论文分类 / 2024 论文整理 | 分类：[link](https://zhuanlan.zhihu.com/p/617510702；2024：https://zhuanlan.zhihu.com/p/700895749) |
| 4D Vision | 视频理解：时序建模与跨帧一致性（具身中非常常见） | 开山之作 / 串讲 / 综述 | 开山：[link](https://www.bilibili.com/video/BV1mq4y1x7RU；串讲：https://www.bilibili.com/video/BV1fL4y157yA；综述：https://arxiv.org/pdf/2312.17432) |
| 4D Gen | 视频/4D 生成（用于合成与世界建模相关） | Lilian Weng 视频扩散博客 / 4D generation list | 博客：[link](https://lilianweng.github.io/posts/2024-04-12-diffusion-video/；list：https://github.com/cwchenwang/awesome-4d-generation) |

### (6.2) Visual Prompting & Affordance Grounding

具身视觉的一个关键变化是：我们不只想识别物体，而是要回答“**哪里能抓、怎么推、哪能开合**”。  
因此在工程系统里，视觉常常以两种形式进入控制：  
（1）通过 prompt / 标注把视觉模型“定向”到当前任务；（2）通过 affordance 将视觉输出直接变成可执行的交互区域或动作参数。

| 方向 | 资源 | 链接 | 说明 |
|---|---|---|---|
| Visual Prompting | 视觉提示综述 | [link](https://arxiv.org/abs/2409.15310) | Prompt 作为任务条件，连接视觉与决策 |
| Visual Prompting | PIVOT | [link](https://pivot-prompt.github.io) | 迭代式视觉问答，zero-shot 控制与空间推理 |
| Visual Prompting | Set-of-Mark（SoM）for GPT-4V | [link](https://som-gpt4v.github.io) | 用可视标记提升可控性与对齐 |

| 维度 | 工作/数据集 | 链接 | 说明 |
|---|---|---|---|
| 2D Affordance | Cross-View-AG / AGD20K | [link](https://arxiv.org/pdf/2203.09905) / [link](https://github.com/lhc1224/Cross-View-AG) | 跨视角学习可供性 + 数据集 |
| 2D Affordance | AffordanceLLM | [link](https://arxiv.org/pdf/2401.06341) | 借助 VLM/LLM 知识提升泛化 |
| 3D Affordance | Where2Act | [link](https://arxiv.org/abs/2101.02692) | 铰接物体可供性与交互点 |
| 3D Affordance | VAT-Mart | [link](https://openreview.net/pdf?id=iEx3PiooLy) | 铰接交互数据 |
| 3D Affordance | DeformableAffordance / UniGarmentManip | [link](https://arxiv.org/pdf/2303.11057) / [link](https://arxiv.org/abs/2405.06903) | 柔性物体与服装等场景 |
| 3D Affordance | SceneFun3D / 3D AffordanceNet | [link](https://scenefun3d.github.io/) / [link](https://github.com/lhc1224/Cross-View-AG) | 室内环境+实物数据与点云可供性数据集 |

**小结**：  
对具身而言，CV 不只是分类/检测，而是提供可用于交互与决策的稳定表征：2D 打底，3D 提供几何约束，4D 提供跨时间一致性，而 Prompting/可供性把视觉输出变成“可执行”的中间表示。

---

<section id="cg"></section>

## (7) Computer Graphics —— 计算机图形学（仿真、重建与可微渲染的入口）

图形学在具身中的价值通常体现在三类事情：  
（1）仿真与渲染：让你低成本生成交互数据；（2）重建：把现实转成可学习的资产；（3）新型表示：如 NeRF / 3DGS 带来的可微与高效渲染，正在影响数据合成与世界建模。

| 方向 | 资源 | 链接 | 备注 |
|---|---|---|---|
| 图形学入门 | GAMES101 | [link](https://games-cn.org/intro-graphics/) | 闫令琪老师 |
| 实时渲染 | GAMES202 | [link](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html) |  |
| 角色动画 | GAMES105 | [link](https://games-105.github.io/) | motion synthesis / animation |
| 三维重建 | NeRF 原理代码讲解 | [link](https://www.bilibili.com/video/BV1CC411V7oq) |  |
| 三维重建 | 3DGS 原理代码讲解 | [link](https://www.bilibili.com/video/BV1zi421v7Dr) |  |
| 3D 预训练综述 | 3D pre-training survey | [link](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf) |  |
| 3DGS+机器人综述 | 3DGS in Robotics survey | [link](https://arxiv.org/pdf/2410.12262v2) |  |

**小结**：  
图形学更像“具身的数据与世界接口”：它决定了你能否把场景/资产做成可复现、可扩展、可规模化的训练资源。

---

<section id="mm"></section>

## (8) Multimodal Models —— 多模态模型（视觉×语言×时序的统一表征）

具身系统中常见的输入是视觉（RGB/Depth/点云）与语言（目标与约束），并且往往伴随强烈的时序依赖。多模态模型的核心作用是：把这些信息压缩成一个统一表征空间，使得系统能够在“看懂 + 听懂 + 记住”的前提下做决策与控制。

| 工作/项目 | 链接 | 说明 |
|---|---|---|
| CLIP | [link](https://zhuanlan.zhihu.com/p/493489688) | 经典图文对齐工作（具身中常用作检索/对齐） |
| LLaVA | [link](https://llava-vl.github.io/) | 多模态大语言模型经典工作 |
| 多模态生成综述 | [link](https://arxiv.org/pdf/2503.04641) |  |
| VLM-R1 | [link](https://github.com/om-ai-lab/VLM-R1) | OmAI Lab：R1-style 多模态强化学习（GRPO），强调比常规 SFT 更强 |

**小结**：  
多模态并不是“把模态拼起来”，而是解决对齐与一致性：对齐让语言可控，一致性让跨时间的决策更稳定。

---

<section id="navigation"></section>

## (9) Robot Navigation —— 机器人导航（任务、系统与生态）

机器人导航的本质是：智能体在已知或未知环境中，根据传感器输入（RGB/Depth/GPS/IMU 等）与目标指令，输出一系列动作以到达目标。具身任务里，导航往往是更复杂操作的前置能力：先到达、再交互。

为了避免“分类太碎导致阅读成本高”，这里把导航组织为三层：**任务形态 → 系统形态 → 代表工作与数据集生态**。

### (9.1) 任务形态（你到底在导航到什么）

| 任务类型 | 简述 |
|---|---|
| 物体目标导航（Object-Goal Nav） | 输入是目标物体描述，输出到达目标物体附近的动作序列 |
| 图像目标导航（Image-Goal Nav） | 输入是一张目标图像，目标是到达与图像一致的场景位置 |
| 视觉-语言导航（VLN） | 输入是自然语言指令（路线/描述/约束），目标是按语言完成路径 |

### (9.2) 系统形态（你如何把感知变成行动）

| 系统 | 描述 | 优势 | 局限 |
|---|---|---|---|
| 端到端（E2E） | 直接从传感器输入映射到动作（RL/IL 等） | 简洁直接 | 易过拟合、泛化挑战大 |
| 模块化（Modular） | Mapping + Global Policy + Local Policy 等模块接口组合 | 可解释、工程可控 | 规则与手工设计仍限制通用性 |
| 零样本（Zero-shot） | 不训练或少训练，依赖 CLIP/LLM 等先验 | 更接近迁移到真实场景 | 推理慢、上限受限，常需再对齐 |

### (9.3) 代表工作（按系统形态组织）

> 这里的工作可以作为“入门时的 anchor”，建议先读摘要+方法图建立直觉，再决定深入方向。

<details>
<summary><b>展开：端到端（E2E）</b></summary>

| 工作 | 链接 |
|---|---|
| Learning Object Relation Graph and Tentative Policy for Visual Navigation | [link](https://arxiv.org/abs/2007.11018) |
| VTNet: Visual Transformer Network for Object Goal Navigation | [link](https://openreview.net/forum?id=DILxQP08O3B) |

</details>

<details>
<summary><b>展开：模块化（Modular）</b></summary>

| 方法/简称 | 工作 | 链接 | 备注 |
|---|---|---|---|
| SemExp | Object Goal Navigation using Goal-Oriented Semantic Exploration | [link](https://arxiv.org/abs/2007.00643) | 早期语义地图代表 |
| PONI | Potential Functions for ObjectGoal Navigation with Interaction-free Learning | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Ramakrishnan_PONI_Potential_Functions_for_ObjectGoal_Navigation_With_Interaction-Free_Learning_CVPR_2022_paper.pdf) | potential function + 语义地图预测 |
| 3D-aware | 3D-Aware Object Goal Navigation via Simultaneous Exploration and Identification | [link](https://arxiv.org/abs/2212.00338) | 引入 3D 缓解 2D 语义图信息损失 |

</details>

<details>
<summary><b>展开：零样本（Zero-shot）</b></summary>

| 工作 | 链接 | 备注 |
|---|---|---|
| CoWs on Pasture: Baselines and Benchmarks for Language-Driven Zero-Shot Object Navigation | [link](https://arxiv.org/abs/2203.10421) | 用 CLIP 找目标，找到就走过去 |
| L3MVN: Leveraging Large Language Models for Visual Target Navigation | [link](https://arxiv.org/abs/2304.05501) | LLM 决策“朝哪走” |
| ESC: Exploration with Soft Commonsense Constraints for Zero-shot Object Navigation | [link](https://arxiv.org/abs/2301.13166) | 语义地图 + 常识约束 |
| SG-Nav: Online 3D Scene Graph Prompting for LLM-based Zero-shot Object Navigation | [link](https://arxiv.org/abs/2410.08189) | 在线构建场景图喂给 LLM |

</details>

### (9.4) 数据集与仿真生态（决定你能跑什么实验）

| 数据集/平台 | 链接 | 备注 |
|---|---|---|
| Matterport3D（MP3D） | [link](https://niessner.github.io/Matterport/) | 真实场景采集，规模大、难度高 |
| Habitat-Matterport3D（HM3D） | [link](https://aihabitat.org/datasets/hm3d/) | Habitat 生态核心数据 |
| RoboTHOR | [link](https://ai2thor.allenai.org/robothor/) | 场景较小，仿真更轻量 |
| AI2-THOR | [link](https://ai2thor.allenai.org/) | 与 RoboTHOR 同系，交互生态强 |
| Gibson / iGibson | （可补链接） | 室内仿真常用，含交互任务生态 |
| VLN 常用：R2R / RxR / CVDN | （可补链接） | 偏语言导航方向的数据集 |

> 注：如果你希望这里“完全自洽且可点击”，我也可以把 Gibson/iGibson 与 R2R/RxR/CVDN 的链接补齐并统一格式。

### (9.5) 其他参考（进一步扩展）

| 资源 | 链接 |
|---|---|
| Object-Goal Navigation 综述 | [link](https://orca.cardiff.ac.uk/id/eprint/167432/1/ObjectGoalNavigationSurveyTASE.pdf) |
| Awesome VLN | [link](https://github.com/eric-ai-lab/awesome-vision-language-navigation) |
| Habitat Navigation Challenge | [link](https://github.com/facebookresearch/habitat-challenge) |

**小结**：  
导航方向最重要的分歧不在“用什么网络”，而在系统形态：端到端追求简洁但容易过拟合，模块化更可控但偏工程，零样本更易迁移但速度与上限受限。做项目时建议先选定评估平台与数据集生态，再决定模型路线，否则很容易在实现层面被卡住。


<section id="embodied-ai-4-x"></section>

## (10) Embodied AI for X - 具身智能+X

<section id="medical"></section>

### (10.1) EAI for Healthcare - 具身医疗

> 具身智能技术的迅猛发展正在引领医疗服务模式迈向革命性的新纪元。作为人工智能算法、先进机器人技术与生物医学深度融合的前沿交叉学科, 具身智能+医疗这一研究领域不仅突破了传统医疗的边界, 更开创了智能化医疗的新范式。其多学科协同创新的特质, 正在重塑医疗服务的全流程, 为精准医疗、远程诊疗和个性化健康管理带来前所未有的发展机遇, 推动医疗行业向更智能、更人性化的方向转型升级。这一领域的突破性进展, 标志着医疗科技正迈向一个全新的智能化时代。

| 综述 | 链接 |
|---|---|
| 医疗具身智能综述 | [link](https://arxiv.org/abs/2501.07468) |

#### (10.1.1) MLLM for Medical - 多模态大语言模型在医学中的应用

| 资源 | 链接 |
|---|---|
| 用于医学影像分析的通用人工智能综述 | [link](https://arxiv.org/pdf/2306.05480) |
| 医学影像的通用分割模型-MedSAM | [link](https://www.nature.com/articles/s41467-024-44824-z.pdf) |
| 2024盘点：医学AI大模型, 从通用视觉到医疗影像 | [link](https://mp.weixin.qq.com/s?__biz=MzIxNTc4NzU0MQ==&mid=2247550230&idx=1&sn=6baa8dcba12f3f70f4c8205a0f23b6a0&chksm=966df4ca45c8cbcaa0a5d2e42fbb4de92e6881f92981071ce7fda3bd1e13e4715f92415a9258&scene=27) |
| 医疗领域基础模型的发展机遇与挑战 | [link](https://arxiv.org/pdf/2404.03264) |
| SkinGPT-4 for dermatological diagnosis | [link](https://www.nature.com/articles/s41467-024-50043-3) |
| PneumoLLM for pneumoconiosis diagnosis | [link](https://www.sciencedirect.com/science/article/abs/pii/S1361841524001737) |
| BiomedGPT | [link](https://github.com/taokz/BiomedGPT) |
| LLaVA-Med | [link](https://github.com/microsoft/LLaVA-Med?tab=readme-ov-file) |
| RoboNurse-VLA | [link](https://robonurse-vla.github.io) |
| PathChat | [link](https://www.nature.com/articles/s41586-024-07618-3) |
| DeepDR-LLM | [link](https://www.nature.com/articles/s41591-024-03139-8) |
| VisionFM | [link](https://ai.nejm.org/doi/full/10.1056/AIoa2300221) |
| Medical-CXR-VQA | [link](https://github.com/Holipori/Medical-CXR-VQA) |

#### (10.1.2) Medical Robotics - 医疗机器人

| 主题 | 资源 | 链接 |
|---|---|---|
| 五级自动化 | Medical robotics—Regulatory, ethical, and legal considerations for increasing levels of autonomy | [link](https://www.science.org/doi/pdf/10.1126/scirobotics.aam8638) |
| 十年回顾 | A decade retrospective of medical robotics research from 2010 to 2020 | [link](https://www.science.org/doi/epdf/10.1126/scirobotics.abi8017) |
| 医疗具身智能分级 | A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities | [link](https://arxiv.org/pdf/2501.07468) |
| AI meets medical robotics | Artificial intelligence meets medical robotics | [link](https://www.science.org/doi/abs/10.1126/science.adj3312) |
| 机器人手术综述 | Robotic surgery (Nature Reviews Bioengineering) | [link](https://www.nature.com/articles/s44222-025-00294-6) |

**医疗机器人的机器视觉**

| 资源 | 链接 |
|---|---|
| 3DGS在腔镜手术中的应用综述 | [link](https://arxiv.org/pdf/2408.04426) |
| LVM在手术机器人上的综述（CUHK任洪亮团队） | [link](https://www.nature.com/articles/s44287-025-00166-6) |

**达芬奇相关**

| 资源 | 链接 |
|---|---|
| dVRK介绍 | [link](https://ieeexplore.ieee.org/abstract/document/9531355) |
| Surgical Robot Transformer (SRT) | [link](https://surgical-robot-transformer.github.io/) |

**Domain-specific Simulators（手术机器人技能学习模拟器）**

| 模拟器 | 链接 |
|---|---|
| SurRoL | [link](https://med-air.github.io/SurRoL/) |
| Surgical Gym | [link](https://github.com/SamuelSchmidgall/SurgicalGym) |
| ORBIT-Surgical | [link](https://orbit-surgical.github.io/) |
| 自主缝合综述 | [link](https://link.springer.com/article/10.1007/s00464-024-10788-w) |

**连续体与软体手术机器人**

| 资源 | 链接 |
|---|---|
| Continuum Robots for Medical Interventions | [link](https://ieeexplore.ieee.org/abstract/document/9707607) |
| Soft Robot-Assisted Minimally Invasive Surgery and Interventions: Advances and Outlook | [link](https://ieeexplore.ieee.org/abstract/document/9765966/authors#authors) |
| 血管介入手术机器人具身智能综述 | [link](https://arxiv.org/abs/2504.15327) |
| 什么是软体机器人？软体机器人的具身智能定义 | [link](https://www.zhihu.com/question/61637360/answer/92834447300?utm_psn=1870238291607040000) |
| Learning-Based Control Strategies for Soft Robots: Theory, Achievements, and Future Challenges | [link](https://ieeexplore.ieee.org/abstract/document/10136428) |
| A concise guide to modelling the physics of embodied intelligence in soft robotics | [link](https://inria.hal.science/hal-03921606/document) |
| Data-driven methods applied to soft robot modeling and control: A review | [link](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10477253) |

**微纳机器人**

| 资源 | 链接 |
|---|---|
| Machine learning for micro- and nanorobots | [link](https://www.nature.com/articles/s42256-024-00859-x) |

---

<section id="uav"></section>

### (10.2) UAV —— 无人机（技能、任务与本体）

无人机研究大体可以用“三条主线”来理解：  
**技能（Skill）**：避障、竞速、敏捷飞行/特技等，强调高速闭环与安全约束；  
**任务（Task）**：探索、重建、跟踪/追捕等，强调长时规划与不确定环境；  
**本体（Platform）**：飞行器构型与载荷（例如空中机械臂、全驱动、多模态等），决定了可执行的动作空间与任务边界。  
实际系统里三者往往是耦合的：任务提出约束，技能保证可执行，本体决定上限。

#### (10.2.1) 技能实现/学习（Skill Learning）

无人机技能学习的瓶颈通常不是“有没有算法”，而是**闭环速度、仿真可用性、sim2real 稳定性**。因此这里先列出更贴近 RL/学习的仿真器与工程链路，再给代表工作做索引。

| 类别 | 仿真/链路 | 链接 | 备注 |
|---|---|---|---|
| 学习仿真 | AirSim | [link](https://microsoft.github.io/AirSim/) | UE4；生态成熟但运行偏慢 |
| 学习仿真 | Flightmare | [link](https://github.com/uzh-rpg/flightmare) | Unity 渲染；CPU 并行动力学 |
| 学习仿真 | AerialGym | [link](https://github.com/ntnu-arl/aerial_gym_simulator) | IsaacSim；GPU 并行动力学 |
| 轻量生态 | gym-pybullet-drones | （建议补链接） | 轻量、研究/教学常用 |
| 工程链路 | PX4 SITL / ROS2 | （建议补链接） | 更贴近真实系统部署与接口 |

<details>
<summary><b>展开：经典技能代表工作（按主题归类）</b></summary>

**未知场景障碍物躲避 / 反应式控制**

| 工作 | 链接 | 备注 |
|---|---|---|
| Learning Monocular Reactive UAV Control in Cluttered Natural Environments (ICRA 2013, CMU) |  | 监督学习：图像 → 离散控制指令 |
| CAD2RL: Real Single-Image Flight without a Single Real Image (RSS 2017, UCB) |  | sim2real RL + domain randomization |
| DroNet: Learning to Fly by Driving (RAL 2018, UZH) | [link](https://github.com/uzh-rpg/rpg_public_dronet) | 输出速度指令 |
| Learning High-Speed Flight in the Wild (SciRob 2021, UZH) | [link](https://github.com/uzh-rpg/agile_autonomy) | dagger + 传统轨迹规划监督 |
| Back to Newton's Laws… Differentiable Physics (Arxiv 2024, SJTU) |  | 可微物理辅助策略优化 |
| Flying on Point Clouds using RL (Arxiv 2025, ZJU) | [link](https://arxiv.org/abs/2503.00496) | 机载雷达 + sim2real RL |

**无人机竞速（高速度、高精度、高风险约束）**

| 工作 | 链接 | 备注 |
|---|---|---|
| Champion-level drone racing using deep RL (Nature 2023, UZH) |  | RL 战胜人类冠军 |
| Optimal Control vs RL in Racing (SciRob 2023, UZH) |  | RL 与最优控制对比 |
| Agile Flight from Pixels w/o State Estimation (RSS 2024, UZH) |  | 视觉端到端，不依赖显式状态估计 |

**大机动 / 特技飞行（敏捷性与可控性）**

| 工作 | 链接 | 备注 |
|---|---|---|
| Deep Drone Acrobatics (RSS 2020, UZH) |  | 模仿学习 + MPC 轨迹跟踪 |
| Whole-Body Control Through Narrow Gaps (ICRA 2025, ZJU) | [link](https://arxiv.org/abs/2409.00895) | 端到端窄缝穿越 |

</details>

**小结**：  
技能学习的主矛盾通常是“闭环工程问题”：仿真速度、传感器噪声、延迟与 sim2real。选平台时建议先明确你需要的是 **快速迭代（轻量）** 还是 **高保真+可部署（PX4/ROS 链路）**。

---

#### (10.2.2) 任务实现/学习（Task Learning）

任务层比技能层更强调：**长时规划、部分可观测、目标不确定与多机协作**。很多工作会把“任务规划”交给上层策略，把“飞行稳定”交给下层控制/技能模块。

<details>
<summary><b>展开：经典任务代表工作（探索/追捕等）</b></summary>

| 任务 | 工作 | 链接 |
|---|---|---|
| 追捕/协作 | HOLA-Drone: Hypergraphic Open-ended Learning for Zero-Shot Multi-Drone Cooperative Pursuit (Arxiv 2024, Manchester) |  |
| 追捕/规划 | Multi-UAV Pursuit-Evasion with Online Planning… (Arxiv 2024, THU) |  |
| 探索 | Deep RL-based Large-scale Robot Exploration (RAL 2024, NUS) |  |
| 探索 | ARiADNE: … Exploration (ICRA 2023, NUS) |  |
| 探索 | DARE: Diffusion Policy for Autonomous Robot Exploration (ICRA 2025, NUS) |  |

</details>

---

#### (10.2.3) 无人机硬件平台搭建

| 教程 | 链接 |
|---|---|
| 从 0 制作自主空中机器人 | [link](https://www.bilibili.com/video/BV1WZ4y167me) |

---

#### (10.2.4) 新构型无人机设计

这一部分更偏“具身本体学”：通过构型改变动作空间，使无人机从“移动平台”变成“可交互平台”。

**空中机械臂（Aerial Manipulator）**

| 资源/工作 | 链接 | 备注 |
|---|---|---|
| 空中作业机器人，下一代无人机技术？ | [link](https://zhuanlan.zhihu.com/p/442331197) |  |
| Past, Present, and Future of Aerial Robotic Manipulators (TRO 2022) | [link](https://ieeexplore.ieee.org/document/9462539) | 综述 |
| Millimeter-Level Pick and Peg-in-Hole by Aerial Manipulator (TRO 2023) | [link](https://ieeexplore.ieee.org/abstract/document/10339889) |  |
| NDOB-Based Control of a UAV with Delta-Arm… (ICRA 2025) | [link](https://arxiv.org/abs/2501.06122) |  |
| A Compact Aerial Manipulator… (JIRS 2024) | [link](https://link.springer.com/article/10.1007/s10846-024-02090-7) |  |

**全驱动无人机（Fully-Actuated UAV）**

| 工作 | 链接 | 备注 |
|---|---|---|
| Fully Actuated Multirotor UAVs: A Literature Review (RAM 2020) | [link](https://ieeexplore.ieee.org/document/8978486/?arnumber=8978486) | 综述 |
| Omni-directional aerial vehicle (ICRA 2016, ETH) | [link](https://ieeexplore.ieee.org/document/7487497) |  |
| Voliro omniorientational hexacopter (RAM 2018, ETH) | [link](https://ieeexplore.ieee.org/document/8485627) |  |
| FLOAT Drone (Arxiv 2025, ZJU) | [link](https://arxiv.org/abs/2503.00785) |  |

**可变形无人机（Deformable UAV）**

| 工作 | 链接 |
|---|---|
| DRAGON (RAL 2018) | [link](https://ieeexplore.ieee.org/document/8258850) |
| The Foldable Drone (RAL 2019) | [link](https://ieeexplore.ieee.org/document/8567932?arnumber=8567932) |
| Ring-Rotor (RAL 2023) | [link](https://ieeexplore.ieee.org/document/10044964) |
| Passively Morphing Quadcopter (ICRA 2019) | [link](https://ieeexplore.ieee.org/document/8794373) |

**多模态无人机（Terrestrial-Aerial / Multi-Modal）**

| 工作 | 链接 |
|---|---|
| A bipedal walking robot that can fly… (SciRob 2021, Caltech) | [link](https://www.science.org/doi/10.1126/scirobotics.abf8136) |
| Morphobot (NC 2023) | [link](https://www.nature.com/articles/s41467-023-39018-y) |
| Skater (RAL 2024, ZJU) | [link](https://ieeexplore.ieee.org/document/10538378) |
| Terrestrial-Aerial Bimodal Vehicles Navigation (RAL 2022, ZJU) | [link](https://ieeexplore.ieee.org/document/9691888) |

**小结**：  
如果你关注“具身交互”，新构型往往比换算法更有效：空中机械臂解决“能不能操作”，全驱动解决“姿态与力控自由度”，可变形解决“通过性与安全”，多模态解决“跨地形任务连续性”。

---

<section id="ad"></section>

### (10.3) Autonomous Driving —— 自动驾驶

自动驾驶和具身操作类似，本质是“在复杂开放世界中闭环决策”。但它的研究与工程路线经常可以归纳成两大块：  
**世界模型（World / Simulation）**：如何表示、重建并可控生成驾驶世界（用于仿真、数据增广、评测与训练）；  
**策略系统（Policy）**：从模块化到端到端，并出现越来越多“快慢系统”范式（快系统高频安全控制，慢系统语义理解与规划）。

#### (10.3.1) World / Simulation：重建 + 可控生成

| 主题 | 资源/工作 | 链接 | 备注 |
|---|---|---|---|
| 生成式仿真（概念） | 生成式仿真为具身智能释放无限灵感 | [link](https://bydrug.pharmcube.com/news/detail/80b67b2227879864af934e5f81835776) |  |

**3D/4D 场景重建**

| 工作 | 链接 | 备注 |
|---|---|---|
| NSG | [link](https://github.com/princeton-computational-imaging/neural-scene-graphs) / [link](https://arxiv.org/abs/2011.10379) | CVPR 2021 |
| MARS | [link](https://open-air-sun.github.io/mars/) / [link](https://arxiv.org/abs/2307.15058) |  |
| StreetGaussians | [link](https://github.com/zju3dv/street_gaussians) / [link](https://arxiv.org/abs/2401.01339) |  |
| OmniRe | [link](https://ziyc.github.io/omnire) / [link](https://github.com/ziyc/drivestudio) / [link](https://arxiv.org/abs/2408.16760) | ICLR 2025 Spotlight |

**场景可控生成 / 世界模型**

| 工作 | 链接 | 备注 |
|---|---|---|
| GAIA-1 | [link](https://wayve.ai/thinking/introducing-gaia1/) / [link](https://arxiv.org/abs/2309.17080) |  |
| GenAD（OpenDV） | [link](https://github.com/OpenDriveLab/DriveAGI?tab=readme-ov-file#opendv) / [link](https://arxiv.org/abs/2403.09630) | CVPR 2024 Highlight |
| Vista | [link](https://opendrivelab.com/Vista) / [link](https://github.com/OpenDriveLab/Vista) / [link](https://arxiv.org/abs/2405.17398) | NeurIPS 2025 |
| SCP-Diff | [link](https://air-discover.github.io/SCP-Diff/) / [link](https://github.com/AIR-DISCOVER/SCP-Diff-Toolkit) / [link](https://arxiv.org/abs/2403.09638) |  |
| MagicDrive → MagicDriveDiT | [link](https://gaoruiyuan.com/magicdrive-v2/) / [link](https://arxiv.org/abs/2411.13807) |  |
| UniScene | [link](https://arlo0o.github.io/uniscene/) / [link](https://arxiv.org/abs/2412.05435) | CVPR 2025 |
| VaVAM | [link](https://github.com/valeoai/VideoActionModel) |  |

**生态补充**

| 仿真/数据生态 | 链接 | 说明 |
|---|---|---|
| CARLA | （建议补链接） | 自动驾驶仿真常用 |
| nuScenes / Waymo Open / Argoverse 2 | （建议补链接） | 数据与评测生态（决定可复现实验） |

**小结**：  
世界模型路线的关键不是“生成得像不像”，而是“能不能被策略有效利用”：可控性、可评测性、覆盖长尾场景，往往比视觉质量更关键。

---

#### (10.3.2) Policy：从模块化到端到端，再到快慢系统

| 主题 | 资源 | 链接 |
|---|---|---|
| 模块化到端到端 | End-to-end Autonomous Driving: Challenges and Frontiers | [link](https://arxiv.org/pdf/2306.16927) |
| 快慢系统并行（观点） | 理想端到端-VLM双系统 | [link](https://www.sohu.com/a/801987742_258768) |

为了便于“选路线”，这里把代表工作按快/慢系统拆开：  
快系统通常强调高频闭环（检测、占用、轨迹与控制），慢系统强调语义理解、解释与规划（往往更接近 VLM/LLM）。

**快系统代表作**

| 工作 | 链接 | 备注 |
|---|---|---|
| UniAD | [link](https://github.com/OpenDriveLab/UniAD) / [link](https://arxiv.org/abs/2212.10156) | CVPR 2023 Best Paper |
| VAD | [link](https://github.com/hustvl/VAD) / [link](https://arxiv.org/abs/2303.12077) | ICCV 2023 |
| SparseDrive | [link](https://github.com/swc-17/SparseDrive) / [link](https://arxiv.org/abs/2405.19620) |  |
| DiffusionDrive | [link](https://github.com/hustvl/DiffusionDrive) / [link](https://arxiv.org/abs/2411.15139) | CVPR 2025 |
| Scale-up 特性探究 | [link](https://arxiv.org/pdf/2412.02689) |  |

**慢系统代表作**

| 工作 | 链接 | 备注 |
|---|---|---|
| DriveVLM | [link](https://arxiv.org/abs/2402.12289) | CoRL 2024 |
| EMMA | [link](https://arxiv.org/abs/2410.23262) |  |
| Open-EMMA | [link](https://github.com/taco-group/OpenEMMA) | 开源实现 |

**小结**：  
自动驾驶策略的发展越来越像具身操作：快系统保证稳定与安全，慢系统提供语义理解与长时规划。做研究时建议先固定评测生态（数据/仿真/指标），再讨论模型形态，否则很难做可复现对比。

---

#### (10.3.3) 未来方向

| 资源 | 链接 |
|---|---|
| AIR ApolloFM 技术全解读 | [link](https://air.tsinghua.edu.cn/info/1007/2258.htm) |
