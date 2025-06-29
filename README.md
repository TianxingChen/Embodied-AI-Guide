<h1 align="center">具身智能技术指南 Embodied-AI-Guide</h1>

<p align="center"> </p>


> Embodied AI（具身智能）入门的路径以及高质量信息的总结, 期望是按照路线走完后, 新手可以快速建立关于这个领域的认知, 希望能帮助到各位入门具身智能的朋友, 欢迎点Star、分享与提PR🌟~<br>【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Embodied-AI-Guide</a>, Latest Update: May. 1, 2025 】<img alt="GitHub repo stars" src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide"> ![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FTianxingChen%2FEmbodied-AI-Guide&label=Daily%20Visitors&labelColor=%232ccce4&countColor=%23d9e3f0)


# Lumina具身智能社区: [点击访问](https://lumina-embodied.ai)

> Embodied-AI-Guide项目很快将会以网页版wiki的形式上传到Lumina具身智能社区网站，敬请期待。如果你对合作构建Lumina具身社区感兴趣（目前更倾向于机构、社区间合作），欢迎邮件联系<a href="mailto:lumina.embodiedai@gmail.com">lumina.embodiedai@gmail.com</a>或联创微信<code>TianxingChen_2002</code>（请备注机构+姓名与来意）

**扫描右下图关注`Lumina具身智能`社区**:

<img src="./files/images/Lumina.png" alt="Task Descriptions">


# Contents - 目录

<nav>
  <ul>
    <li><a href="#start">1. Start From Here - 从这里开始</a></li>
    <li><a href="#info">2. Useful Info - 有利于搭建认知的资料</a></li>
    <li><a href="#algorithm">3. Algorithm - 算法</a>
      <ul>
        <li><a href="#common-tools">3.1 Common Tools - 常用工具</a></li>
        <li><a href="#foundation-models">3.2 Foundation Models - 基础模型</a></li>
        <li><a href="#robot-learning">3.3 Robot Learning - 机器人学习</a>
          <ul>
            <li><a href="#robot_autonomy">3.3.1 ETH & TTIC & UdeM Robot Autonomy - 自主机器人</a></li>
            <li><a href="#mpc">3.3.2 Model Predictive Control - 模型预测控制</a></li>
            <li><a href="#rl">3.3.3 Reinforcement Learning - 强化学习</a></li>
            <li><a href="#il">3.3.4 Imitation Learning - 仿人学习</a></li>
            <li><a href="#mila_robot_learning">3.3.5 MILA & UdeM Robot Learning - 机器人学习课程</a></li>
            <li><a href="#cmu_robot_learning">3.3.6 CMU 16-831 Introduction to Robot Learning - 机器人学习导论</a></li>
            <li><a href="#usc_robot_learning">3.3.7 USC CSCI 699: Robot Learning - 机器人学习</a></li>
            <li><a href="#mit_robot_manipulation">3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - 机器人操作</a></li>
            <li><a href="#underactuated_robotics">3.3.9 MIT 6.8210: Underactuated Robotics - 欠驱动机器人</a></li>
          </ul>
        </li>
        <li><a href="#llm_robot">3.4 LLM for Robotics - 大语言模型在机器人学中的应用</a></li>
        <li><a href="#vla">3.5 Vision-Language-Action Models - VLA模型</li>
        <li><a href="#cv">3.6 Computer Vision - 计算机视觉</a>
          <ul>
            <li><a href="#2dv">3.6.1 2D Vision - 二维视觉</a></li>
            <li><a href="#3dv">3.6.2 3D Vision - 三维视觉</a></li>
            <li><a href="#4dv">3.6.3 4D Vision - 四维视觉</a></li>
            <li><a href="#vp">3.6.4 Visual Prompting - 视觉提示</a></li>
            <li><a href="#ag">3.6.5 Affordance Grounding - 可供性锚定</a></li>
          </ul>
        </li>
        <li><a href="#cg">3.7 Computer Graphics - 计算机图形学</a></li>  
        <li><a href="#mm">3.8 Multimodal Models - 多模态模型</a></li>  
        <li><a href="#navigation">3.9 Robot Navigation - 机器人巡航</a></li>  
        <li><a href="#embodied-ai-4-x">3.10 Embodied AI for X - 具身智能+X</a>
          <ul>
            <li><a href="#medical">3.10.1 EAI for Healthcare - 具身医疗</a></li>
            <li><a href="#uav">3.10.2 UAV - 无人机</a></li>
            <li><a href="#ad">3.10.3 Autonomous Driving - 自动驾驶</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#control">4 Control and Robotics - 控制论与机器人学基础</a>
      <ul>
        <li><a href="#41-控制理论基础">4.1 控制理论基础</li>
        <ul>
          <li><a href="#411-经典控制原理">4.1.1 经典控制原理</li>
          <li><a href="#412-现代控制理论线性系统控制">4.1.2 现代控制理论(线性系统控制)</li>
          <li><a href="#413-先进控制技术">4.1.3 先进控制技术</li>
        </ul>
        <li><a href="#42-机器人学导论">4.2 机器人学导论</li>
        <ul>
          <li><a href="#421-推荐材料">4.2.1 推荐资料</li>
          <li><a href="#422-机器人运动学-kinematics-与动力学-dynamics">4.2.2 机器人运动学与动力学</li>
          <li><a href="#423-里程计和同步定位与建图-odometryslam">4.2.3 里程计和同步定位与建图 (Odometry&SLAM)</li>
          <li><a href="#424-杂项-misc">4.2.4 杂项</li>
        </ul>
      </ul>
    </li> 
    <li><a href="#hardware">5. Hardware - 硬件</a>
      <ul>
        <li><a href="#embedded">5.1 Embedded - 嵌入式</a></li>
        <li><a href="#mechanical">5.2 Mechanical Design - 机械设计</a></li>
        <li><a href="#robosystem">5.3 Robot System Design - 机器人系统设计</a></li>
        <li><a href="#sensors">5.4 Sensors - 传感器</a></li>
        <li><a href="#tactile">5.5 Tactile Sensing - 触觉感知</a></li>
        <li><a href="#companies">5.6 Companies - 公司</a></li>
      </ul>
    </li>
    <li><a href="#software">6. Software - 软件</a>
      <ul>
        <li><a href="#simulators">6.1 Simulators - 仿真器</a></li>
        <li><a href="#benchmarks">6.2 Benchmarks - 基准集</a></li>
        <li><a href="#datasets">6.3 Datasets - 数据集</a></li>
      </ul>
    </li>
    <li><a href="#paper_list">7. Paper Lists - 论文列表</a></li>
    <li><a href="#acknowledgement">8. Acknowledgement - 致谢</a></li>
    <li><a href="#cite">👍 Citation - 引用</a></li>
    <li><a href="#license">🏷️ License - 许可证</a></li>
    <li><a href="#star-history">⭐️ Star History - Star历史</a></li>
  </ul>
</nav>



<section id="start"></section>

# 1. Start From Here - 从这里开始

> 具身智能是指一种基于物理身体进行感知和行动的智能系统, 其通过智能体与环境的交互获取信息、理解问题、做出决策并实现行动, 从而产生智能行为和适应性。

## How - 如何学习这份指南

我们希望的是帮助新人快速建立领域认知, 所以设计理念是：**简要**介绍目前具身智能涉及到的主要技术, 让大家知道不同的技术能够解决什么问题, 未来想要深入发展的时候能够有头绪。

## About us - 关于我们
我们是一个由具身初学者组成的团队, 希望能够通过我们自己的学习经验, 为后来者提供一些帮助, 加快具身智能的普及。欢迎更多朋友加入我们的项目, 也很欢迎交友、学术合作, 有任何问题, 可以联系邮箱`chentianxing2002@gmail.com`。

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (深大BS)</a>, <a href="https://github.com/kxwangzju">王开炫 (25' 港大PhD)</a>, <a href="https://jiayueru.github.io/">贾越如 (北大Ms)</a >, <a href="https://metaphysicist0.github.io/">姚天亮 (25' 港中文PhD)</a>, <a href="https://c7w.tech/about/">高焕昂 (清华PhD)</a>, <a href="https://axi404.top/">高宁 (西交BS)</a>, <a href="https://github.com/guo-cq">郭常青 (清华Ms)</a>, <a href="https://shijiapeng03.github.io/">彭时佳 (深大BS)</a>, <a href="https://yudezou.github.io/">邹誉德 (25' 上交AILab联培PhD)</a>, <a href="">陈思翔 (25' 北大PhD)</a>, <a href="https://github.com/csyufei">朱宇飞 (25' 上科大Ms)</a>, <a href="https://github.com/LambdaGuard">韩翊飞 (清华Ms)</a>, <a href="https://hao-starrr.github.io/">王文灏 (宾大Ms)</a>, <a href="https://github.com/StarCycle">李卓恒 (港大PhD)</a>, <a href="https://github.com/GihhArwtw">邱一航 (港大PhD)</a>, <a href="https://github.com/Henry-lsy">梁升一 (港科广PhD)</a>, <a href="https://scholar.google.com/citations?user=azPXbWcAAAAJ&hl=en">林俊晓 (浙大Ms)</a>, <a href="https://gkw0010.github.io/">王冠锟 (港中文PhD)</a>, <a href="https://ngchikit.github.io">吴志杰 (港中文PhD)</a>, <a href="https://github.com/27yw">叶雯 (25' 中科院PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (深大BS)</a>, <a href="https://hbhalpha.github.io">侯博涵 (山大BS)</a>, <a href="https://github.com/Scodive">江恒乐 (25‘ 南科大PhD)</a>, <a href="https://yongchao98.github.io/YongchaoChen/">陈勇超 (MIT+哈佛PhD)</a>, <a href="https://aaron617.github.io/">胡梦康 (港大PhD)</a>, <a href="https://liang-zx.github.io/">梁志烜 (港大PhD)</a>, <a href="https://yimouwu.github.io/">吴贻谋 (港中文MPhil)</a>, <a href="https://warshallrho.github.io/">吴睿海 (北大博士)</a>, <a href="https://yaomarkmu.github.io/">穆尧 (上交AP)</a>.</p> 

<a href="https://github.com/TianxingChen/Embodied-AI-Guide/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=TianxingChen/Embodied-AI-Guide" />
</a>

<section id="info"></section>

# 2. Useful Info - 有利于搭建认知的资料

* 具身智能基础技术路线-YunlongDong [2]: [PDF](./files/具身智能基础技术路线-YunlongDong.pdf), [bilibili](https://www.bilibili.com/video/BV1d5ukedEsi)

* 社交媒体:

  * 可以关注的公众号: **石麻日记 (超高质量!!!)**, 机器之心, 新智元, 量子位, Xbot具身知识库, 具身智能之心, 自动驾驶之心, 3D视觉工坊, 将门创投, RLCN强化学习研究, CVHub

  * AI领域值得关注的博主列表 [3]: [zhihu](https://zhuanlan.zhihu.com/p/682110383)

* Robotics实验室总结 [4]: [zhihu_1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608), [zhihu_2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)

* 具身智能会投稿的较高质量会议与期刊：Science Robotics, TRO, IJRR, JFR, RSS, IROS, ICRA, ICCV, ECCV, ICML, CVPR, NeurIPS, ICLR, AAAI, ACL等。

* 斯坦福机器人学导论：[website](https://www.bilibili.com/video/BV17T421k78T)

* 共建全网最全具身智能知识库 [6]: [website](https://yv6uc1awtjc.feishu.cn/wiki/WPTzw9ON0ivIVrkLjVocNZh8nLf)

* Awesome-Embodied-AI-Job (具身智能招贤榜): [Repo](https://github.com/StarCycle/Awesome-Embodied-AI-Job/tree/main)

* 具身智能华人高引榜: [Repo](https://github.com/Will-Gao/Embodied_Intelligence)
  
* 社区:
  * Lumina具身智能社区: [website](https://lumina-embodied.ai)
  * DeepTimber Robotics Innovations Community, 深木科研交流社区: [website](https://gamma.app/public/DeepTimber-Robotics-Innovations-Community-A-Community-for-Multi-m-og0uv8mswl1a3q7?mode=doc)
  * 宇树具身智能社群: [website](https://www.unifolm.com/#/)
  * Simulately: Handy information and resources for physics simulators for robot learning research: [website](https://simulately.wiki/)
  * DeepTimber-地瓜机器人社区: [website](https://developer.d-robotics.cc/forumList?id=156&title=Deeptimber)
  * HuggingFace LeRobot (Europe, check the Discord): [website](https://github.com/huggingface/lerobot)
  * K-scale labs (US, check the Discord): [website](https://kscale.dev/)

<section id="algorithm"></section>

# 3. Algorithm - 算法

<section id="common-tools"></section>

## 3.1 Common Tools - 常用工具

> 这个部分是关于具身中常用技巧的分享

* 点云降采样: [zhihu](https://zhuanlan.zhihu.com/p/558683732?utm_campaign=shareopn&utm_medium=social&utm_psn=1772067996070236160&utm_source=wechat_session), 包括随机降采样、均匀降采样、最远点降采样、法线空间降采样等, 需要了解清楚每一种降采样的优劣, 这个技巧的选择对于3D应用来说是至关重要的。
* 手眼标定：[github](https://github.com/fishros/handeye-calib), 手眼标定用于确定相机和机械臂之间以及相机与相机之间的相对位置, 大部分Project的开始都需要做一次手眼标定, 分为眼在手上和眼在手外。


<section id="foundation-models"></section>

## 3.2 Vision Foundation Models - 视觉基础模型

> 以下是部分具身智能中常用的基础模型, 计算机视觉中发展的非常好的工具可以直接赋能具身智能的下游应用。

* CLIP: [website](https://github.com/openai/CLIP), 来自OpenAI的研究, 最基本的应用是可以计算图像与语言描述的相似度, 中间层的视觉特征对各种下游应用非常有帮助。

* DINO: [DINO repo](https://github.com/facebookresearch/dino), [DINO-v2 repo](https://github.com/facebookresearch/dinov2), 来自Meta的研究, 可以提供图像的高层视觉特征, 对corresponding之类的信息提取非常有帮助, 比如不同个体之间的鼻子都有类似的几何特征, 这个时候不同图像中关于不同鼻子的视觉特征值可能是近似的。

* SAM: [website](https://segment-anything.com/), 来自Meta的研究, 可以基于提示点或者框, 对图像的物体进行分割。

* SAM2: [website](https://ai.meta.com/sam2/), 来自Meta的研究, SAM的升级版, 可以在视频层面持续对物体进行分割追踪。

* Grounding-DINO: [repo](https://github.com/IDEA-Research/GroundingDINO), [在线尝试](https://deepdataspace.com/playground/grounding_dino), **这个DINO与上面Meta的DINO没有关系**, 是一个由IDEA研究院(做了很多不错开源项目的机构)开发集成的图像目标检测的框架, 很多时候需要对目标物体进行检测的时候可以考虑使用。

* OmDet-Turbo: [repo](https://github.com/om-ai-lab/OmDet), 一个由OmAI Lab开源的研究, 提供OVD（开放词表目标检测）能力, 优点在于推理速度非常快（100+FPS）, 适合需要高FPS的自定义目标物体检测场景。

* Grounded-SAM: [repo](https://github.com/IDEA-Research/Grounded-SAM-2), 比Grounding-DINO多了一个分割功能, 也就是支持检测后分割, 也有很多下游应用, 具体可以翻一下README。

* FoundationPose: [website](https://github.com/NVlabs/FoundationPose), 来自Nvidia的研究, 物体姿态追踪模型。

* Stable Diffusion: [repo](https://github.com/CompVis/stable-diffusion), [website](https://ommer-lab.com/research/latent-diffusion-models/), 22年的文生图模型, 现在虽然不是SOTA了, 但是依然可以作为不错的应用, 例如中间层特征支持下游应用、生成Goal Image (目标状态) 等等。

* Depth Anything (v1 & v2): [repo](https://github.com/LiheYoung/Depth-Anything), [repo](https://github.com/DepthAnything/Depth-Anything-V2), 港大和字节的研究工作, 单目深度估计模型。

* Point Transformer (v3): [repo](https://github.com/Pointcept/PointTransformerV3), 点云特征提取的工作。

* RDT-1B: [website](https://rdt-robotics.github.io/rdt-robotics/), 清华朱军老师团队的工作, 机器人双臂操作的基础模型, 具有强大的few-shot能力。

* SigLIP: [huggingface](https://huggingface.co/docs/transformers/en/model_doc/siglip), 类似CLIP。

<section id="robot-learning"></section>

## 3.3 Robot Learning - 机器人学习

机器人学习 Robot Learning 的发展: [zhihu](https://zhuanlan.zhihu.com/p/26988866)

<section id="robot_autonomy"></section>

### 3.3.1 ETH & TTIC & UdeM Robot Autonomy - 自主机器人

[课程视频](https://www.edx.org/learn/technology/eth-zurich-self-driving-cars-with-duckietown) ｜ [课程网站](https://duckietown.com/self-driving-cars-with-duckietown-mooc/)

该课程由ETH苏黎世、TTIC与蒙特利尔大学联合开设，围绕Duckietown平台系统讲解自主机器人的构建过程，涵盖感知、控制、建模、强化学习等模块。强调完整的感知-决策-控制闭环系统设计，并通过项目实践推动学生掌握从0构建并部署一个具备自主导航能力的机器人智能体。适合希望初步了解机器人系统和Robot Learning的人。

<section id="mpc"></section>

### 3.3.2 Model Predictive Control (MPC) - 模型预测控制

模型预测控制（MPC）是一种先进的控制策略，利用系统的显式动态模型预测有限时间范围内的未来行为。每个控制周期，MPC 通过求解优化问题来确定控制输入，以优化指定的性能指标，同时满足输入和输出的约束条件。优化序列中的第一个控制输入应用于系统，在下一个时间步中，结合新的系统状态测量或估计，重复该过程。

* 入门推荐视频：

    - Model Predictive Control 模型预测控制,从公式到代码 - 华工机器人实验室: [bilibili](https://www.bilibili.com/video/BV1U54y1J7wh); 仿真工程源码:[Gitee](https://gitee.com/clangwu/mpc_control.git) 这门课程适合作为从PID到MPC的入门课程，适合只了解PID控制原理，但不太清楚MPC原理的入门者；从公式原理推导，到CoppeliaSim（V-ERP）仿真教程以及MatLab代码编写，深入浅出。
    
* 经典工作：
  
    **理论基础**：
    - [Model predictive control: Theory and practice—A survey](https://www.sciencedirect.com/science/article/abs/pii/0005109889900022) ： 这篇全面的综述论文讨论了 MPC 的理论基础及其实践应用，为未来的研究奠定了基础。

    **非线性 MPC**：
    - [An Introduction to Nonlinear Model Predictive Control](https://pure.tue.nl/ws/files/3079152/555518.pdf#page=120) ： 提供了对非线性 MPC 的简明介绍，扩展了 MPC 在具有显著非线性系统中的应用。

    **显式 MPC**：
    - [The explicit linear quadratic regulator for constrained systems](https://www.sciencedirect.com/science/article/abs/pii/S0005109801001741) ： 讨论了显式 MPC 解的公式化，对于需要快速实时控制的系统至关重要。

    **鲁棒 MPC**：
    - [Predictive End-Effector Control of Manipulators on Moving Platforms Under Disturbance](https://ieeexplore.ieee.org/document/9425004) ： 使用时间序列分析预测基座运动并相应地转换期望轨迹，使得机械臂可以达到主动在扰动下的基座运动。是使用二次规划（QP）公式化模型预测控制（MPC）问题的经典之作。
    - [Min-max feedback model predictive control for constrained linear systems](https://ieeexplore.ieee.org/abstract/document/704989) ： 解决了 MPC 中的鲁棒性，提出了处理模型不确定性并确保在扰动下性能的方法。

    **基于学习的MPC**：
    - [Learning-Based Model Predictive Control for Safe Exploration](https://ieeexplore.ieee.org/abstract/document/8619572) ： 将机器学习与 MPC 相结合，代表了将数据驱动的模型和学习纳入控制的现代趋势。
    - [Confidence-Aware Object Capture for a Manipulator Subject to Floating-Base Disturbances](https://ieeexplore.ieee.org/document/10684104) ： 利用小波神经网络进行实时运动预测，并且引入置信度评价，实现短周期内最优轨迹规划，使得机械臂在扰动平面上抓取无人机（UAV）表现优异，具备良好的鲁棒性。

<section id="rl"></section>

### 3.3.3 Reinforcement Learning - 强化学习

* 强化学习的数学原理 - 西湖大学赵世钰: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665) [GitHub](https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning) 这门课程作为强化学习的入门课程非常合适，适合只对机器学习略有了解，但没有了解过强化学习的初学者，可以了解强化学习的数学原理，其教材编写也十分用心。

#### Deep Reinforcement Learning - 深度强化学习

下面列出三门比较受欢迎的深度强化学习相关的课程，这几门课互有overlap，时间长短和授课风格也各有不同，读者可以选择适合自己的课程进行学习。此外，深度强化学习的经典算法相关的文章也在必读清单：如[PPO](https://arxiv.org/abs/1707.06347), [SAC](https://proceedings.mlr.press/v80/haarnoja18b/haarnoja18b.pdf), [TRPO](https://arxiv.org/abs/1502.05477), [A3C](https://arxiv.org/abs/1602.01783)等。

* The Foundations of Deep RL in 6 Lectures [YouTube](https://www.youtube.com/watch?v=2GwBez0D20A) 本门在线课程由在RL领域著名的Pieter Abbeel教授主讲，从MDP开始在六节课之内介绍了深度强化学习的主要知识。

* UC Berkeley CS285 深度强化学习: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [YouTube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps) 本课程的主讲老师是在RL领域著名的Berkeley的Sergey Levine教授，DRL领域许多著名的工作如SAC就出自他之手。Sergey在授课方面非常用心，本课程对DRL提供了非常详细的介绍。

* 李宏毅老师也有一套关于强化学习的课程: bilibili上课+刷蘑菇书巩固+gymnasium动手实践, 重点了解一下PPO。

  * 台湾大学李宏毅公开课: [bilibili](https://www.bilibili.com/video/BV1XP4y1d7Bk)

  * EasyRL - 蘑菇书: [website](https://datawhalechina.github.io/easy-rl/#/), 基本是配套李宏毅老师的课程

  * 实践[gymnasium](https://gymnasium.farama.org/), 可以尝试一下把玩一下登月着陆等经典强化学习场景, 思考+动手, 观察阶段agent的表现并分析, 有助于深入理解强化学习

然而，深度强化学习的Reward Tuning和参数调整非常依赖于经验，建议读者在对深度强化学习有相关经验之后，可以自己尝试训练一个policy并在机器人上部署，体会其中的Sim-to-Real Gap。常用的仿真平台有[MuJoCo PlayGround](https://playground.mujoco.org/), [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html), [SAPIEN](https://sapien.ucsd.edu/), [Genesis](https://github.com/Genesis-Embodied-AI/Genesis)等。

常用的Codebase有[legged-gym](https://github.com/leggedrobotics/legged_gym)(由ETH RSL开发，基于IsaacGym)等，也可以根据你想做的任务找到相近的codebase。

<section id="il"></section>

### 3.3.4 Imitation Learning - 模仿学习

* 《模仿学习简洁教程》 - 南京大学LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
* Supervised Policy Learning for Real Robots, RSS 2024 Workshop 教程：真实机器人的监督策略学习, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if)

<section id="mila_robot_learning"></section>

### 3.3.5 MILA & UdeM Robot Learning - 机器人学习课程

[课程视频](https://www.youtube.com/playlist?list=PLMe2pHxzxHp-UJ1jd-uuGSGK7P7Phtm-f) ｜ [课程网站](https://fracturedplane.notion.site/Robot-Learning-IFT6163-Scaling-Learning-for-Real-World-Agents-Apprentissage-robotique-Apprentiss-14a2148572768017864af202952c4b7e)

由MILA和蒙特利尔大学开设的课程，聚焦于将深度强化学习等方法扩展到现实世界中的机器人智能体，重点探讨了现有学习技术的局限，并研究如何构建更强健、泛化能力更强的智能体系统。适合希望了解机器学习，强化学习算法在机器人领域的前沿应用的同学。

<section id="cmu_robot_learning"></section>

### 3.3.6 CMU 16-831 Introduction to Robot Learning - 机器人学习导论

[课件](https://16-831-s24.github.io/lectures/) ｜ [作业](https://github.com/kavin-cmu/16831-S24-HW)

由CMU Robotics Institute开设的课程，虽然没有视频，但是课件内容简明扼要，对整个Robot Learning有比较全面的覆盖，而且内容insights很强，十分推荐学习。

<section id="usc_robot_learning"></section>

### 3.3.7 USC CSCI 699: Robot Learning - 机器人学习

[课程主页](https://liralab.usc.edu/csci699/)

由南加州开设的课程，RL相关内容很丰富，注重概念之间的联系，有很多intuition。

<section id="mit_robot_manipulation"></section>

### 3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - 机器人操作

[课程主页](https://manipulation.csail.mit.edu/Fall2024/index.html) | [电子书](https://manipulation.mit.edu/)

由MIT CSAI开设的课程，内容丰富且硬核，对机器人操作有比较全面的介绍，包含感知、规划、动力学和控制。建议前置课程有：数学、编程、机器学习、机器人导论。

<section id="underactuated_robotics"></section>

### 3.3.9 MIT 6.8210: Underactuated Robotics - 欠驱动机器人

[课程主页](https://underactuated.csail.mit.edu/Spring2024/index.html) | [课程视频](https://www.youtube.com/watch?v=v04rn86Dehg&t=4319s)

由MIT CSAI开设的课程，介绍非线性动力学和欠驱动机械系统的控制。有Youtube视频，且录制质量很高。

<section id="llm_robot"></section>

## 3.4 LLM for Robotics - 大语言模型在机器人学中的应用
为了促使机器人更好的规划, 现代具身智能工作常常利用大语言模型强大的信息处理能力与泛化能力进行规划。
* Robotics+LLM系列通过大语言模型控制机器人 [2]: [zhihu](https://zhuanlan.zhihu.com/p/668053911)<br>
* Embodied Agent wiki: [website](https://en.wikipedia.org/wiki/Embodied_agent)<br>
* Lilian Weng 个人博客 - AI Agent 系统综述 [5]: 中文: [website](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) 英文: [website](https://lilianweng.github.io/posts/2023-06-23-agent/)<br>
* 过去一系列工作常常仅使用LLM作为High-Level的策略生成器 用作High-Level 规划
  * 经典工作(1) PaLM-E: [Arxiv](https://arxiv.org/abs/2303.03378)<br>
  * 经典工作(2) DO AS I CAN, NOT AS I SAY: [Arxiv](https://arxiv.org/abs/2204.01691)<br>
  * 经典工作(3) Look Before You Leap: [Arxiv](https://arxiv.org/abs/2311.17842)<br>
  * 经典工作(4) EmbodiedGPT: [Arxiv](https://arxiv.org/abs/2305.15021)<br>
* 同时也有一些工作将High-Level的策略规划与 Low-Level的动作生成进行统一
  * 经典工作(1) RT-2: [Arxiv](https://arxiv.org/abs/2307.15818)<br>
* 另一个代表性方向的工作将LLM与传统基于算法的Planner结合来做任务与移动规划
  * 经典工作(1) LLM+P: [Arxiv](https://arxiv.org/abs/2304.11477)<br>
  * 经典工作(2) AutoTAMP: [Arxiv](https://arxiv.org/abs/2306.06531)<br>
  * 经典工作(3) Text2Motion: [Arxiv](https://arxiv.org/abs/2303.12153)<br>
* 利用LLM的code能力实现具身智能是一个有趣的想法
  * 经典工作(1) Code as Policy: [Arxiv](https://arxiv.org/abs/2209.07753)<br>
  * 经典工作(2) Instruction2Act: [Arxiv](https://arxiv.org/abs/2305.11176)<br>
* 有一些工作将三维视觉感知同LLM结合起来，共同促进具身智能规划
  * VoxPoser [Arxiv](https://arxiv.org/abs/2307.05973)<br>
  * OmniManip [Arxiv](https://arxiv.org/abs/2501.03841)<br>
* 还有一些工作试图把基于LLM的机器人规划扩展到多机器人协同合作的场景
  * 经典工作(1) RoCo: [Arxiv](https://arxiv.org/abs/2307.04738)<br>
  * 经典工作(2) Scalable-Multi-Robot: [Arxiv](https://arxiv.org/abs/2309.15943)<br>

<section id="vla"></section>

## 3.5 Vision-Language-Action Models - VLA模型
**Vision-Language-Action Models(VLA模型)** 是一种结合VLM(Vision-Language Model)与机器人控制的模型，旨在将预训练的VLM直接用于生成机器人动作(RT-2中定义)。和以往利用VLM做planning以及build from strach的方法不同，VLA无需重新设计新的架构，将动作转化为token，微调VLM。

**VLA的特点**：端到端，使用LLM/VLM backbone，加载预训练模型, etc. 

目前的VLA可以从以下几个方面进行区分：模型结构&大小(如action head的设计, tokenize的方法如FAST)，预训练与微调策略和数据集，输入和输出(2D vs. 3D | TraceVLA输入visual trace)，不同的应用场景等。

**参考资料：**

* Blog:  [具身智能Vision-Language-Action的思考](https://zhuanlan.zhihu.com/p/9880769870), [zhihu](https://www.zhihu.com/question/655570660/answer/87040917575)

* Survey: [A Survey on Vision-Language-Action Models for Embodied AI](https://arxiv.org/abs/2405.14093), 2024.11.28

### **3.5.1 经典工作**：

* **Autoregressive Models**

  - **RT系列(Robotic Transformers)**:
    - **RT-1** ([paper](https://arxiv.org/abs/2212.06817))
    - **RT-2** ([page](https://robotics-transformer2.github.io/) | [paper](https://arxiv.org/abs/2307.15818), Google Deepmind, 2023.7)：55B
    - **RT-Trajectory** ([paper](https://arxiv.org/pdf/2311.01977), Google Deepmind, UCSD, 斯坦福 2023.11)
    - **AUTORT** ([paper](https://arxiv.org/abs/2401.12963), Google Deepmind, 2024.1)

  - **RoboFlamingo** ([paper](https://arxiv.org/abs/2311.01378) | [code](https://github.com/roboflamingo), 字节、清华, 2024.2)

  - **OpenVLA** ([paper](https://arxiv.org/pdf/2406.09246) | [code](https://github.com/openvla), Stanford, 2024.6): 7B

  - **TinyVLA** ([paper](https://arxiv.org/abs/2409.12514), 上海大学, 2024.11)
  - **TraceVLA** ([paper](https://arxiv.org/pdf/2412.10345) | [code](https://github.com/umd-huang-lab/tracevla), 微软，2024.12)

* **Diffusion Models for Action Head:**

  - **Octo** ([paper](https://arxiv.org/pdf/2405.12213) | [code](https://octo-models.github.io/), 斯坦福，伯克利, 2024.5): Octo-base (93M)

  - **π0** ([paper](https://arxiv.org/pdf/2410.24164) | [code](https://github.com/Physical-Intelligence/openpi), 斯坦福, physical intelligence, ) : 3.3B; flow-based diffusion VLA; PaliGemma (3B VLM);

  - **CogACT** ([paper](https://arxiv.org/pdf/2411.19650) | [code](https://github.com/microsoft/CogACT.git), 清华，MSRA, 2024.11): 7B

  - **Diffusion-VLA** ([paper](https://arxiv.org/abs/2412.03293) | [code](https://arxiv.org/pdf/2410.07864), 华东师范，上海大学，美的, 2024.12)

* **3D Vision:**
  - **3D-VLA** ([paper](https://arxiv.org/pdf/2403.09631) | [code](https://github.com/UMass-Foundation-Model/3D-VLA/tree/main), UMass, 2024.3): 3D-based LLM
  - **SpatialVLA** ([paper](https://arxiv.org/pdf/2501.15830) | [code](https://github.com/SpatialVLA/SpatialVLA) , 上海AI Lab, 2025.1): Adaptive Action Grid

* **VLA-related:**

  - **FAST (π0)** ([paper](https://arxiv.org/pdf/2410.24164), [code](https://github.com/Physical-Intelligence/openpi.git), 斯坦福，伯克利, physical intelligence, 2025.1):  autoregressive VLA

  - **RLDG** ([paper](https://generalist-distillation.github.io/static/high_performance_generalist.pdf) | [code](https://arxiv.org/abs/2410.01971), 伯克利, 2024.12 ): 强化学习(RL)生成高质量的训练数据进行微调

  - **BYO-VLA** ([paper](https://arxiv.org/abs/2410.01971) | [code](https://github.com/irom-princeton/byovla), 普林斯顿大学, 2024.10): 运行时图像干预，有效降低VLA模型对任务无关视觉干扰的敏感度

* **Different Locomotion:**

  - **RDT-1B (双臂)** ([paper](https://arxiv.org/pdf/2410.07864) | [code](https://github.com/thu-ml/RoboticsDiffusionTransformer), 清华): 双臂控制的扩散模型

  - **QUAR-VLA (四足机器人)** ([paper](https://arxiv.org/pdf/2312.14457), 西湖大学，浙江大学, 2025.2.4)

  - **CoVLA (自动驾驶)** ([paper](https://arxiv.org/abs/2408.10845) | [page](https://turingmotors.github.io/covla-ad/), Turing, 2024.12)

  - **Mobility-VLA (导航)** ([paper](https://arxiv.org/pdf/2407.07775), Google Deepmind, 2024.7)

  - **NaVILA (腿式机器人导航)** ([paper](https://arxiv.org/pdf/2412.04453) | [code](https://navila-bot.github.io/), USCD, 2024.12)

### **3.5.2 双系统分层VLA**：（2025.5更新） ⭐

目前VLA的一大范式是采用分层双系统架构，模拟人类的快速反应（System 1）和深度思考（System 2）机制。System 2 利用视觉语言模型（VLM）进行环境理解和任务规划，接收视觉、语言等多模态输入，并通过语言或潜在向量（Latent Vector）将信息传递给 System 1。System 1 则将这些规划转化为精确的机器人动作。
目前，采用双系统架构的主要区别在于：
- *单模型 vs 双模型架构*：例如，Hi-Robot 采用了 VLM + VLA 的双模型架构，而 pi-0.5 则采用了单模型架构。
- *快慢系统的通信方式*：快慢系统在何时分层，通信可以通过低级指令（low-level command）或潜在向量（latent vector）进行。
- *仿真训练数据的使用*：如 GROOT N-1 使用了模拟器数据和合成数据，而 pi 系列则完全依赖于真实机器人数据。
- 在*模型表现*方面，可以关注以下几个方面：模型大小、动作输出频率以及任务的难度（如人形、长程任务、柔性物体处理、跨本体性能等）。

**产业级VLA**：

- **Figure: Helix** (link: [Figure](https://www.figure.ai/news/helix), 2025.2.20): 机器人全身上半身控制
- **智元：GO-1** (link: [智元官网](https://www.zhiyuan-robot.com/article/189/detail/56.html), 2025.3.10)：ViLLA: VLM+MoE, vision-language-latent-action model
- **Physical Intelligence** : code https://github.com/Physical-Intelligence/openpi
  - **pi-0.5** ([paper](https://arxiv.org/abs/2504.16054) | blog: CSDN, 2025.4.22): 高级任务分解后由单一模型执行低级任务
  - **Hi Robot** ([paper](https://arxiv.org/abs/2502.19417) | blog: CSDN, 2025.2.26): 使用VLM进行高级推理，VLA执行低级任务
- **Nvidia: GROOT-N1** (code: [Nvidia Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) | [paper](https://arxiv.org/abs/2503.14734) | blog, 2025.3.27): 机器人全身控制, 2B, NVIDIA-Eagle架构和SmolLM-1.7B
- **灵初智能：Psi-R1** ([blog](https://www.jiqizhixin.com/articles/2025-03-03-9), 2025.4.27): 分层端到端VLA+强化学习算法模型, 验证test-time scaling
- **Google DeepMind: Gemini Robotics** ([paper](https://arxiv.org/pdf/2503.20020), 2025.3.25): Gemini 2.0构建的Gemini Robotics-ER（具身推理模型）和Gemini Robotics主模型, 50 Hz

**最新VLA工作**：
- **SafeVLA** ([paper](https://arxiv.org/abs/2503.03480) | [code](https://github.com/PKU-Alignment/SafeVLA), 北大, 2025.3.5): 解决传统VLA模型在抓取和导航任务中的不安全行为
- **HybridVLA** ([paper](https://arxiv.org/pdf/2503.10631) | [code](https://github.com/PKU-HMI-Lab/Hybrid-VLA), 北大, 2025.3.17): 用统一模型集成扩散和自回归动作预测，2.7B 和 7B模型
- **DexVLA** ([paper](https://arxiv.org/pdf/2502.05855) | [code](https://github.com/juruobenruo/DexVLA), 美的, 东南大学, 2025.2.9): Diffusion expert 1B，采用多个action head
- **DexGraspVLA** ([paper](https://arxiv.org/abs/2502.20900) | [code](https://github.com/Psi-Robot/DexGraspVLA), 北大, 2025.2.28): 灵巧手抓取VLA
- **UP-VLA** ([paper](https://arxiv.org/pdf/2501.18867), 清华, 2025.2.3): 加入goal-image预测任务帮助动作生成
- **CoT-VLA** ([paper](https://arxiv.org/pdf/2503.22020) ,  Nvidia, Stanford, CVPR2025): 将CoT融入VLA中，通过自回归地预测未来的图像帧作为视觉目标，7B
- **UniAct** ([paper](https://arxiv.org/abs/2501.10105) | [code](https://github.com/2toinf/UniAct), CVPR2025, 清华): 基于通用动作空间的具身基础模型
- **UniVLA** ([paper](https://arxiv.org/pdf/2505.06111) | [code](https://github.com/OpenDriveLab/UniVLA), 港大, 上海人工智能实验室, 智元, 2025.5.9): 利用潜在动作模型从多样化数据中提取任务核心表征，提升泛化能力，降低计算和数据需求


<section id="cv"></section>

## 3.6 Computer Vision - 计算机视觉

CS231n (斯坦福计算机视觉课程): [website](https://cs231n.stanford.edu/schedule.html), 该课程对深度学习在计算机视觉的应用有较为全面的介绍。因为已经在具体实现某个论文的算法了, 所以这个阶段可以不用做作业, 只需要看课程视频和课程讲义即可。<br>

<section id="2dv"></section>

### 3.6.1 2D Vision - 二维视觉
* 2D Vision 领域的经典代表作
  * CNN (卷积神经网络): [link](https://easyai.tech/ai-definition/cnn/)
  * ResNet (深度残差网络): [bilibili](https://www.bilibili.com/video/BV1P3411y7nn)
  * ViT (第一个将Transformer用在视觉领域): [bilibili](https://www.bilibili.com/video/BV15P4y137jb)
  * Swin Transformer (披着Transformer皮的CNN): [bilibili](https://www.bilibili.com/video/BV13L4y1475U)
  * 对比学习论文综述: [bilibili](https://www.bilibili.com/video/BV19S4y1M7hm)
* 以判别式模型为主的感知任务, 比如识别、分类、分割、检测等等, 看看即可, 现在继续刷点意义不大
* 生成式模型
  * 自回归综述: [PDF](https://arxiv.org/pdf/2411.05902)
  * 扩散模型综述: [PDF](https://arxiv.org/pdf/2209.00796)
  * 如果对扩散模型的理论推导感兴趣, 可以看苏剑林老师的博客 - 生成扩散模型漫谈(推导非常清楚): [link](https://kexue.fm/archives/9119)

<section id="3dv"></section>

### 3.6.2 3D Vision - 三维视觉

* 三维视觉导论 - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) (重点关注课程作业) <br>
* GAMES203 - 三维重建和理解: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS)<br>
* 三维生成的一些经典论文:
  * Diffusion Model for 2D/3D Generation 相关论文分类: [link](https://zhuanlan.zhihu.com/p/617510702)
  * 3D生成相关论文-2024: [link](https://zhuanlan.zhihu.com/p/700895749)

<section id="4dv"></section>

### 3.6.3 4D Vision - 四维视觉
* 视频理解
  * 开山之作: [bilibili](https://www.bilibili.com/video/BV1mq4y1x7RU)
  * 论文串讲: [bilibili](https://www.bilibili.com/video/BV1fL4y157yA)
  * LLM时代的视频理解综述: [PDF](https://arxiv.org/pdf/2312.17432)
* 4D 生成
  * 视频生成博客(英文): [link](https://lilianweng.github.io/posts/2024-04-12-diffusion-video/)
  * 4D 生成的论文列表: [website](https://github.com/cwchenwang/awesome-4d-generation)

<section id="vp"></section>

### 3.6.4 Visual Prompting - 视觉提示

视觉提示是一种利用视觉输入引导大模型完成特定任务的方法，常用于具身智能领域。它通过提供示例图像、标注或视觉线索，让模型理解任务要求，而无需额外训练。例如，在机器人导航、操控等场景中，视觉提示可帮助模型适应新环境，提高泛化能力。相比传统方法，视觉提示具备更强的灵活性和可扩展性，使具身智能系统能够通过视觉信息快速适应复杂任务。

- 视觉提示综述：[paper](https://arxiv.org/abs/2409.15310)
- **PIVOT**, [page](https://pivot-prompt.github.io): 通过将任务转化为迭代式视觉问答，实现在无需特定任务数据微调的情况下，zero-shot控制机器人系统和进行空间推理。
- **Set-of-Mark Visual Prompting for GPT-4V**: [page](https://som-gpt4v.github.io)

<section id="ag"></section>

### 3.6.5 Affordance Grounding - 可供性锚定

可供性锚定任务的目标是从图像中定位物体上能够与之交互的区域，充当了感知与行动之间的桥梁，是具身智能重要的一环。它不仅需要模型对物体及其局部结构的检测与识别，还需要模型理解物体与人或机器人之间的潜在互动关系。例如，在机器人抓取场景中，可供性锚定帮助模型寻找物体上最佳的抓取位置，从而确定最佳抓取角度。该方向通过整合计算机视觉，多模态大模型技术，能够在弱监督或零样本条件下实现对物体交互可能性的精确定位，提升机器人抓取、操作以及人机交互等任务的性能。

* **2D**
  - 跨视角学习可供性：**Cross-View-AG**, [paper](https://arxiv.org/pdf/2203.09905): 第三视角图像提供他者如何与物体交互的信息，帮助模型学习如何与第一视角图像中的物体交互。
  - 单视角学习可供性：**AffordanceLLM**, [paper](https://arxiv.org/pdf/2401.06341)：通过利用预训练的大规模视觉语言模型中的丰富知识，显著提升了物体可供性锚定在未见对象和动作上的泛化能力。
  - 数据集：**AGD20K**, [page](https://github.com/lhc1224/Cross-View-AG)

* **3D**
  - 基于点云的可供性锚定：**OpenAD**, [paper](https://arxiv.org/pdf/2203.09905)
  - 铰接物体的可供性锚定：**Where2Act**, [paper](https://arxiv.org/abs/2101.02692); **VAT-Mart**, [paper](https://openreview.net/pdf?id=iEx3PiooLy)
  - 柔性物体的可供性锚定：**DeformableAffordance**, [paper](https://arxiv.org/pdf/2303.11057); **UniGarmentManip**, [paper](https://arxiv.org/abs/2405.06903)
  - 室内环境任务中的可供性锚定：**SceneFun3D**, [paper](https://arxiv.org/pdf/2401.06341)
  - 点云数据集：**3D AffordanceNet**, [page](https://github.com/lhc1224/Cross-View-AG)，专注于物体层面的可供性锚定。
  - 实物数据集：**SceneFun3D**, [page](https://scenefun3d.github.io/)，强调在真实室内环境的应用。

<section id="cg"></section>

## 3.7 Computer Graphics - 计算机图形学

如果说计算机视觉是考虑图像之间的变化以及从图像到三维模型(三维重建和生成)，那么计算机图形学主要研究的就是三维模型之间的变化以及从三维模型到图像的渲染过程。具身智能在开发和测试的时候离不开仿真器，而仿真也属于图形学的研究范畴。快速、高质量的渲染，并行化、准确的仿真一直是机器人仿真器追求的目标，而这一切通过计算机图形学来实现。

* 如果对传统图形学感兴趣, 可以看下面两门(闫令琪老师开的课, 讲得特别好):<br>
  * **GAMES101 - 现代计算机图形学入门**: [website](https://games-cn.org/intro-graphics/)<br>
  * GAMES202 - 高质量实时渲染: [website](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html)<br>
* 如果对motion synthesis/computer animation感兴趣, 可以看:
  * GAMES105 - 计算机角色动画基础: [website](https://games-105.github.io/)<br>
* 如果对三维重建感兴趣, 可以看下面两门:
  * Nerf原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1CC411V7oq)
  * 3DGS原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1zi421v7Dr)
* 三维预训练最新综述:
  * Advances in 3D pre-training and downstream tasks: a survey: [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>
* 3DGS在具身上的综述:
  * 3D Gaussian Splatting in Robotics: A Survey: [PDF](https://arxiv.org/pdf/2410.12262v2)<br>

<section id="mm"></section>

## 3.8 Multimodal Models - 多模态模型

> 多模态旨在统一来自不同模态信息的表征, 在具身智能中由于面对着机器识别的视觉信息与人类自然语言的引导信息等不同模态的信息，多模态技术愈发重要。
* 最经典的工作CLIP: [知乎](https://zhuanlan.zhihu.com/p/493489688)<br>
* 多模态大语言模型的经典工作 LLaVA: [website](https://llava-vl.github.io/)<br>
* 多模态生成模型综述: [pdf](https://arxiv.org/pdf/2503.04641)<br>
* 多模态大语言模型强化学习项目：VLM-R1: [repo](https://github.com/om-ai-lab/VLM-R1) 来自OmAI Lab的多模态大语言模型DeepSeek R1-style强化学习开源项目，使用GRPO强化学习算法对多模态大语言模型进行优化，效果优于常规sft，是训练具身智能模型的一种新方向。<br>

<section id="navigation"></section>

## 3.9 Robot Navigation - 机器人导航
**机器人导航（Robot Navigation）**是一类要求智能体在**已知或未知**场景中，通过获取并处理环境信息，实现达成某种目标的路径规划。机器人导航是具身任务中的一个重要能力，是完成复杂任务不可缺少的基础技术。机器人导航任务中，智能体一般接受传感器提供的RGB、深度、GPS等信息和相关目标指令，输出是一系列的动作指令。

按照任务类型分类，机器人导航可以分为以下几个部分：

- **物体目标导航（Object-Goal Navigation）**：最常见和最广泛的导航任务。智能体接受的指令是对一个特定物体的描述，目标是找寻到这个物体。
- **图像目标导航（Image-Goal Navigation）**：智能体接受的指令是一个图像，目标是找寻到这个图像所描述的场景。
- **视觉-语言导航（Vision-Language Navigation，VLN）**：智能体接受的指令是一个自然语言指令描述，目标是跟随该指令行进。

按照模型架构分类，机器人导航可以分为以下几个类别：

- **端到端模型（End-to-End Model）**：模型直接将传感器输入通过强化学习或模仿学习映射到动作指令。模型会先将传感器信息编码为视觉表征，结合历史动作作为输入，最后通过与环境交互获得reward实现动作决策的学习。端到端模型主要针对两方面进行优化：一是提升视觉表征能力，二是解决稀疏奖励等动作决策方面的问题。端到端模型的优势在于直截了当，但是面临着严重的过拟合和低泛化性问题，使得其在现实生活中的应用收到了挑战。

    - 经典工作：

        - [Learning Object Relation Graph and Tentative Policy for Visual Navigation](https://arxiv.org/abs/2007.11018)
        - [VTNet: Visual Transformer Network for Object Goal Navigation](https://openreview.net/forum?id=DILxQP08O3B)

- **模块化模型（Modular Model）**：将传感器信息输入不同的模块，模块之间通过接口交互，输出动作指令。模块包括建图模块（Mapping，构建语义和占有地图），长期决策模块（Global Policy，决定长期的导航目标），短期决策模块（Local Policy，决定实现长期目标的具体操作）等。建图模块是模型的核心，包含有网格地图、包含预测的网格地图、图表示地图等多种形式。模块化模型的优势在于模块之间的解耦，大大加强了模型的可解释性。同时，独立的建图模块也使得模型更容易泛化到未知环境。但是模块化模型的建图模块仍然充斥着手动设计的规则，这一定程度上也限制了模型的通用性。
  
    - 经典工作：
      
        - [Object Goal Navigation using Goal-Oriented Semantic Exploration](https://arxiv.org/abs/2007.00643) ： SemExp，最早提出语义地图的概念，学习区域和物体之间关联的语义先验，使智能体能够更好地判断目标物体可能在的方向。
        - [PONI: Potential Functions for ObjectGoal Navigation with Interaction-free Learning](https://openaccess.thecvf.com/content/CVPR2022/papers/Ramakrishnan_PONI_Potential_Functions_for_ObjectGoal_Navigation_With_Interaction-Free_Learning_CVPR_2022_paper.pdf)：PONI，提出了基于potential functions的语义地图预测，即基于已有的语义地图学习“补全”的完整地图，想象物体最可能在整个房间的哪个位置，使智能体能够迁移在其他样本中观察到的知识。
        - [3D-Aware Object Goal Navigation via Simultaneous Exploration and Identification](https://arxiv.org/abs/2212.00338)：把3D信息编码进导航的经典工作，通过更精细的点云分割信息，避免了2D语义图在z轴上的信息损失，实现了更精确的语义地图构建。

- **零样本模型（Zero-shot Model）**：模型不接触训练数据，直接在测试阶段完成任务。零样本模型往往利用具有知识先验的大规模预训练模型（CLIP, LLM等）实现。零样本模型的提出旨在解决基于学习的方法面临的过拟合和低泛化性问题，同时也更适合迁移到现实场景。但是零样本模型的缺陷在于推理速度较慢，且性能受限，需要进一步微调以实现更好的性能。

    - 经典工作：

        - [CoWs on Pasture: Baselines and Benchmarks for Language-Driven Zero-Shot Object Navigation](https://arxiv.org/abs/2203.10421)：开放语义物体导航的提出工作。思路很简单：用CLIP寻找目标物体，找到了就走过去。在不常见物体、复杂描述上取得了很好的效果，同时也有着对不同属性的同类别物体的区分能力。
        - [L3MVN: Leveraging Large Language Models for Visual Target Navigation](https://arxiv.org/abs/2304.05501)：利用LLM决定“我要向哪个边界前进”。利用LLM的人类知识先验，判断物体可能在的房间，以及与其他物体之间的相关关系，实现更快速更有效的导航。
        - [ESC: Exploration with Soft Commonsense Constraints for Zero-shot Object Navigation](https://arxiv.org/abs/2301.13166)：显式提出了区域对于导航的影响，在语义地图上标注出区域占有的位置，作为输入的一部分输入给LLM。结合了语义地图连续性和LLM知识丰富的优势。
        - [SG-Nav: Online 3D Scene Graph Prompting for LLM-based Zero-shot Object Navigation](https://arxiv.org/abs/2410.08189)：在线构建多层场景图(Scene Graph)并输入给LLM，利用CoT实现LLM对于物体位置的推理。

常用数据集：

- [MatterPort3D(MP3D)](https://niessner.github.io/Matterport/)：真实场景采集，场景复杂庞大，数据量大，难度高。
- [Habitat-Matterport3D(HM3D)](https://aihabitat.org/datasets/hm3d/)：同上
- [RoboTHOR](https://ai2thor.allenai.org/robothor/)：仿真环境，场景小简单。


其他参考：

- [物体目标导航综述](https://orca.cardiff.ac.uk/id/eprint/167432/1/ObjectGoalNavigationSurveyTASE.pdf)
- [awesome vision-language navigation](https://github.com/eric-ai-lab/awesome-vision-language-navigation)
- [Habitat Navigation Challenge](https://github.com/facebookresearch/habitat-challenge)(Habitat框架中整合了非常多常见的agent skill，例如语义地图构建，FBE和一些heuristic方法，非常适合模块化方法的开发)

<section id="embodied-ai-4-x"></section>

## 3.10 Embodied AI for X - 具身智能+X

<section id="medical"></section>

### 3.10.1 EAI for Healthcare - 具身医疗

> 具身智能技术的迅猛发展正在引领医疗服务模式迈向革命性的新纪元。作为人工智能算法、先进机器人技术与生物医学深度融合的前沿交叉学科, 具身智能+医疗这一研究领域不仅突破了传统医疗的边界, 更开创了智能化医疗的新范式。其多学科协同创新的特质, 正在重塑医疗服务的全流程, 为精准医疗、远程诊疗和个性化健康管理带来前所未有的发展机遇, 推动医疗行业向更智能、更人性化的方向转型升级。这一领域的突破性进展, 标志着医疗科技正迈向一个全新的智能化时代。
> 
* 医疗具身智能综述: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/abs/2501.07468)<br>

#### 3.10.1.1 MLLM for Medical - 多模态大语言模型在医学中的应用
* 用于医学影像分析的通用人工智能综述: [website](https://arxiv.org/pdf/2306.05480)<br>
* 医学影像的通用分割模型-MedSAM： [website](https://www.nature.com/articles/s41467-024-44824-z.pdf)<br>
* 2024盘点：医学AI大模型, 从通用视觉到医疗影像: [NEJM医学前沿](https://mp.weixin.qq.com/s?__biz=MzIxNTc4NzU0MQ==&mid=2247550230&idx=1&sn=6baa8dcba12f3f70f4c8205a0f23b6a0&chksm=966df4ca45c8cbcaa0a5d2e42fbb4de92e6881f92981071ce7fda3bd1e13e4715f92415a9258&scene=27)<br>
* 医疗领域基础模型的发展机遇与挑战: [website](https://arxiv.org/pdf/2404.03264)<br>
* SkinGPT-4 for dermatological diagnosis: [website](https://www.nature.com/articles/s41467-024-50043-3)<br>
* PneumoLLM for pneumoconiosis diagnosis: [website](https://www.sciencedirect.com/science/article/abs/pii/S1361841524001737)<br>
* BiomedGPT: [website](https://github.com/taokz/BiomedGPT)<br>
* LLaVA-Med: [website](https://github.com/microsoft/LLaVA-Med?tab=readme-ov-file)<br>
* RoboNurse-VLA: [website](https://robonurse-vla.github.io)<br>
* PathChat 哈佛医学院Faisal Mahmood教授团队的病理大模型。临床上, 病理被称为诊断的金标准: [website](https://www.nature.com/articles/s41586-024-07618-3)<br>
* DeepDR-LLM 糖尿病视网膜病变 (DR)的专科垂域多模态大模型: [website](https://www.nature.com/articles/s41591-024-03139-8)<br>
* VisionFM 通用眼科人工智能的多模式多任务视觉基础模型: [website](https://ai.nejm.org/doi/full/10.1056/AIoa2300221)<br>
* Medical-CXR-VQA 用于医学视觉问答任务的大规模胸部 X 光数据集: [website](https://github.com/Holipori/Medical-CXR-VQA)<br>

#### 3.10.1.2 Medical Robotics - 医疗机器人
* 医疗机器人的五级自动化(医疗机器人领域行业共识), 杨广中教授于2017年在Science Robotics上的论著: [Medical robotics—Regulatory, ethical, and legal considerations for increasing levels of autonomy](https://www.science.org/doi/pdf/10.1126/scirobotics.aam8638)<br>
* 医疗机器人的十年回顾(含医疗机器人的不同分类), 杨广中教授在Science Robotics上的综述文章：[A decade retrospective of medical robotics research from 2010 to 2020](https://www.science.org/doi/epdf/10.1126/scirobotics.abi8017)<br>
* 医疗具身智能的分级: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/pdf/2501.07468?)<br>
* Artificial intelligence meets medical robotics, 2023年发表在Science正刊上的论著: [website](https://www.science.org/doi/abs/10.1126/science.adj3312)<br>
* 机器人手术：从理论到实践的突破 (Nature Reviews Bioengineering): [Robotic surgery](https://www.nature.com/articles/s44222-025-00294-6)

* 医疗机器人的机器视觉
  * 3DGS在腔镜手术中的应用综述: [website](https://arxiv.org/pdf/2408.04426)<br>
  * 香港中文大学任洪亮教授团队在Nature Reviews Electrical Engineering上关于大型视觉模型 (LVM)在手术机器人上的综述 [website](https://www.nature.com/articles/s44287-025-00166-6)

* 达芬奇手术机器人是最为常用的外科手术机器人, 对于这类机器人自主技能操作的研究最为广泛
  * 达芬奇手术机器人研究套件dVRK介绍: [website](https://ieeexplore.ieee.org/abstract/document/9531355)<br>
  * 通过模仿学习在达芬奇机器人上学习外科手术操作任务 Surgical Robot Transformer (SRT): [website](https://surgical-robot-transformer.github.io/)<br>
  * Domain-specific Simulators - 手术机器人技能学习领域的模拟器
    * SurRoL: RL-Centered and dVRK Compatible Platform for Surgical Robot Learning [website](https://med-air.github.io/SurRoL/)<br>
    * Surgical Gym: A high-performance GPU-based platform for surgical robot learning (ICRA 2024, work in progress, based on NVIDIA Omniverse): [website](https://github.com/SamuelSchmidgall/SurgicalGym)<br>
    * ORBIT-Surgical: An Open-Simulation Framework for Learning Surgical Augmented Dexterity  (ICRA 2024, based on NVIDIA Omniverse): [website](https://orbit-surgical.github.io/)<br>
    * 缝合是手术机器人操作中的一个关键子任务，实现其自主化已有多项研究。关于自主缝合技能操作的综述可参考: [website](https://link.springer.com/article/10.1007/s00464-024-10788-w)<br>

* 连续体和软体手术机器人作为柔性医疗机器人的重要分支, 凭借其独特的结构设计和材料特性, 在微创介入诊疗领域展现出显著优势。它们能够灵活进入人体狭窄腔体, 实现精准操作, 同时最大限度地减小手术创口, 降低患者术后恢复时间及感染风险, 为现代微创手术提供了创新性的技术解决方案。
  * 连续体机器人在医疗领域的应用 (Nabil Simaan; Howie Choset等): [Continuum Robots for Medical Interventions](https://ieeexplore.ieee.org/abstract/document/9707607)<br>
  * 软体手术机器人在微创介入手术中的应用 (Ka-wai Kwok; Kaspar Althoefer等)： [Soft Robot-Assisted Minimally Invasive Surgery and Interventions: Advances and Outlook](https://ieeexplore.ieee.org/abstract/document/9765966/authors#authors)<br>
  * 血管介入手术机器人的具身智能（面向血管介入特定场景与任务的感知、决策、技能学习）：[Advancing Embodied Intelligence in Robotic-Assisted Endovascular Procedures: A Systematic Review of AI Solutions](https://arxiv.org/abs/2504.15327)
* 连续体和软体机器人因其超冗余自由度和高度非线性的结构特性, 采用传统的控制与传感方法构建正逆运动学方程时面临显著的计算复杂性和建模局限性。传统方法难以精确描述其多自由度耦合运动及环境交互中的动态响应。为此, 基于数据驱动的智能控制方法(如深度学习、强化学习及自适应控制算法)成为解决这一问题的前沿方向。这些方法能够通过大量数据训练, 高效学习系统的非线性映射关系, 显著提升运动控制的精度、自适应性和鲁棒性, 为复杂医疗场景下的机器人操作提供了更为可靠的技术支撑。
    * 什么是软体机器人？软体机器人的具身智能定义: [知乎, by Ke WU from MBUZAI](https://www.zhihu.com/question/61637360/answer/92834447300?utm_psn=1870238291607040000)<br>
    * IROS 2024大会Program Chair新加坡国立大学Cecilia Laschi教授的论著: [Learning-Based Control Strategies for Soft Robots: Theory, Achievements, and Future Challenges](https://ieeexplore.ieee.org/abstract/document/10136428)<br>
    * 软体机器人中具身智能物理建模简明指南(也是出自NUS Cecilia教授团队): [A concise guide to modelling the physics of embodied intelligence in soft robotics](https://inria.hal.science/hal-03921606/document)<br>
    * 数据驱动方法在软体机器人建模与控制中的应用: [Data-driven methods applied to soft robot modeling and control: A review](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10477253)<br>

* 微纳机器人技术是一类集成了微纳米制造、生物工程和智能控制等多学科前沿技术的微型机器人系统。凭借其微纳米级的独特尺寸、优异的生物相容性和精准的操控性能，这一前沿技术为现代医学诊疗范式带来了突破性创新。在精准诊断方面，微纳机器人能够深入人体微观环境，实现细胞乃至分子水平的实时监测；在靶向治疗领域，其可作为智能药物载体，实现病灶部位的精准定位与可控释放；在微创手术应用中，微纳机器人系统为复杂外科手术提供了前所未有的精确操作平台。这些创新性应用不仅显著提升了诊疗效率，更为攻克重大疾病提供了全新的技术途径，推动着现代医学向更精准、更微创、更智能的方向发展。
    * 微纳机器人的机器学习(CUHK 张立教授团队在Nature Machine Intelligence上的论著): [Machine learning for micro- and nanorobots](https://www.nature.com/articles/s42256-024-00859-x)<br>

<section id="uav"></section>

### 3.10.2 UAV - 无人机
无人机的发展来源于：
1. 从外部传感设备保护发展至机载传感与计算；
2. 从遥控/预先编程发展至自主。

不同于legged locomotion和manipulation，在无人机领域，data-driven的方法与model-based/modular的方法在不同任务中的优势不同，仍处于分庭抗礼的阶段。这主要是因为无人机的模型与驱动模式较为简单(如四旋翼的驱动机构只有四个电机)，且传统的无人机(即不具有操作设备)不会与环境产生交互，因此基于模型、优化和分层的方法，通过良好的状态机/规则设计和高效的局部优化技术，仍能够被赋予很强的性能。然而，无人机的难点在于其状态估计(通常需要)、感知和底层驱动充满噪声，这是因为小型化无人机的负载能力十分有限以及其成本被尽可能压低，因此在一些任务中data-driven/端到端的方法展现出了远超于传统方法的性能。因此，以下对无人机data-driven资料介绍的同时会穿插其与传统方法的对比，以便大家了解整个领域发展的动机。

总体而言，无人机的研究分为三个部分：
1. 技能实现/学习，例如避障、竞速、大机动飞行/特技等；
2. 任务实现/学习，例如探索、重建、跟踪等；
3. 飞行机器人本体设计。

无人机工作的开源代码并不多且良莠不齐，大部分需要通过论文学习。

### 3.10.2.1 技能实现/学习
- **支持RL的仿真器**
  
  无人机的仿真器普遍并不强大，并且几乎没有开源的RL sim2real项目。基于开源代码需要较大的内容改动才能实现理想的sim2real performance。
  - **AirSim** (https://microsoft.github.io/AirSim/)：基于UE4引擎，具有较为逼真动力学transition模拟。缺点是UE4底层功能较难修改并且运行速度较慢。
  - **Flightmare** (https://github.com/uzh-rpg/flightmare)：基于Unity渲染，CPU并行动力学。
  - **AerialGym** (https://github.com/ntnu-arl/aerial_gym_simulator)：基于IsaacSim，GPU并行动力学。

- **经典技能代表性工作**

  我们主要介绍一些data-driven方法在经典任务上的应用。值得一提的是，以下的工作中，出现了一些摆脱了对SLAM系统和里程计依赖的方法(而无人机最初的兴起正是依靠SLAM/里程计系统的日益成熟)，将成为无人机技能学习中有趣的进展方向。
  - **未知场景障碍物躲避**
    - Learning Monocular Reactive UAV Control in Cluttered Natural Environments. ICRA 2013, CMU. 受自动驾驶发展启发，第一个使用监督学习将图像映射为离散上游控制指令的系统。
    - CAD2RL: Real Single-Image Flight without a Single Real Image. RSS 2017，UCB. 第一个使用sim2real RL，对单目RGB图像进行大量domain randomization，在长廊中输出速度指令的系统。
    - DroNet: Learning to Fly by Driving. RAL 2018, UZH. 利用自动假设数据集让飞机输出速度指令，代码开源( https://github.com/uzh-rpg/rpg_public_dronet )。
    - Learning High-Speed Flight in the Wild. SciRob 2021, UZH. 使用dagger利用传统轨迹规划进行监督学习。文章claim网络推理的低延迟可以使未知环境中飞行速度更快。代码开源( https://github.com/uzh-rpg/agile_autonomy )。
    - Back to Newton's Laws: Learning Vision-based Agile Flight via Differentiable Physics, Arxiv 2024, SJTU. 用differentiable physics提供的一阶梯度做策略优化，不需要显式的位置和速度估计。文章用低分辨率深度图，训练避障比RL更高效，实现高速飞行。
    - [Flying on Point Clouds using Reinforcement Learning](https://arxiv.org/abs/2503.00496) [[Video](https://www.bilibili.com/video/BV1xeRpYnEYT)].Arxiv 2025, ZJU. 使用机载雷达和sim2real RL实现自主避障。
    - 值得一提的是，作为无人机最常用的任务，避障现在最常用的还是传统方法的系统如开源的ego-planner( https://github.com/ZJU-FAST-Lab/ego-planner )，由于这样的方案已经足以胜任大部分场景(而不像四足的MPC)，因此在实际应用中比较少使用data-driven的方案。

  - **无人机竞速**
    - Champion-level drone racing using deep reinforcement learning. Nature 23, UZH. 用强化学习战胜人类冠军飞手, 近几年无人机领域影响力最高的文章，是UZH RPG实验室多年来深厚工程积累的结果，其中的RL方案较为简单直接。
    - Reaching the Limit in Autonomous Racing: Optimal Control versus Reinforcement Learning. SciRob 23, UZH. 强化学习与最优控制方法竞速飞行对比。
    - Demonstrating Agile Flight from Pixels without State Estimation. RSS 2024, UZH. 使用视觉，不需要显式状态估计的现实世界竞速demo。
    - UZH的Perception and Robotics Group (RPG) 使用最优控制和RL的方法在竞速上有诸多尝试，使得无人机在固定轨道上达到最快飞行速度。

  - **大机动/特技飞行**
    - Deep Drone Acrobatics. RSS 2020, UZH. 使用模仿学习，从视觉特征点中学习MPC的轨迹跟踪，实现姿态剧烈变化的特技飞行。
    - [Whole-Body Control Through Narrow Gaps From Pixels to Action](https://arxiv.org/abs/2409.00895). ICRA 2025, ZJU. 使用强化学习实现视觉端到端窄缝穿越，不需要显式的位置和速度估计，超越传统方法性能。

- **经典任务实现代表性工作**
  - **追捕**
    - HOLA-Drone: Hypergraphic Open-ended Learning for Zero-Shot Multi-Drone Cooperative Pursuit. Arxiv 2024, University of Manchester.
    - Multi-UAV Pursuit-Evasion with Online Planning in Unknown Environments by Deep Reinforcement Learning. Arxiv 2024, THU.
  - **探索**
    - Deep Reinforcement Learning-based Large-scale Robot Exploration, RAL 2024, National University of Singapore (NUS). 利用注意力机制学习不同空间尺度的依赖关系，对未知区域进行隐式预测，优化已知空间探索策略，提高探索效率。
    - ARiADNE: A Reinforcement learning approach using Attention-based Deep Networks for Exploration, ICRA 2023, National University of Singapore (NUS). 学习已知不同区域在多个空间尺度上的相互依赖关系，并隐式预测探索这些区域可能获得的潜在收益。这使得代理能够安排行动顺序，以平衡在已知区域对地图进行开发/细化与探索新区域之间的自然权衡。
    - DARE: Diffusion Policy for Autonomous Robot Exploration. ICRA 2025, National University of Singapore (NUS). DARE方法利用self-attention学习地图空间信息，并通过diffusion生成通往未知区域的轨迹，以提高自主机器人的探索效率。

### 3.10.2.2 无人机硬件平台搭建
手搓一个遥控器操控的穿越机不是一个很难的事情，网上有很多爱好者分享教程。但想搭建一个具有自主导航功能的无人机并非易事，是一个系统工程，这里推荐浙大FAST-lab开源的教程：

- [从0制作自主空中机器人](https://www.bilibili.com/video/BV1WZ4y167me)

### 3.10.2.3 新构型无人机设计
除了常规用于航拍，环境探索的四旋翼无人机，想让无人机具备更多能力，应用于更广泛的具身智能场景，除了算法上的创新外，也需要在硬件层面对无人机的构型进行创新设计。

- **空中机械臂(Aerial Manipulator)** 

    空中机械臂，也叫空中操作无人机，兼具无人机的快速空间移动能力和机械臂的精确操纵能力，是具身智能的一种理想载体。西湖大学赵世钰老师组在知乎上有一系列文章介绍：

    - [空中作业机器人，下一代无人机技术？](https://zhuanlan.zhihu.com/p/442331197)
    - [空中作业机器人—没那么简单！](https://zhuanlan.zhihu.com/p/487203757)
    - [空中操作机器人：如何设计机械臂？](https://zhuanlan.zhihu.com/p/509669272)
    - [空中作业机器人都有哪些应用？](https://zhuanlan.zhihu.com/p/517471760)

    * 代表性工作
        * [Past, Present, and Future of Aerial Robotic Manipulators](https://ieeexplore.ieee.org/document/9462539). TRO 2022. 空中机械臂领域目前最全的综述文章，入门了解必备。
        * [Millimeter-Level Pick and Peg-in-Hole Task Achieved by Aerial Manipulator](https://ieeexplore.ieee.org/abstract/document/10339889). TRO 2023, BHU. 使用四旋翼加串联机械臂实现毫米精度peg-in-pole任务。
        * [NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122) [[Video](https://www.bilibili.com/video/BV16Zt5eBEPW)]. ICRA 2025, SYU. 使用四旋翼加并联机械臂实现毫米精度抓取。
        * [A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7) [[Video](https://www.bilibili.com/video/BV1CC4y1Z7xS)]. JIRS 2024, BHU. 用空中机械臂做一些有趣的应用，比如抓鸡蛋、开门等等。

- **全驱动无人机(Fully-Actuated UAV)**

    常见的四旋翼无人机具有欠驱动特性，即位置与姿态耦合。而具有位置姿态解耦控制的全驱动无人机，理论上更适合作为空中操作的飞行平台。

    * 代表性工作
        * [Fully Actuated Multirotor UAVs: A Literature Review](https://ieeexplore.ieee.org/document/8978486/?arnumber=8978486). RAM 2020. 全驱动无人机领域目前最全的综述文章，入门了解必备。
        * [Design, modeling and control of an omni-directional aerial vehicle](https://ieeexplore.ieee.org/document/7487497). ICRA 2016, ETH. 第一个实现全向飞行的固定倾角全驱动无人机。
        * [The Voliro omniorientational hexacopter: An agile and maneuverable tiltable-rotor aerial vehicle](https://ieeexplore.ieee.org/document/8485627). RAM 2018, ETH. 第一个实现全向飞行的可变倾角全驱动无人机 
        * [FLOAT Drone: A Fully-actuated Coaxial Aerial Robot for Close-Proximity Operations](https://arxiv.org/abs/2503.00785) [[Website](https://zju-jxlin.github.io/float-drone.github.io/)]. Arxiv 2025, ZJU. 适合近端作业的小尺寸全驱动无人机。

- **可变形无人机(Deformable UAV)**

    除了通过往飞行平台上安装机械臂，让无人机本体可以变形，也是使其实现更多功能的一种方法。

    * 代表性工作
        * [Design, Modeling, and Control of an Aerial Robot DRAGON: A Dual-Rotor-Embedded Multilink Robot With the Ability of Multi-Degree-of-Freedom Aerial Transformation](https://ieeexplore.ieee.org/document/8258850). RAL 2018，东京大学. Best paper award on UAV in ICRA 2018，多关节可变形无人机。
        * [The Foldable Drone: A Morphing Quadrotor That Can Squeeze and Fly](https://ieeexplore.ieee.org/document/8567932?arnumber=8567932). RAL 2019, Uzh. 四旋翼每个机臂上安装一个舵机，实现机体变形飞行。
        * [Ring-Rotor: A Novel Retractable Ring-Shaped Quadrotor With Aerial Grasping and Transportation Capability](https://ieeexplore.ieee.org/document/10044964) [[Video](https://www.bilibili.com/video/BV1gY4y1K723)]. RAL 2023, ZJU. 一种可变形的环形四旋翼，可用于抓取、运输等任务。
        * [Design and Control of a Passively Morphing Quadcopter](https://ieeexplore.ieee.org/document/8794373) [[Video](https://www.youtube.com/watch?v=MSvoQT__c9U)]. ICRA 2019, UCB. 一种被动变形的四旋翼无人机。

- **多模态无人机(Multi-Modal UAV)**

    无人机与地面机器人相比，其优势在于三维空间运动能力，劣势则是续航差。因此一些研究关注多模态无人机的构型设计、运动控制以及自主导航。多模态无人机具备空中、地面、水下等多域运动能力。这不仅能解决无人机的续航问题，也能让无人机具有更多应用潜力。

    * 代表性工作
        * [A bipedal walking robot that can fly, slackline, and skateboard](https://www.science.org/doi/10.1126/scirobotics.abf8136). SR 2021, Caltech. 多模态空地足式机器人。
        * [Multi-Modal Mobility Morphobot (M4) with appendage repurposing for locomotion plasticity enhancement](https://www.nature.com/articles/s41467-023-39018-y). NC 2023, Northeastern University. 具有很多种运动模式的多模态无人机。
        * [Skater: A Novel Bi-Modal Bi-Copter Robot for Adaptive Locomotion in Air and Diverse Terrain](https://ieeexplore.ieee.org/document/10538378) [[Video](https://www.bilibili.com/video/BV1y2421M7HM)]. RAL 2024, ZJU. 适应多样地形的多模态空地双旋翼无人机。
        * [Autonomous and Adaptive Navigation for Terrestrial-Aerial Bimodal Vehicles](https://ieeexplore.ieee.org/document/9691888). RAL 2022, ZJU. 实现空地多模态无人机的自主导航。


<section id="ad"></section>

### 3.10.3 Autonomous Driving - 自动驾驶

[自动驾驶之心](https://www.zdjszx.com/) (也有个微信公众号)

自动驾驶被称为“最小的具身智能验证场景”，这是因为它在具身智能的框架中，具备完整的感知、决策和行动闭环，但任务目标明确、物理交互简单、场景复杂性相对较低。作为一个技术验证场景，自动驾驶既能体现具身智能的核心特性，又为更复杂的具身智能任务提供了技术积累和理论支持。

#### Model：自动驾驶仿真

[生成式仿真为具身智能释放无限灵感](https://bydrug.pharmcube.com/news/detail/80b67b2227879864af934e5f81835776)

自动驾驶仿真是自动驾驶技术开发中不可或缺的一部分。它通过提供安全、高效、可控的测试环境，不仅降低了研发成本和风险，还加速了技术的迭代和规模化部署。同时，仿真能够覆盖大量现实中难以复现的场景，为自动驾驶系统的安全性、可靠性和泛化能力提供了重要保障。

1. 3D/4D 场景重建

* 经典工作：NSG, MARS, StreetGaussians, OmniRe
  * **NSG**: CVPR 2021, [github](https://github.com/princeton-computational-imaging/neural-scene-graphs), [arxiv](https://arxiv.org/abs/2011.10379), [paper](https://openaccess.thecvf.com/content/CVPR2021/html/Ost_Neural_Scene_Graphs_for_Dynamic_Scenes_CVPR_2021_paper.html)
  * **MARS**: [github](https://open-air-sun.github.io/mars/), [arxiv](https://arxiv.org/abs/2307.15058)
  * **StreetGaussians**: [github](https://github.com/zju3dv/street_gaussians), [arxiv](https://arxiv.org/abs/2401.01339)
  * **OmniRe**: ICLR 2025 Spotlight, [demo page](https://ziyc.github.io/omnire), [github](https://github.com/ziyc/drivestudio), [arxiv](https://arxiv.org/abs/2408.16760)

2. 场景可控生成(世界模型)

* 经典工作：GAIA-1, GenAD（OpenDV数据集）, Vista, SCP-Diff, MagicDrive -> MagicDriveDiT, UniScene, VaVAM
  * **GAIA-1**: [demo page](https://wayve.ai/thinking/introducing-gaia1/), [arxiv](https://arxiv.org/abs/2309.17080)
  * **GenAD**: CVPR 2024 Highlight, OpenDV数据集, [github](https://github.com/OpenDriveLab/DriveAGI?tab=readme-ov-file#opendv), [arxiv](https://arxiv.org/abs/2403.09630)
  * **Vista**: NeurIPS 2025, [demo page](https://opendrivelab.com/Vista), [github](https://github.com/OpenDriveLab/Vista), [arxiv](https://arxiv.org/abs/2405.17398)
  * **SCP-Diff**: [demo page](https://air-discover.github.io/SCP-Diff/), [github](https://github.com/AIR-DISCOVER/SCP-Diff-Toolkit), [arxiv](https://arxiv.org/abs/2403.09638)
  * **MagicDrive** -> MagicDriveDiT: [demo page](https://gaoruiyuan.com/magicdrive-v2/), [arxiv](https://arxiv.org/abs/2411.13807)
  * **UniScene**: CVPR 2025, [demo page](https://arlo0o.github.io/uniscene/),  [arxiv](https://arxiv.org/abs/2412.05435)
  * **VaVAM**: [github](https://github.com/valeoai/VideoActionModel)


#### Policy：自动驾驶策略

1. 从模块化到端到端

* 经典的模块化管线中，每个模型作为一个独立的组件，负责对应的特定任务(3D目标检测与跟踪 & BEV 建图 -> 目标运动预测 -> 轨迹规划)，这种设计已逐渐被端到端模型所取代。

[End-to-end Autonomous Driving: Challenges and Frontiers](https://arxiv.org/pdf/2306.16927)

2. 快系统与慢系统并行

[理想端到端-VLM双系统](https://www.sohu.com/a/801987742_258768)

* 快系统经典论文：UniAD (CVPR 2023 Best Paper), VAD, SparseDrive, DiffusionDrive
  * **UniAD**: CVPR 2023 Best Paper, [github](https://github.com/OpenDriveLab/UniAD), [arxiv](https://arxiv.org/abs/2212.10156)
  * **VAD**: ICCV 2023, [github](https://github.com/hustvl/VAD), [arxiv](https://arxiv.org/abs/2303.12077)
  * **SparseDrive**: [github](https://github.com/swc-17/SparseDrive), [arxiv](https://arxiv.org/abs/2405.19620)
  * **DiffusionDrive**: CVPR 2025, [github](https://github.com/hustvl/DiffusionDrive), [arxiv](https://arxiv.org/abs/2411.15139)
  * 快系统的 Scale up 特性探究：https://arxiv.org/pdf/2412.02689
* 慢系统经典论文：DriveVLM, EMMA
  * **DriveVLM**: CoRL 2024, [arxiv](https://arxiv.org/abs/2402.12289)
  * **EMMA**: [arxiv](https://arxiv.org/abs/2410.23262)
  	- **[Open-EMMA](https://github.com/taco-group/OpenEMMA)** 是EMMA的一个开源实现，提供了一个用于自动驾驶车辆运动规划的端到端框架。


#### 未来发展方向

[AIR ApolloFM技术全解读](https://air.tsinghua.edu.cn/info/1007/2258.htm)

<section id="control"></section>

## 4. Control and Robotics - 控制论与机器人学基础
**经典课程**
  - [video](https://www.bilibili.com/video/BV1GJ411k7fE) 美国西北大学 现代机器人 Modern Robotics： 这门课侧重于基础的机器人理论，涉及的概念有**笛卡尔坐标系**，**关节坐标系**，**自由度**，**齐次旋转矩阵**，**正运动学（FK）**， **逆运动学（IK）**等等，适合零基础入门。
  - [video](https://www.bilibili.com/video/BV1h7411A7B9) 加州伯克利 高级机器人技术 by Pieter Abbeel： 这门课是机器人的进阶课程，适合在学习完‘现代机器人 Modern Robotics’或者有相应基础后进一步学习。涉及的部分有**马尔科夫决策过程**，**LQR控制**，**在约束条件下的最优化问题**，**基于最优化的控制**，**运动规划**，**卡尔曼滤波**，**模仿学习**，**强化学习**，**Sim2Real**等等。课程中还涉及了很多实操演示，有助于进一步了解理论在真实世界中的应用。
## 4.1. 控制理论基础

### 4.1.1 经典控制原理
* 理解系统、反馈
* 时域与频域分析
* 传递函数
* 理解前馈控制、反馈控制
* **PID控制**：[CSDN](https://blog.csdn.net/name_longming/article/details/115093338) [BiliBili](https://www.bilibili.com/video/BV1B54y1V7hp)

### 4.1.2 现代控制理论(线性系统控制)
* Modern Control Systems (14th edition), Robert. H. Bishop, Richard. C, Dorf. z: [Book](http://103.203.175.90:81/fdScript/RootOfEBooks/E%20Book%20collection%20-%202024/EEE/Modern_control_systems_Robert_H_Bishop_Richard_C_Dorf_z_lib_org.pdf#page=1.00&gsr=0)
* 状态方程
* 状态反馈与最优控制
* **LQR控制** [BiliBili](https://www.bilibili.com/video/BV1Ng4y1V7JQ)

### 4.1.3 先进控制技术
* 鲁棒控制
* 彻底搞懂阻抗控制、导纳控制、力位混合控制: [CSDN](https://blog.csdn.net/a735148617/article/details/108564836)
* **模型预测控制 MPC**
* 智能控制 (包含基于深度学习的控制)

## 4.2. 机器人学导论

### 4.2.1 推荐材料
* 现代机器人学(非常推荐！)[video](https://www.youtube.com/watch?v=29LhXWjn7Pc&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx&index=11)
* 经典教材
  * 《机构学与机器人学的几何基础与旋量代数》 戴建生院士 著
  * 《现代机器人学：机构、规划与控制》凯文·M. 林奇, 朴钟宇 著
  * 《机器人学的现代数学理论基础》丁希仑 著

### 4.2.2 机器人运动学 (Kinematics) 与动力学 (Dynamics)
1. 机器人运动学
> 想要快速了解什么是IK FK的同学可以看这个7分钟的短片, 可以对此建立一个粗略的认知：[BiliBili](https://www.bilibili.com/video/BV18E411v7F9)<br>
> 较为简单的过一遍IK和FK的原理可以看这个：[CSDN](https://blog.csdn.net/Dwzsa/article/details/142386529?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&utm_relevant_index=6) 

* IK (Inverse Kinematics) 逆运动学
  * 较为详细的视频课
    * [BiliBili IK(1)](https://www.bilibili.com/video/BV1PD4y1t7xP)
    * [BiliBili IK(2)](https://www.bilibili.com/video/BV1Tt4y1T79Z)
  * 文字教学
    * [Book](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html), 较为详细的IK理论

* FK (Forward Kinematics) 正运动学
  * 较为详细的视频课
    * [BiliBili FK(1)](https://www.bilibili.com/video/BV1Ve4y127Uf)
    * [BiliBili FK(2)](https://www.bilibili.com/video/BV1a14y157uL)

2. 机器人动力学(**重要！！！**)
* 理解斜对称矩阵, Twist和Exponential of a twist, 旋量代数

### 4.2.3 里程计和同步定位与建图 (Odometry&SLAM)
里程计(Odometry)用于为机器人实时提供定位，里程计常常基于扩展卡尔曼滤波(EKF)实现，融合来自惯性测量单元(IMU)、相机、激光雷达、码盘、毫米波雷达、超宽带(UWB)、光流传感器等等各种常用于机器人位姿感知的传感器之中的多种观测，以较高的频率实现对机器人位姿的估计。

里程计中最常见的是视觉惯性里程计(VIO)和激光惯性里程计(LIO)，以及最近新兴的一些用4D毫米波雷达作为主要传感器的方法，其中比较经典的工作包括VINS系列[VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)，[ORB-SLAM](https://github.com/UZ-SLAMLab/ORB_SLAM3)，[VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)，[LOAM](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf)，[FAST-LIO](https://github.com/hku-mars/FAST_LIO)等等。此外还有融合了IMU、相机和激光传感器的里程计[FAST-LIVO](https://github.com/hku-mars/FAST-LIVO2)系列等。

SLAM(Simultaneous Locolization And Mapping)在定位的同时完成地图的构建，使得回环(Loop Closure)检测成为可能，回环检测的存在使得当机器人重新访问到某个位置时可以修正一部分的累计误差，提高在长时间作业时的定位精度。SLAM的实现主要有filter-based和optimization-based两种，实现中一般又分前端和后端，基于不同传感器的SLAM又各有其特点，在这里提供一些学习资源，主要是书籍：

* [SLAM Handboook](https://github.com/SLAM-Handbook-contributors/slam-handbook-public-release)
* [Past, Present, and Future of Simultaneous Localization And Mapping: Towards the Robust-Perception Age](https://arxiv.org/abs/1606.05830): SLAM领域的经典综述
* 高翔老师的[《视觉SLAM十四讲》](https://github.com/gaoxiang12/slambook2)
* 高翔老师的[《自动驾驶与机器人的SLAM技术》](https://github.com/gaoxiang12/slam_in_autonomous_driving)

此外，SLAM也有端到端的实现[DROID-SLAM](https://arxiv.org/abs/2108.10869)。

其他关于slam的思考可以参考[awesome-and-novel-works-in-slam](https://github.com/runjtu/awesome-and-novel-works-in-slam)

### 4.2.4 杂项 Misc

* ROS基础:
  * 具身智能ROS1基础: [website](http://www.autolabor.com.cn/book/ROSTutorials/)
  * 具身智能ROS2基础: [website](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)  
* 常用的库 
  * cuRobo：[cuRobo](https://curobo.org/), cuRobo是Nvidia的一个利用 CUDA 加速的机器人库, 提供了一套高效的机器人算法, 主要通过并行计算显著提升性能, 包括但不限于IK, 碰撞检测, 路径规划等。
  * IKFast：[IKFast](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html), 经典IK库。
  * mplib：[mplib](https://github.com/haosulab/mplib), Maniskill Benchmark以及Sapien仿真平台的IK库。
* ROS多传感器时间戳同步：[website](https://blog.csdn.net/qq_43495930/article/details/125649446)
* 动手实践LeRobot SO-100：[website](https://huggingface.co/lerobot)


<section id="hardware"></section>

# 5. Hardware - 硬件

> 具身智能硬件方面涵盖多个技术栈, 如嵌入式软硬件设计, 机械设计, 机器人系统设计, 这部分知识比较繁杂, 适合想要专注此方向的人
> 关于硬件部分的学习, 最好从实践出发！

<section id="embedded"></section>

## 5.1 Embedded - 嵌入式
* 嵌入式学习路线: [CSDN](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452)
* 51单片机：[BiliBili](https://www.bilibili.com/video/BV1Mb411e7re), 经典江科大自动协出品
* Stm32单片机：[BiliBili](https://www.bilibili.com/video/BV1th411z7sn), 经典江科大自动协出品
* Stm32电机驱动：[BiliBili](https://www.bilibili.com/video/BV1AZ4y1V7wt), 野火
* 野火Stm32标准库：[BiliBili](https://www.bilibili.com/video/BV1yW411Y7Gw), 野火
* 正点原子Stm32：[BiliBili](https://www.bilibili.com/video/BV1Lx411Z7Qa), 正点原子
* 韦东山嵌入式Linux：[BiliBili](https://www.bilibili.com/video/BV1w4411B7a4), 韦东山

<section id="mechanical"></section>

## 5.2 Mechanical Design - 机械设计

* SolidWorks教学：[BiliBili](https://www.bilibili.com/video/BV1iw411Z7HZ)
* URDF生成：[CSDN](https://blog.csdn.net/weixin_45168199/article/details/105755388), 指导如何通过SolidWorks装配体出发生成机器人URDF文件。
  
<section id="robosystem"></section>

## 5.3 Robot System Design - 机器人系统设计

* 《机器人学简介》, 来自[2]做的高质量教材: [PDF](./files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf)
* 《机器人系统教材》: [website](https://motion.cs.illinois.edu/RoboticSystems/)


<section id="sensors"></section>

## 5.4 Sensors - 传感器
### 5.4.1深度相机

RealSense，[RealSense Ros 开发套件](https://github.com/IntelRealSense/realsense-ros/tree/ros1-legacy)

<section id="tactile"></section>

## 5.5 Tactile Sensing - 触觉感知

### 1. 视触觉传感器(Vision-Based Tactile Sensors)


视触觉传感器通过摄像头捕捉触觉信息，将触摸表面变形映射为视觉数据，以估计接触力、形变等信息。其设计涉及 **传感器形状**(影响接触范围与适应性)、**标记点设置**(追踪表面形变，提高分辨率)、**材料选择**(如硅胶或弹性体，提高灵敏度)以及 **光照与摄像系统**(增强视觉信号质量)。

* **优点**：提供高分辨率触觉信息、非侵入式感知、不影响物体表面特性，并且可与视觉系统集成，提高多模态感知能力。  
* **缺点**：计算量大，依赖视觉处理和机器学习；易受环境光影响；光学设计复杂，封装和耐用性受限。

 **参考文献综述**：写的非常详细，分别是算法和结构设计
- 算法：*[When Vision Meets Touch: A Contemporary Review for Visuotactile Sensors From the Signal Processing Perspective
](https://ieeexplore.ieee.org/document/10563188)*
- 结构：*[On the Design and Development of Vision-Based Tactile Sensors](https://link.springer.com/article/10.1007/s10846-021-01431-0)*

### 2. 电子皮肤(Electronic Skin)

触觉感知的路径主要就是这两类。电子皮肤模拟人类皮肤的触觉能力，通常采用柔性电子材料(如压力传感薄膜、纳米传感器网络等)来感知外界压力、温度和形变，使机器人具备更接近生物的触觉感知能力。

* **优点**：电子皮肤可 **大面积覆盖** 机器人表面，实现全身触觉感知；具有 **高灵敏度**，能够检测微小的力变化，实现精准反馈；同时 **可伸缩性** 使其适应复杂表面，提高耐久性。
* **缺点**：电子皮肤的 **制造复杂**，材料和工艺要求高，成本较高；**数据处理挑战**，大规模触觉数据需要高效的计算与存储方案；此外，**稳定性问题** 可能导致长期使用后灵敏度下降，影响可靠性。


 **参考文献综述**：*[Toward an AI Era: Advances in Electronic Skins](https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00049)*

### 3. 触觉感知的应用和算法(视触觉)

* 3.1 姿态估计(Pose Estimation)
  * 估计in hand物体姿态
    * *[3D Shape Perception from Monocular Vision, Touch, and Shape Priors](https://arxiv.org/abs/1808.03247)*
  * in scene
    * *[Fast Model-Based Contact Patch and Pose Estimation for Highly Deformable Dense-Geometry Tactile Sensors](https://ieeexplore.ieee.org/document/8936859)*

* 3.2 物体分类(Classification)
  * 区分不同液体、材料或透明物体。
    * *[Understanding Dynamic Tactile Sensing for Liquid Property Estimation](https://arxiv.org/abs/2205.08771)*
    * *[Multimode Fusion Perception for Transparent Glass Recognition](https://www.semanticscholar.org/paper/Multimode-fusion-perception-for-transparent-glass-Zhang-Shan/90109f2eabba717d152a599fc8d8d5a3677c85e5)*

* 3.3 触觉操控(Manipulation)
  * 物体装配
    * *[Active Extrinsic Contact Sensing: Application to General Peg-in-Hole Insertion](https://ieeexplore.ieee.org/abstract/document/9812017)*
    * *[Building a Library of Tactile Skills Based on Fingervision](https://ieeexplore.ieee.org/abstract/document/9035000)*
  * 线缆整理
    * *[Cable Manipulation with a Tactile-Reactive Gripper](https://arxiv.org/abs/1910.02860)*
  * 精细手部操作
    * *[Manipulation by Feel: Touch-Based Control with Deep Predictive Models](https://arxiv.org/abs/1903.04128)*
    * *[NeuralFeels with Neural Fields: Visuotactile Perception for In-Hand Manipulation](https://www.science.org/doi/10.1126/scirobotics.adl0628)*

* 3.4 触觉大模型(Large Tactile Models)
  * 以统一多模态触觉表示，提高通用性。
    * *[Binding Touch to Everything: Learning Unified Multimodal Tactile Representations](https://openaccess.thecvf.com/content/CVPR2024/papers/Yang_Binding_Touch_to_Everything_Learning_Unified_Multimodal_Tactile_Representations_CVPR_2024_paper.pdf)*

### 4. 传感器购买

市面上有一些成熟的视触觉传感器可供选择 🔗 **[GelSight 官网](https://gelsight.com/)**

<section id="companies"></section>

## 5.6 Companies - 公司

| 公司 | 主营产品 | Others |
|-------|------|------|
| [松灵AgileX](https://www.agilex.ai/) | [pipper 六轴机械臂](https://www.agilex.ai/chassis/16)<br> [PIKA 数采方案](https://www.agilex.ai/chassis/22)<br>[Cobot Magic 双臂遥操作平台](https://www.agilex.ai/chassis/27)<br>移动底盘| 面向教育科研
| [宇树Unitree](https://www.unitree.com/cn) | [四足机器人开发指南](https://www.yuque.com/ironfatty/nly1un/luo9gb)<br>[Go2机器狗](https://www.unitree.com/cn/go2)<br>[AlienGo机器狗](https://www.yuque.com/ironfatty/nly1un/dqcz3u)<br>[通用人形H1](https://www.unitree.com/cn/h1)<br>[通用人形G1](https://www.unitree.com/cn/g1)<br> | 许多产出使用宇树的机器人作为硬件基础
| [方舟无限ARX](https://www.arx-x.com/?product/) | [X5机械臂](https://www.arx-x.com/?product/21.html)<br>[X7双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5机械臂](https://www.arx-x.com/?product/22.html)  | 适合复现很多经典的工作, eg. [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin松灵底盘+方舟臂](https://github.com/TianxingChen/RoboTwi)
| [波士顿动力](https://bostondynamics.com/)  | [spot机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas通用人形](https://bostondynamics.com/atlas/)  | 具身智能本体制造商, 从液压驱动转向电机驱动 |
| [灵心巧手](https://www.linkerbot.cn/index) | [Linker Hand L30（健绳驱动）](https://www.linkerbot.cn/product?page=L30)<br>[Linker Hand L20（连杆驱动）](https://www.linkerbot.cn/product?page=L20) | 主攻各类灵巧手 |
| [灵巧智能DexRobot](https://www.dex-robot.com/)| [Dexhand 021灵巧手](https://www.dex-robot.com/productionDexhand) | 19自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) | [GALBOT G1](https://www.galbot.com/g1) | 专注于具身智能多模态大模型通用机器人研发 |
| [星海图Galaxea](https://galaxea.ai/) | [A1六轴机械臂](https://galaxea.ai/A1)<br>[R1-Pro 仿人形机器人](https://galaxea.ai/R1-Pro) | 软硬件产品均自主研发，专注于打造“一脑多型“ |
| [World Labs](https://www.worldlabs.ai/) | | 专注于空间智能, 致力于打造大型世界模型(LWM), 以感知、生成并与 3D 世界进行交互。 [相关介绍](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1人形](https://www.robotera.com/goods/1.html)<br> [XHAND1灵巧手](https://www.robotera.com/goods/2.html) | |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1人形](https://boosterobotics.com/zh/store/)|  |
| [青龙机器人](https://www.openloong.net/) |  |  |
| [云深处科技](https://www.deeprobotics.cn/) |  [绝影X30四足机器人](https://www.deeprobotics.cn/robot/index/product3.html)<br> [Dr.01人形机器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | 具身智能仿真平台供应商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能数据平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [远征A2人形机器人](https://www.zhiyuan-robot.com/products/A2)<br>[远征A2-W 轮式人形](https://www.zhiyuan-robot.com/products/A2_W)<br>[灵犀X1 人形机器人](https://www.zhiyuan-robot.com/products/X1)<br>[精灵G1 轮式人形](https://www.zhiyuan-robot.com/products/A2_D)|  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://airbots.online/)  | [TOK2 移动主从臂平台](https://airbots.online/zh/tok)<br>[MMK2 移动升降双臂平台](https://airbots.online/zh/mmk2)<br> Play 六轴机械臂|  |
| [穹彻智能](https://www.noematrix.ai/) | | |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) | | |
| [具身风暴](https://www.robotstorm.tech) | | 落地具身智能通用按摩机器人 |
| [众擎机器人](https://engineai.com.cn/) |[SE 01](https://engineai.com.cn/product_one)<br>[PM 01](https://engineai.com.cn/product_fore)| |
| [魔法原子](https://www.magiclab.top/) |[MagicBot](https://www.magiclab.top/human)<br>[MagicDog](https://www.magiclab.top/dog)| |
| [帕西尼](https://www.paxini.com/) |[PX-6AX GEN2 触觉传感器](https://www.paxini.com/ax/gen2)<br>[DexH13 GEN2 灵巧手](https://www.paxini.com/dex/gen2)<br>[TORA-ONE 人形机器人](https://www.paxini.com/robot) | |
<section id="software"></section>

# 6. Software - 软件

<section id="simulators"></section>

## 6.1 Simulators 仿真器
常见仿真器wiki: [wiki](https://simulately.wiki/)
| 仿真器 | 对应基准集 |
|-------|------|
| [IsaacGym](https://developer.nvidia.com/isaac-gym) | [legged gym](https://github.com/leggedrobotics/legged_gym)<br>[parkour(包括蒸馏以及真机部署)](https://github.com/ZiwenZhuang/parkour)<br>[extreme-parkour](https://github.com/chengxuxin/extreme-parkour) |
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K(可跨平台)](https://behavior.stanford.edu/behavior-1k)+[omniGibson(工具链)](https://behavior.stanford.edu/omnigibson/)<br>[ARNOLD](https://arnold-benchmark.github.io/) <br> [GarmentLab](https://garmentlab.github.io/) and [DexGarmentLab](https://wayrise.github.io/DexGarmentLab/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html)+[robomimic(工具链)](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics(Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](https://github.com/robocasa/robocasa?tab=readme-ov-file)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| [Genesis](https://genesis-embodied-ai.github.io/) ||
| [SOFA](https://github.com/sofa-framework/sofa/)| 常用于软体机器人的仿真 |

**教程**：
- **Isaac 101：** [Blog](https://axi404.top/tags/isaac%20101) by Axi404.

<section id="benchmarks"></section>

## 6.2 Benchmarks 基准集
具身智能常用benchmark总结 [1]: [zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
* **CALVIN**, [github](https://github.com/mees/calvin), [website](http://calvin.cs.uni-freiburg.de/)2022年, 第一个公开的结合了自然语言控制、高维多模态输入、7自由度的机械臂控制以及长视野的机器人操纵benchmark。支持不同的语言指令, 不同的摄像头输入, 不同的控制方式, 主要用来评估具身智能模型的多模态输入的能力和长程规划能力。
* **Meta-World**, [webpage](https://meta-world.github.io/): 评估机器人在多任务和元强化学习场景下的表现。50个机器人操作任务(如抓取、推动物体、开门等), 组织成不同的基准测试集(如ML1、ML10、ML45、MT10、MT50等), 每个集合都有明确的训练任务和测试任务。周边和文档比较全面, 基于mojoco, 有完整的API和工具, python import即可运行。
* **Embodied Agent Interface: Benchmarking LLMs for Embodied Decision Making**, [website](https://embodied-agent-interface.github.io/): 主要评估大型语言模型(LLMs)在具身决策中的表现, 重点在于决策过程, 包括目标解释、子目标分解、动作序列化和状态转换建模, 不涉及到具体的执行。
* **RoboGen**, [repo](https://github.com/Genesis-Embodied-AI/RoboGen), [website](https://robogen-ai.github.io/): 不是生成policy, 而是生成任务、场景和带标记的数据, 能直接用来监督学习。
* **LIBERO**, [repo](https://github.com/Lifelong-Robot-Learning/LIBERO), [website](https://libero-project.github.io/intro.html): 用一个程序化生成管道来生成任务, 这个管道理论上可以生成无限数量的操作任务, 还提供了：三种视觉运动策略网络架构(RNN、Transformer和ViLT) 和 三种终身学习算法, 以及顺序微调和多任务学习的基准。
* **RoboTwin**, [repo](https://github.com/TianxingChen/RoboTwin): 使用程序生成双臂机器人无限操作任务数据, 并提供了所有任务的评测基准。

<section id="datasets"></section>

## 6.3 Datasets 数据集
* **Open X-Embodiment: Robotic Learning Datasets and RT-X Models**, [website](https://robotics-transformer-x.github.io/):  22种不同机器人平台的超过100万条真实机器人轨迹数据，覆盖了527种不同的技能和160,266项任务，主要集中在抓取和放置。
* **AgiBot World Datasets (智元机器人)**, [website](https://agibot-world.com/): 八十余种日常生活中的多样化技能，超过100万条轨迹数据，采集自**同构型机器人**, 多级质量把控和全程人工在环的策略，从采集员的专业培训，到采集过程中的严格管理，再到数据的筛选、审核和标注，每一个环节都经过了精心设计和严格把控。
* **RoboMIND**, [website](https://x-humanoid-robomind.github.io/): 包含了在479种不同任务中涉及96类独特物体的10.7万条真实世界演示轨迹，来自四种不同协作臂，任务被分为基础技能、精准操作、场景理解、柜体操作和协作任务五大类。
* **All Robots in One,** [website](https://imaei.github.io/project_pages/ario/): ARIO 数据集，包含了 **2D、3D、文本、触觉、声音 5 种模态的感知数据**，涵盖**操作**和**导航**两大类任务，既有**仿真数据**，也有**真实场景数据**，并且包含多种机器人硬件，有很高的丰富度。在数据规模达到三百万的同时，还保证了数据的统一格式，是目前具身智能领域同时达到高质量、多样化和大规模的开源数据集。
* **MimicGen** [26 Oct 2023, CoRL 2023],[repo](https://github.com/NVlabs/mimicgen),[website](https://mimicgen.github.io/)：基于Robosuite与MuJoCo开发的高效数据生成框架，主要聚焦于单臂机器人桌面操作任务，支持多种主流机器人型号。MimicGen提出了一种自动化的数据扩增方法，能够从少量真实人类演示中自动生成大量模拟数据，例如仅使用200段真人演示即可生成超过5万条仿真演示数据，涵盖18类常见机器人任务。
* **RoboCasa** [4 Jun 2024],[repo](https://github.com/robocasa/robocasa), [website](https://robocasa.ai/):基于RoboSuite与MimicGen在MuJoCo中构建的高仿真厨房任务仿真平台。RoboCasa提供了120个多样化厨房环境，包含超过2500个3D物体模型。平台支持单臂、双臂、人形机器人以及移动底座搭载机械臂的机器人系统。此外，RoboCasa内置了25种基础原子任务和75种组合任务，能够真实模拟机器人在复杂厨房场景中的多样化操作行为。
* **DexMimicGen** [6 Mar 2025, ICRA 2025],[repo](https://github.com/NVlabs/dexmimicgen/), [website](https://dexmimicgen.github.io/):以RoboSuite和MimicGen为基础，在MuJoCo平台上构建的高保真双臂桌面操作任务仿真环境。DexMimicGen涵盖9类典型双臂任务，提出了增强版real2sim2real数据自动生成技术，只需60段真实人类演示便可生成2.1万条高质量仿真数据。相比原版MimicGen，该框架显著提升了数据生成效率和真实感，使机器人双臂协作任务的仿真训练更具实用性。
* **FUSE Dataset** [ICRA 2025] [website](https://fuse-model.github.io/) 包含26,866条远程操控轨迹，涵盖桌面抓取、购物袋内抓取和按钮按压三类任务。机器人通过Meta Oculus Quest 2 VR头显操作，任务结合语言指令和复杂视觉遮挡，支持多传感器与语言融合的机器人策略研究。
* **BiPlay Dataset** [website](https://dit-policy.github.io/):为了解决现有双臂数据集任务单一、环境固定的问题，BiPlay数据集采用随机物体和背景，采集多样化双臂操作轨迹。数据由多段3.5分钟的机器人操作视频拆分成7023个带语言任务描述的剪辑，总计10小时数据，支持双臂操作泛化研究。
* **DROID (Distributed Robot Interaction Dataset)**[website](https://droid-dataset.github.io/)：包含76,000条示范轨迹，约350小时交互数据，覆盖564个场景和86个任务。数据由50名采集员在北美、亚洲和欧洲12个月内收集，场景和任务多样性显著提升。基于DROID训练的策略表现更优、鲁棒性和泛化能力更强。数据集、训练代码及硬件搭建指南均已开源。
* **BridgeData V2**[website](https://rail-berkeley.github.io/bridgedata/)：包含60,096条轨迹数据，涵盖24个环境和13类技能，支持基于目标图像或自然语言指令的多任务开放词汇学习。数据主要采集自7个玩具厨房环境及多样桌面、洗衣机等场景，轨迹包括50,365条远程操控示范和9,731条脚本策略执行。每条轨迹均标注对应自然语言任务描述，促进跨环境和跨机构的技能泛化研究。
* **Ego4DSounds** [website](https://ego4dsounds.github.io/)：作为Ego4D大规模第一人称视角数据集的多模态子集，包含超过120万条视频剪辑，覆盖3000多个不同日常场景和行为，如烹饪、清洁、购物和社交等。数据强调动作与环境声音的高度对应，配备带时间戳的动作叙述，支持具身智能中动作感知、多模态融合及声音生成等任务的研究。
* **RH20T**[website](https://rh20t.github.io/)：人机交互数据集，包含丰富的人脸和语音信息，使用时需注意隐私保护，仅限模型训练。数据原始规模约40TB，提供尺寸缩减版（约5TB RGB，10TB RGB-D）。包含7组RGB视频及对应深度数据，附带相机标定和机器人关节角度信息。数据通过Google Drive和百度云公开下载。



<section id="paper_list"></section>

# 7. Paper Lists - 论文列表

* Awesome Humanoid Robot Learning - Yanjie Ze: [repo](https://github.com/YanjieZe/awesome-humanoid-robot-learning)
* Paper Reading List - DeepTimber Community: [repo](https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List)
* Paper List - Yanjie Ze: [repo](https://github.com/YanjieZe/Paper-List)
* Paper List For EmbodiedAI - Tianxing Chen: [repo](https://github.com/TianxingChen/Paper-List-For-EmbodiedAI)
* SOTA Paper Rating - Weiyang Jin: [website](https://waynejin0918.github.io/SOTA-paper-rating.io/)
* Awesome-LLM-Robotics: A repo contains a curative list of papers using Large Language/Multi-Modal Models for Robotics/RL: [website](https://github.com/GT-RIPL/Awesome-LLM-Robotics)
* Awesome-Video-Robotic-Papers - Yaoyao(Freax) Qian: [repo](https://github.com/H-Freax/Awesome-Video-Robotic-Papers)
* Awesome Embodied Robotics and Agent - Haonan Zhang: [repo](https://github.com/zchoi/Awesome-Embodied-Robotics-and-Agent)
* awesome-embodied-vla/va/vln - Qiang (Jony) ZHANG: [repo](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln)
* Awesome-Affordance-Learning - Hanqing Wang: [repo](https://github.com/hq-King/Awesome-Affordance-Learning)
<section id="acknowledgement"></section>

# 8. Acknowledgement - 致谢
本文转载/引用了一些博主的文章, 我们对他们的知识分享表示感谢, 引用列表如下：
[1] 知乎 [穆尧](https://www.zhihu.com/people/mu-yao-12-34), [2] 知乎 [东林钟声](https://www.zhihu.com/people/dong-lin-zhong-sheng-76), Github [Yunlong Dong](https://github.com/yunlongdong), [3] 知乎 [强化学徒](https://www.zhihu.com/people/heda-he-28), [4] 知乎 [Biang哥](https://www.zhihu.com/people/qi-da-guang), [5] OpenAI [Lilian Weng](https://lilianweng.github.io/), [6] B站 [木木具身](https://space.bilibili.com/350563565), [7] Github [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file), [8] 知乎 [Flood Sung](https://www.zhihu.com/people/flood-sung), [9] Github [Sida Peng](https://github.com/pengsida/learning_research)

<section id="cite"></section>

# 👍 Citation - 引用
If you find this repository helpful, please consider citing:

```
@misc{embodiedaiguide2025,
      title = {Embodied-AI-Guide},
      author = {Embodied-AI-Guide-Contributors, Lumina-Embodied-AI-Community},
      month = {January},
      year = {2025},
      url = {https://github.com/tianxingchen/Embodied-AI-Guide},
}
```

<section id="license"></section>

# 🏷️ License - 许可证
This repository is released under the MIT license. See [LICENSE](./LICENSE) for additional details.


<section id="star-history"></section>

# ⭐️ Star History - Star历史

[![Star History Chart](https://api.star-history.com/svg?repos=TianxingChen/Embodied-AI-Guide&type=Date)](https://star-history.com/#TianxingChen/Embodied-AI-Guide&Date)
