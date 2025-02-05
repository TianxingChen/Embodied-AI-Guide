<h1 align="center">具身智能入门指南 Embodied-AI-Guide</h1>

<p align="center"> </p>


> Embodied AI（具身智能）入门的路径以及高质量信息的总结, 期望是按照路线走完后, 新手可以快速建立关于这个领域的认知, 希望能帮助到各位入门具身智能的朋友, 欢迎点Star、分享与提PR🌟~<br>【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Embodied-AI-Guide</a>, Latest Update: Feb. 5, 2025 】<img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Ftianxingchen%2FEmbodied-AI-Guide&count_bg=%232B8DD9&title_bg=%237834C6&icon=github.svg&icon_color=%23E7E7E7&title=Page+Viewers&edge_flat=false"/> <img alt="GitHub repo stars" src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide">


# Contents - 目录

<nav>
  <ul>
    <li><a href="#start">1. Start Up - 从这里开始</a></li>
    <li><a href="#info">2. Useful Info - 有利于搭建认知的资料</a></li>
    <li><a href="#algorithm">3. Algorithm - 算法</a>
      <ul>
        <li><a href="#common-tools">3.1 Common Tools - 常用工具</a></li>
        <li><a href="#foundation-models">3.2 Foundation Models - 基础模型</a></li>
        <li><a href="#robot-learning">3.3 Robot Learning - 机器人学习</a>
          <ul>
            <li><a href="#rl">3.3.1 Reinforcement Learning - 强化学习</a></li>
            <li><a href="#il">3.3.2 Imitation Learning - 模仿学习</a></li>
          </ul>
        </li>
        <li><a href="#llm_robot">3.4 LLM for Robotics - 大语言模型在机器人学中的应用</a></li>
        <li><a href="#cv">3.5 Computer Vision - 计算机视觉</a>
          <ul>
            <li><a href="#2dv">3.5.1 2D Vision - 二维视觉</a></li>
            <li><a href="#3dv">3.5.2 3D Vision - 三维视觉</a></li>
            <li><a href="#4dv">3.5.3 4D Vision - 四维视觉</a></li>
          </ul>
        </li>
        <li><a href="#mm"> 3.6 Multimodal Models - 多模态模型</a></li>  
        <li><a href="#embodied-ai-4-x">3.7 Embodied AI for X - 具身智能+X</a>
          <ul>
            <li><a href="#medical">3.7.1 Embodied AI for Healthcare - 具身智能+医疗</a></li>
            <li><a href="#uav">3.7.2 UAV - 无人机</a></li>
            <li><a href="#ad">3.7.2 Autonomous Driving - 自动驾驶</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#hardware">4. Hardware - 硬件</a>
      <ul>
        <li><a href="#embedded">4.1 Embedded - 嵌入式</a></li>
        <li><a href="#mechanical">4.2 Mechanical Design - 机械设计</a></li>
        <li><a href="#robosystem">4.3 Robot System Design - 机器人系统设计</a></li>
        <li><a href="#control">4.4 Control - 控制学</a></li>  
        <li><a href="#sensors">4.5 Sensors - 传感器</a></li>
        <li><a href="#companies">4.6 Companies - 公司</a></li>
      </ul>
    </li>
    <li><a href="#software">5. Software - 软件</a>
      <ul>
        <li><a href="#simulators">5.1 Simulators - 仿真器</a></li>
        <li><a href="#benchmarks">5.2 Benchmarks  - 基准集</a></li>
        <li><a href="#datasets">5.3 Datasets  - 数据集</a></li>
      </ul>
    </li>
    <li><a href="#paper_list">6. Paper Lists - 论文列表</a></li>
    <li><a href="#acknowledgement">7. Acknowledgement - 致谢</a></li>
    <li><a href="#license">🏷️ License - 许可证</a></li>
    <li><a href="#star-history">⭐️ Star History - Star历史</a></li>
  </ul>
</nav>


<section id="start"></section>

# 1. Start Up - 从这里开始

> 具身智能是指一种基于物理身体进行感知和行动的智能系统, 其通过智能体与环境的交互获取信息、理解问题、做出决策并实现行动, 从而产生智能行为和适应性。

## How - 如何食用这份指南

我们希望的是帮助新人快速建立领域认知, 所以设计理念是：**简要**介绍目前具身智能涉及到的主要技术, 让大家知道不同的技术能够解决什么问题, 未来想要深入发展的时候能够有头绪。

## About us - 关于我们
我们是一个由具身初学者组成的团队, 希望能够通过我们自己的学习经验, 为后来者提供一些帮助, 加快具身智能的普及。欢迎更多朋友加入我们的项目, 也很欢迎交友、学术合作, 有任何问题, 可以联系邮箱`chentianxing2002@gmail.com`。

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (25' 港大PhD)</a>, <a href="https://github.com/ShijiaPeng03">彭时佳 (深大本科生)</a>, <a href="https://metaphysicist0.github.io/">姚天亮 (25' 港中文PhD)</a>, <a href="https://yudezou.github.io/">邹誉德 (25' 上交-浦江实验室联培PhD)</a>, <a href="">陈思翔 (25' 北大PhD)</a>, <a href="https://github.com/csyufei">朱宇飞 (25' 上科大Ms)</a>, <a href="https://hao-starrr.github.io/">王文灏 (UPenn GRASP Lab Ms)</a>, <a href="">贾越如 (北大 Ms)</a>,<a href="https://gkw0010.github.io/">王冠锟 (港中文-华为联培PhD)</a>, <a href="https://ngchikit.github.io">吴志杰 (港中文PhD)</a>, <a href="https://github.com/27yw">叶雯 (25' 中科院自所PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (深大本科生)</a>, <a href="https://hbhalpha.github.io">侯博涵 (山大本科生)</a>.</p> 
<a href="https://github.com/TianxingChen/Embodied-AI-Guide/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=TianxingChen/Embodied-AI-Guide" />
</a>

<section id="info"></section>

# 2. Useful Info - 有利于搭建认知的资料

* 具身智能基础技术路线-YunlongDong [2]: [PDF](./files/具身智能基础技术路线-YunlongDong.pdf), [bilibili](https://www.bilibili.com/video/BV1d5ukedEsi/?buvid=XXCD799C01878A6CFDECF3FB4427E2F070877&from_spmid=default-value&is_story_h5=false&mid=iWFclAyh36UYMh2G6ZcsDw%3D%3D&p=1&plat_id=114&share_from=ugc&share_medium=android&share_plat=android&share_session_id=9c0dccf5-ec0b-4369-8b89-ff1d848467ee&share_source=WEIXIN&share_tag=s_i&spmid=united.player-video-detail.0.0&timestamp=1716466406&unique_k=Q0CaIUj&up_id=249218043)

* 社交媒体:

  * 可以关注的公众号: **石麻日记 (超高质量!!!)**, 机器之心, 新智元, 量子位, Xbot具身知识库, 具身智能之心, 自动驾驶之心, 3D视觉工坊, 将门创投, RLCN强化学习研究, CVHub

  * AI领域值得关注的博主列表 [3]: [zhihu](https://zhuanlan.zhihu.com/p/682110383)

* Robotics实验室总结 [4]: [zhihu_1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608), [zhihu_2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)

* 具身智能会投稿的较高质量会议与期刊：RSS, TRO, Science Robotics, IROS, ICRA, ICCV, ECCV, AAAI, ICML, CVPR, NIPS, ICLR, IJRR, ACL等。

* 斯坦福机器人学导论：[website](https://www.bilibili.com/video/BV17T421k78T/?spm_id_from=333.337.search-card.all.click)

* 共建全网最全具身智能知识库 [6]: [website](https://yv6uc1awtjc.feishu.cn/wiki/WPTzw9ON0ivIVrkLjVocNZh8nLf)

* 社区:
  * DeepTimber Robotics Innovations Community, 深木科研交流社区: [website](https://gamma.app/public/DeepTimber-Robotics-Innovations-Community-A-Community-for-Multi-m-og0uv8mswl1a3q7?mode=doc)
  * 宇树具身智能社群: [website](https://www.unifolm.com/#/)
  * Simulately: Handy information and resources for physics simulators for robot learning research: [website](https://simulately.wiki/)
  * DeepTimber-地瓜机器人社区: [website](https://cn.developer.d-robotics.cc/forumList?id=156&title=Deeptimber)
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

## 3.2 Foundation Models - 基础模型

> 以下是部分具身智能中常用的基础模型, 计算机视觉中发展的非常好的工具可以直接赋能具身智能的下游应用。

* CLIP: [website](https://github.com/openai/CLIP), 来自OpenAI的研究, 最基本的应用是可以计算图像与语言描述的相似度, 中间层的视觉特征对各种下游应用非常有帮助。

* DINO: [DINO repo](https://github.com/facebookresearch/dino), [DINO-v2 repo](https://github.com/facebookresearch/dinov2), 来自Meta的研究, 可以提供图像的高层视觉特征, 对corresponding之类的信息提取非常有帮助, 比如不同个体之间的鼻子都有类似的几何特征, 这个时候不同图像中关于不同鼻子的视觉特征值可能是近似的。

* SAM: [website](https://segment-anything.com/), 来自Meta的研究, 可以基于提示点或者框, 对图像的物体进行分割。

* SAM2: [website](https://ai.meta.com/sam2/), 来自Meta的研究, SAM的升级版, 可以在视频层面持续对物体进行分割追踪。

* Grounding-DINO: [repo](https://github.com/IDEA-Research/GroundingDINO), [在线尝试](https://deepdataspace.com/playground/grounding_dino), **这个DINO与上面Meta的DINO没有关系**, 是一个由IDEA研究院（做了很多不错开源项目的机构）开发集成的图像目标检测的框架, 很多时候需要对目标物体进行检测的时候可以考虑使用。

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

<section id="rl"></section>

### 3.3.1 Reinforcement Learning - 强化学习
* 推荐直接跟着李宏毅老师一套走: bilibili上课+刷蘑菇书巩固+gymnasium动手实践, 重点了解一下PPO。
  * 台湾大学李宏毅公开课: [bilibili](https://www.bilibili.com/video/BV1XP4y1d7Bk/?spm_id_from=333.337.search-card.all.click&vd_source=ab9cf5374617c2867aaea34af29b53c9)<br>
  * EasyRL - 蘑菇书: [website](https://datawhalechina.github.io/easy-rl/#/), 基本是配套李宏毅老师的课程<br>
  * 实践[gymnasium](https://gymnasium.farama.org/), 可以尝试一下把玩一下登月着陆等经典强化学习场景, 思考+动手, 观察阶段agent的表现并分析, 有助于深入理解强化学习
<!-- * UCB CS285 深度强化学习: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [youtube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps)<br> -->
<!-- * 强化学习的数学原理 - 西湖大学赵世钰: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665)<br> -->

<section id="il"></section>

### 3.3.2 Imitation Learning - 模仿学习

* 《模仿学习简洁教程》 - 南京大学LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
* Supervised Policy Learning for Real Robots, RSS 2024 Workshop 教程：真实机器人的监督策略学习, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if/?buvid=XY415384A771A6C681C9BEB3817566ED57724&is_story_h5=false&mid=ORgXkVzTHaOKTsml0RX5Gw%3D%3D&plat_id=240&share_from=ugc&share_medium=android&share_plat=android&share_source=WEIXIN&share_tag=s_i&spmid=dt.space-dt.0.0&timestamp=1721464513&unique_k=Cqj5d9J&up_id=2185804&vd_source=ab9cf5374617c2867aaea34af29b53c9)

<!-- * 实践[RoboTwin]() -->

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
* 利用LLM的code能力实现具身智能是一个有趣的想法
  * 经典工作(1) Code as Policy: [Arxiv](https://arxiv.org/abs/2209.07753)<br>
  * 经典工作(2) Instruction2Act: [Arxiv](https://arxiv.org/abs/2305.11176)<br>
* 有一些工作将三维视觉感知同LLM结合起来，共同促进具身智能规划
  * VoxPoser [Arxiv](https://arxiv.org/abs/2307.05973)<br>
  * OmniManip [Arxiv](https://arxiv.org/abs/2501.03841)<br>

<section id="cv"></section>

## 3.5 Computer Vision - 计算机视觉

CS231n (斯坦福计算机视觉课程): [website](https://cs231n.stanford.edu/schedule.html), 该课程对深度学习在计算机视觉的应用有较为全面的介绍。因为已经在具体实现某个论文的算法了, 所以这个阶段可以不用做作业, 只需要看课程视频和课程讲义即可。<br>

<section id="2dv"></section>

### 3.5.1 2D Vision - 二维视觉
* 2D Vision 领域的经典代表作
  * CNN (卷积神经网络): [link](https://easyai.tech/ai-definition/cnn/)
  * ResNet (深度残差网络): [bilibili](https://www.bilibili.com/video/BV1P3411y7nn/?spm_id_from=333.1387.collection.video_card.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * ViT (第一个将Transformer用在视觉领域): [bilibili](https://www.bilibili.com/video/BV15P4y137jb/?spm_id_from=333.1387.collection.video_card.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * Swin Transformer (披着Transformer皮的CNN): [bilibili](https://www.bilibili.com/video/BV13L4y1475U/?spm_id_from=333.1387.collection.video_card.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * 对比学习论文综述: [bilibili](https://www.bilibili.com/video/BV19S4y1M7hm/?spm_id_from=333.1387.collection.video_card.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
* 以判别式模型为主的感知任务, 比如识别、分类、分割、检测等等, 看看即可, 现在继续刷点意义不大
* 生成式模型
  * 自回归综述: [PDF](https://arxiv.org/pdf/2411.05902)
  * 扩散模型综述: [PDF](https://arxiv.org/pdf/2209.00796)
  * 如果对扩散模型的理论推导感兴趣, 可以看苏剑林老师的博客 - 生成扩散模型漫谈(推导非常清楚): [link](https://kexue.fm/archives/9119)

<section id="3dv"></section>

### 3.5.2 3D Vision - 三维视觉
第一阶段：学习最基础的3DV知识, 追求广度, 了解一些基础的概念和算法<br>
* 三维视觉导论 - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) （重点是完成课程里面的作业） <br>
* GAMES203 - 三维重建和理解: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS/?share_source=copy_web&vd_source=0b7603f37af6d369a97df34525b149be)<br>

第二阶段：细分方向, 追求深度, 上手一些项目<br>
* 如果对传统图形学感兴趣, 可以看下面两门（闫令琪老师开的课, 讲得特别好）:<br>
  * GAMES101 - 现代计算机图形学入门: [website](https://games-cn.org/intro-graphics/)<br>
  * GAMES202 - 高质量实时渲染: [website](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html)<br>
* 如果对motion synthesis/computer animation感兴趣, 可以看:
  * GAMES105 - 计算机角色动画基础: [website](https://games-105.github.io/)<br>
* 如果对三维重建感兴趣, 可以看下面两门:
  * Nerf原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1CC411V7oq/?spm_id_from=333.337.search-card.all.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * 3DGS原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1zi421v7Dr?spm_id_from=333.788.recommend_more_video.-1&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
* 三维预训练最新综述:
  * Advances in 3D pre-training and downstream tasks: a survey: [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>
* 3DGS在具身上的综述:
  * 3D Gaussian Splatting in Robotics: A Survey: [PDF](https://arxiv.org/pdf/2410.12262v2)<br>
* 三维生成的一些经典论文:
  * Diffusion Model for 2D/3D Generation 相关论文分类: [link](https://zhuanlan.zhihu.com/p/617510702)
  * 3D生成相关论文-2024: [link](https://zhuanlan.zhihu.com/p/700895749)

<section id="4dv"></section>

### 3.5.3 4D Vision - 四维视觉
* 视频理解
  * 开山之作: [bilibili](https://www.bilibili.com/video/BV1mq4y1x7RU/?spm_id_from=333.1387.collection.video_card.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * 论文串讲: [bilibili](https://www.bilibili.com/video/BV1fL4y157yA?spm_id_from=333.788.videopod.sections&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * LLM时代的视频理解综述: [PDF](https://arxiv.org/pdf/2312.17432)
* 4D 生成
  * 视频生成博客(英文): [link](https://lilianweng.github.io/posts/2024-04-12-diffusion-video/)
  * 4D 生成的论文列表: [website](https://github.com/cwchenwang/awesome-4d-generation)

<section id="mm"></section>

## 3.6 Multimodal Models - 多模态模型

> 多模态旨在统一来自不同模态信息的表征, 在具身智能中由于面对着机器识别的视觉信息与人类自然语言的引导信息等不同模态的信息，多模态技术愈发重要。
* 最经典的工作CLIP: [知乎](https://zhuanlan.zhihu.com/p/493489688)<br>
* 多模态大语言模型的经典工作 LLaVA: [website](https://llava-vl.github.io/)<br>

<section id="embodied-ai-4-x"></section>

## 3.7 Embodied AI for X - 具身智能+X

<section id="medical"></section>

### 3.7.1 Embodied AI for Healthcare - 具身智能+医疗

> 具身智能技术的迅猛发展正在引领医疗服务模式迈向革命性的新纪元。作为人工智能算法、先进机器人技术与生物医学深度融合的前沿交叉学科, 具身智能+医疗这一研究领域不仅突破了传统医疗的边界, 更开创了智能化医疗的新范式。其多学科协同创新的特质, 正在重塑医疗服务的全流程, 为精准医疗、远程诊疗和个性化健康管理带来前所未有的发展机遇, 推动医疗行业向更智能、更人性化的方向转型升级。这一领域的突破性进展, 标志着医疗科技正迈向一个全新的智能化时代。

#### 3.7.1.1 MLLM for Medical - 多模态大语言模型在医学中的应用
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

#### 3.7.1.2 Medical Robotics - 医疗机器人
* 医疗机器人的五级自动化（医疗机器人领域行业共识）, 杨广中教授于2017年在Science Robotics上的论著: [Medical robotics—Regulatory, ethical, and legal considerations for increasing levels of autonomy](https://www.science.org/doi/pdf/10.1126/scirobotics.aam8638)<br>
* 医疗机器人的十年回顾(含医疗机器人的不同分类), 杨广中教授在Science Robotics上的综述文章：[A decade retrospective of medical robotics research from 2010 to 2020](https://www.science.org/doi/epdf/10.1126/scirobotics.abi8017)<br>
* 医疗具身智能的分级: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/pdf/2501.07468?)<br>
* Artificial intelligence meets medical robotics, 2023年发表在Science正刊上的论著: [website](https://www.science.org/doi/abs/10.1126/science.adj3312)<br>

* 医疗机器人的机器视觉
  * 3DGS在腔镜手术中的应用综述: [website](https://arxiv.org/pdf/2408.04426)<br>

* 达芬奇手术机器人是最为常用的外科手术机器人, 对于这类机器人自主技能操作的研究最为广泛
  * 通过模仿学习在达芬奇机器人上学习外科手术操作任务 Surgical Robot Transformer (SRT): [website](https://surgical-robot-transformer.github.io/)<br>
  * Domain-specific Simulators - 手术机器人技能学习领域的模拟器
    * SurRoL: RL-Centered and dVRK Compatible Platform for Surgical Robot Learning [website](https://med-air.github.io/SurRoL/)<br>
    * Surgical Gym: A high-performance GPU-based platform for surgical robot learning (ICRA 2024, work in progress, based on NVIDIA Omniverse): [website](https://github.com/SamuelSchmidgall/SurgicalGym)<br>
    * ORBIT-Surgical: An Open-Simulation Framework for Learning Surgical Augmented Dexterity  (ICRA 2024, based on NVIDIA Omniverse): [website](https://orbit-surgical.github.io/)<br>

* 连续体和软体手术机器人作为柔性医疗机器人的重要分支, 凭借其独特的结构设计和材料特性, 在微创介入诊疗领域展现出显著优势。它们能够灵活进入人体狭窄腔体, 实现精准操作, 同时最大限度地减小手术创口, 降低患者术后恢复时间及感染风险, 为现代微创手术提供了创新性的技术解决方案。
  * 连续体机器人在医疗领域的应用 (Nabil Simaan; Howie Choset等): [Continuum Robots for Medical Interventions](https://ieeexplore.ieee.org/abstract/document/9707607)<br>
  * 软体手术机器人在微创介入手术中的应用 (Ka-wai Kwok; Kaspar Althoefer等)： [Soft Robot-Assisted Minimally Invasive Surgery and Interventions: Advances and Outlook](https://ieeexplore.ieee.org/abstract/document/9765966/authors#authors)<br>
> 连续体和软体机器人因其超冗余自由度和高度非线性的结构特性, 采用传统的控制与传感方法构建正逆运动学方程时面临显著的计算复杂性和建模局限性。传统方法难以精确描述其多自由度耦合运动及环境交互中的动态响应。为此, 基于数据驱动的智能控制方法（如深度学习、强化学习及自适应控制算法）成为解决这一问题的前沿方向。这些方法能够通过大量数据训练, 高效学习系统的非线性映射关系, 显著提升运动控制的精度、自适应性和鲁棒性, 为复杂医疗场景下的机器人操作提供了更为可靠的技术支撑。
  * 什么是软体机器人？软体机器人的具身智能定义: [知乎, by Ke WU from MBUZAI](https://www.zhihu.com/question/61637360/answer/92834447300?utm_psn=1870238291607040000)<br>
  * IROS 2024大会Program Chair新加坡国立大学Cecilia Laschi教授的论著: [Learning-Based Control Strategies for Soft Robots: Theory, Achievements, and Future Challenges](https://ieeexplore.ieee.org/abstract/document/10136428)<br>
  * 软体机器人中具身智能物理建模简明指南（也是出自NUS Cecilia教授团队）: [A concise guide to modelling the physics of embodied intelligence in soft robotics](https://inria.hal.science/hal-03921606/document)<br>
  * 数据驱动方法在软体机器人建模与控制中的应用: [Data-driven methods applied to soft robot modeling and control: A review](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10477253)<br>

* 微纳机器人技术是一类集成了微纳米制造、生物工程和智能控制等多学科前沿技术的微型机器人系统。凭借其微纳米级的独特尺寸、优异的生物相容性和精准的操控性能，这一前沿技术为现代医学诊疗范式带来了突破性创新。在精准诊断方面，微纳机器人能够深入人体微观环境，实现细胞乃至分子水平的实时监测；在靶向治疗领域，其可作为智能药物载体，实现病灶部位的精准定位与可控释放；在微创手术应用中，微纳机器人系统为复杂外科手术提供了前所未有的精确操作平台。这些创新性应用不仅显著提升了诊疗效率，更为攻克重大疾病提供了全新的技术途径，推动着现代医学向更精准、更微创、更智能的方向发展。
  * 微纳机器人的机器学习(CUHK 张立教授团队在Nature Machine Intelligence上的论著): [Machine learning for micro- and nanorobots](https://www.nature.com/articles/s42256-024-00859-x)<br>

<section id="uav"></section>

### 3.7.2 UAV - 无人机
Coming Soon !

<section id="ad"></section>

### 3.7.3 Autonomous Driving - 自动驾驶
Coming Soon !

<section id="hardware"></section>

# 4. Hardware - 硬件

> 具身智能硬件方面涵盖多个技术栈, 如嵌入式软硬件设计, 机械设计, 机器人系统设计, 这部分知识比较繁杂, 适合想要专注此方向的人
> 关于硬件部分的学习, 最好从实践出发！

<section id="embedded"></section>

## 4.1 Embedded - 嵌入式
* 嵌入式学习路线: [CSDN](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452)
* 51单片机：[BiliBili](https://www.bilibili.com/video/BV1Mb411e7re/), 经典江科大自动协出品
* Stm32单片机：[BiliBili](https://www.bilibili.com/video/BV1th411z7sn/), 经典江科大自动协出品
* Stm32电机驱动：[BiliBili](https://www.bilibili.com/video/BV1AZ4y1V7wt/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e), 野火
* 野火Stm32标准库：[BiliBili](https://www.bilibili.com/video/BV1yW411Y7Gw/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e), 野火
* 正点原子Stm32：[BiliBili](https://www.bilibili.com/video/BV1Lx411Z7Qa/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e), 正点原子
* 韦东山嵌入式Linux：[BiliBili](https://www.bilibili.com/video/BV1w4411B7a4/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e), 韦东山

<section id="mechanical"></section>

## 4.2 Mechanical Design - 机械设计

* SoildWorks教学：[BiliBili](https://www.bilibili.com/video/BV1iw411Z7HZ/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)
* URDF生成：[CSDN](https://blog.csdn.net/weixin_45168199/article/details/105755388), 指导如何通过SolidWorks装配体出发生成机器人URDF文件。
  
<section id="robosystem"></section>

## 4.3 Robot System Design - 机器人系统设计

* 《机器人学简介》, 来自[2]做的高质量教材: [PDF](./files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf)

* 《机器人系统教材》: [website](https://motion.cs.illinois.edu/RoboticSystems/)

<section id="control"></section>

## 4.4 Control - 控制学

* ROS基础:
  * 具身智能ROS1基础: [website](http://www.autolabor.com.cn/book/ROSTutorials/)
  * 具身智能ROS2基础: [website](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)
  
* 基础控制理论:
  * PID控制：[CSDN](https://blog.csdn.net/name_longming/article/details/115093338)
  * 彻底搞懂阻抗控制、导纳控制、力位混合控制: [CSDN](https://blog.csdn.net/a735148617/article/details/108564836)
  * Modern Control Systems (14th edition), Robert. H. Bishop, Richard. C, Dorf. z: [Book](http://103.203.175.90:81/fdScript/RootOfEBooks/E%20Book%20collection%20-%202024/EEE/Modern_control_systems_Robert_H_Bishop_Richard_C_Dorf_z_lib_org.pdf#page=1.00&gsr=0)

  * 机械臂运动学
  > 想要快速了解什么是IK FK的同学可以看这个7分钟的短片, 可以对此建立一个粗略的认知：[BiliBili](https://www.bilibili.com/video/BV18E411v7F9/?spm_id_from=333.337.search-card.all.click&vd_source=b14220472557bfa1918f3d0faa38bdc1)<br>
  > 较为简单的过一遍IK和FK的原理可以看这个：[CSDN](https://blog.csdn.net/Dwzsa/article/details/142386529?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&utm_relevant_index=6) 
    * IK (Inverse Kinematics) 逆运动学
      * 较为详细的视频课
        * [BiliBili IK(1)](https://www.bilibili.com/video/BV1PD4y1t7xP/?spm_id_from=333.337.search-card.all.click&vd_source=b14220472557bfa1918f3d0faa38bdc1)
        * [BiliBili IK(2)](https://www.bilibili.com/video/BV1Tt4y1T79Z?spm_id_from=333.788.recommend_more_video.0&vd_source=b14220472557bfa1918f3d0faa38bdc1)
      * 文字教学
        * [Book](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html), 较为详细的IK理论
      
    * FK (Forward Kinematics) 正运动学
      * 较为详细的视频课
        * [BiliBili FK(1)](https://www.bilibili.com/video/BV1Ve4y127Uf?spm_id_from=333.788.recommend_more_video.0&vd_source=b14220472557bfa1918f3d0faa38bdc1)
        * [BiliBili FK(2)](https://www.bilibili.com/video/BV1a14y157uL?spm_id_from=333.788.videopod.sections&vd_source=b14220472557bfa1918f3d0faa38bdc1)
          
   * 经典教材
     * 《机构学与机器人学的几何基础与旋量代数》 戴建生院士 著
     * 《现代机器人学：机构、规划与控制》凯文·M. 林奇, 朴钟宇 著
     * 《机器人学的现代数学理论基础》丁希仑 著
    
    * 常用的库 
      * cuRobo：[cuRobo](https://curobo.org/), cuRobo是Nvidia的一个利用 CUDA 加速的机器人库, 提供了一套高效的机器人算法, 主要通过并行计算显著提升性能, 包括但不限于IK, 碰撞检测, 路径规划等。
      * IKFast：[IKFast](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html), 经典IK库。
      * mplib：[mplib](https://github.com/haosulab/mplib), Maniskill Benchmark以及Sapien仿真平台的IK库。

* ROS多传感器时间戳同步：[website](https://blog.csdn.net/qq_43495930/article/details/125649446)

* 动手实践LeRobot SO-100：[website](https://huggingface.co/lerobot)


<section id="sensors"></section>

## 4.5 Sensors - 传感器
Coming Soon !

<section id="companies"></section>

## 4.6 Companies - 公司

| 公司 | 主营产品 | Others |
|-------|------|------|
| [松灵AgileX](https://www.agilex.ai/) | [pipper机械臂](https://www.agilex.ai/chassis/16)<br>移动底盘 | 面向教育科研
| [宇树Unitree](https://www.unitree.com/cn) | [Go2机器狗](https://www.unitree.com/cn/go2)<br>[通用人形H1](https://www.unitree.com/cn/h1)<br>[通用人形G1](https://www.unitree.com/cn/g1)<br> | 许多产出使用宇树的机器人作为硬件基础
| [方舟无限ARX](https://www.arx-x.com/?product/) | [X5机械臂](https://www.arx-x.com/?product/21.html)<br>[X7双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5机械臂](https://www.arx-x.com/?product/22.html)  | 适合复现很多经典的工作, eg. [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin松灵底盘+方舟臂](https://github.com/TianxingChen/RoboTwi)
| [波士顿动力](https://bostondynamics.com/)  | [spot机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas通用人形](https://bostondynamics.com/atlas/)  | 具身智能本体制造商, 从液压驱动转向电机驱动 |
| [灵心巧手](https://www.linkerbot.cn/index) |  |  |
| [灵巧智能DexRobot](https://www.dex-robot.com/)| [Dexhand 021灵巧手](https://www.dex-robot.com/productionDexhand) | 19自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) |  | 已完成多轮融资 |
| [星海图Galaxea](http://galaxea.tech/) | [A1机械臂](http://galaxea.tech/Introducing_Galaxea_Robot/product_info/A1/#discover-more) |  |
| [World Labs](https://www.worldlabs.ai/) | | 专注于空间智能, 致力于打造大型世界模型（LWM）, 以感知、生成并与 3D 世界进行交互。 [相关介绍](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1人形](https://www.robotera.com/goods/1.html)<br> [XHAND1灵巧手](https://www.robotera.com/goods/2.html) | |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1人形](https://boosterobotics.com/zh/store/)|  |
| [青龙机器人](https://www.openloong.net/) |  |  |
| [科技云深处](https://www.deeprobotics.cn/) |  [绝影X30四足机器人](https://www.deeprobotics.cn/robot/index/product3.html)<br> [Dr.01人形机器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | 具身智能仿真平台供应商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能数据平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [A2人形机器人](https://www.zhiyuan-robot.com/products/A2)<br>[A2-D数据采集机器人（轮式人形）](https://www.zhiyuan-robot.com/products/A2_D) |  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://air.tsinghua.edu.cn/info/1147/2175.htm)  |  |  |
| [穹彻智能](https://www.noematrix.ai/) | | |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) | | |
| [具身风暴](https://www.robotstorm.tech) | | 落地具身智能通用按摩机器人 |

<section id="software"></section>

# 5. Software - 软件

<section id="benchmarks"></section>

## 5.1 Simulators 仿真器
常见仿真器wiki: [wiki](https://simulately.wiki/)
| 仿真器 | 对应基准集 |
|-------|------|
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K(可跨平台)](https://behavior.stanford.edu/behavior-1k)+[omniGibson(工具链)](https://behavior.stanford.edu/omnigibson/)<br>[ARNOID](https://arnold-benchmark.github.io/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html)+[robomimic(工具链)](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics(Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](Docs.qq.com/sheet/DYmppSU55cFNpaVJo?tab=BB08J2)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| [Genesis](https://genesis-embodied-ai.github.io/) ||
| [SOFA](https://github.com/sofa-framework/sofa/)| 常用于软体机器人的仿真 |

## 5.2 Banchmarks 基准集
具身智能常用benchmark总结 [1]: [zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
* **CALVIN**, [github](https://github.com/mees/calvin), [website](http://calvin.cs.uni-freiburg.de/)2022年, 第一个公开的结合了自然语言控制、高维多模态输入、7自由度的机械臂控制以及长视野的机器人操纵benchmark。支持不同的语言指令, 不同的摄像头输入, 不同的控制方式, 主要用来评估具身智能模型的多模态输入的能力和长程规划能力。
* **Meta-World**, [webpage](https://meta-world.github.io/): 评估机器人在多任务和元强化学习场景下的表现。50个机器人操作任务（如抓取、推动物体、开门等）, 组织成不同的基准测试集（如ML1、ML10、ML45、MT10、MT50等）, 每个集合都有明确的训练任务和测试任务。周边和文档比较全面, 基于mojoco, 有完整的API和工具, python import即可运行。
* **Embodied Agent Interface: Benchmarking LLMs for Embodied Decision Making**, [website](https://embodied-agent-interface.github.io/): 主要评估大型语言模型（LLMs）在具身决策中的表现, 重点在于决策过程, 包括目标解释、子目标分解、动作序列化和状态转换建模, 不涉及到具体的执行。
* **RoboGen**, [repo](https://github.com/Genesis-Embodied-AI/RoboGen), [website](https://robogen-ai.github.io/): 不是生成policy, 而是生成任务、场景和带标记的数据, 能直接用来监督学习。
* **LIBERO**, [repo](https://github.com/Lifelong-Robot-Learning/LIBERO), [website](https://libero-project.github.io/intro.html): 用一个程序化生成管道来生成任务, 这个管道理论上可以生成无限数量的操作任务, 还提供了：三种视觉运动策略网络架构（RNN、Transformer和ViLT） 和 三种终身学习算法, 以及顺序微调和多任务学习的基准。
* **RoboTwin**, [repo](https://github.com/TianxingChen/RoboTwin): 使用程序生成双臂机器人无限操作任务数据, 并提供了所有任务的评测基准。

## 5.3 Datasets 数据集
* **Open X-Embodiment: Robotic Learning Datasets and RT-X Models**, [website](https://robotics-transformer-x.github.io/):  22种不同机器人平台的超过100万条真实机器人轨迹数据，覆盖了527种不同的技能和160,266项任务，主要集中在抓取和放置。
* **AgiBot World Datasets (智元机器人)**, [website](https://agibot-world.com/): 八十余种日常生活中的多样化技能，超过100万条轨迹数据，采集自**同构型机器人**, 多级质量把控和全程人工在环的策略，从采集员的专业培训，到采集过程中的严格管理，再到数据的筛选、审核和标注，每一个环节都经过了精心设计和严格把控。
* **RoboMIND**, [website](https://www.robomind.net/): 55,000条真实世界的演示轨迹，涵盖了279个不同任务和61个独特物体类别，来自四种不同协作臂，任务被分为基础技能、精准操作、场景理解、柜体操作和协作任务五大类。



<section id="paper_list"></section>

# 6. Paper Lists - 论文列表

* Awesome Humanoid Robot Learning - Yanjie Ze: [repo](https://github.com/YanjieZe/awesome-humanoid-robot-learning)
* Paper Reading List - DeepTimber Community: [repo](https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List)
* Paper List - Yanjie Ze: [repo](https://github.com/YanjieZe/Paper-List)
* Paper List For EmbodiedAI - Tianxing Chen: [repo](https://github.com/TianxingChen/Paper-List-For-EmbodiedAI)
* SOTA Paper Rating - Weiyang Jin: [website](https://waynejin0918.github.io/SOTA-paper-rating.io/)
* Awesome-LLM-Robotics: A repo contains a curative list of papers using Large Language/Multi-Modal Models for Robotics/RL: [website](https://github.com/GT-RIPL/Awesome-LLM-Robotics)

<section id="acknowledgement"></section>

# 7. Acknowledgement - 致谢
本文转载/引用了一些博主的文章, 我们对他们的知识分享表示感谢, 引用列表如下：
[1] 知乎 [穆尧](https://www.zhihu.com/people/mu-yao-12-34), [2] 知乎 [东林钟声](https://www.zhihu.com/people/dong-lin-zhong-sheng-76), Github [Yunlong Dong](https://github.com/yunlongdong), [3] 知乎 [强化学徒](https://www.zhihu.com/people/heda-he-28), [4] 知乎 [Biang哥](https://www.zhihu.com/people/qi-da-guang), [5] OpenAI [Lilian Weng](https://lilianweng.github.io/), [6] B站 [木木具身](https://space.bilibili.com/350563565), [7] Github [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file), [8] 知乎 [Flood Sung](https://www.zhihu.com/people/flood-sung), [9] Github [Sida Peng](https://github.com/pengsida/learning_research)

<section id="license"></section>

# 🏷️ License - 许可证
This repository is released under the MIT license. See LICENSE for additional details.

<section id="cite"></section>

<section id="star-history"></section>

# ⭐️ Star History - Star历史

[![Star History Chart](https://api.star-history.com/svg?repos=TianxingChen/Embodied-AI-Guide&type=Date)](https://star-history.com/#TianxingChen/Embodied-AI-Guide&Date)
