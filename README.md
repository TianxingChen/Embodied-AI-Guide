<h1 align="center">具身智能入门指南 Embodied-AI-Guide</h1>

<p align="center"> </p>


> Embodied AI（具身智能）入门的路径以及高质量信息的总结，期望是按照路线走完后，新手可以快速建立关于这个领域的认知，希望能帮助到各位入门具身智能的朋友，欢迎点Star、分享与提PR🌟~<br>【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Embodied-AI-Guide</a>, Latest Update: Dec 29, 2024 】<img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Ftianxingchen%2FEmbodied-AI-Guide&count_bg=%232B8DD9&title_bg=%237834C6&icon=github.svg&icon_color=%23E7E7E7&title=Page+Viewers&edge_flat=false"/> <img alt="GitHub repo stars" src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide">

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
        <li><a href="#llm_robot">3.4 LLM for Robotics - 大模型在机器人学中的应用</a></li>
        <li><a href="#cv">3.5 Computer Vision - 计算机视觉</a>
          <ul>
            <li><a href="#2dv">3.5.1 2D Vision - 二维视觉</a></li>
            <li><a href="#3dv">3.5.2 3D Vision - 三维视觉</a></li>
          </ul>
        </li>
        <li><a href="#embodied-ai-4-x">3.6 Embodied AI for X - 具身智能+X</a>
          <ul>
            <li><a href="#medical">3.6.1 Embodied AI for Healthcare - 具身智能+医疗</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#hardware">4. Hardware - 硬件</a>
      <ul>
        <li><a href="#embedded">4.1 Embedded - 嵌入式</a></li>
        <li><a href="#mechanical">4.2 Mechanical design - 机械设计</a></li>
        <li><a href="#robosystem">4.3 机器人硬件系统设计</a></li>
        <li><a href="#control">4.4 Control - 控制学</a></li>  
        <li><a href="#sensors">4.5 Sensors - 传感器</a></li>
        <li><a href="#companies">4.6 Companies - 公司</a></li>
      </ul>
    </li>
    <li><a href="#software">5. Software - 软件</a>
      <ul>
        <li><a href="#benchmarks">5.1 Benchmarks & Simulators - 基准 & 仿真器</a></li>
      </ul>
    </li>
    <li><a href="#paper_list">6. Paper Lists - 论文列表</a></li>
    <li><a href="#acknowledgement">7. Acknowledgement - 致谢</a></li>
  </ul>
</nav>


<section id="start"></section>

# 1. Start Up - 从这里开始

> 具身智能是指一种基于物理身体进行感知和行动的智能系统，其通过智能体与环境的交互获取信息、理解问题、做出决策并实现行动，从而产生智能行为和适应性。

## How - 如何食用这份指南

我们希望的是帮助新人快速建立领域认知，所以设计理念是：**简要**介绍目前具身智能涉及到的主要技术，让大家知道不同的技术能够解决什么问题，未来想要深入发展的时候能够有头绪。

## About us - 关于我们
我们是一个由具身初学者组成的团队，希望能够通过我们自己的学习经验，为后来者提供一些帮助，加快具身智能的普及。欢迎更多朋友加入我们的项目，也很欢迎交友、学术合作，有任何问题，可以联系邮箱`chentianxing2002@gmail.com`。

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (25' 港大PhD)</a>, <a href="https://yudezou.github.io/">邹誉德 (25' 上交-浦江实验室联培PhD)</a>, <a href="">陈思翔 (25' 北大PhD)</a>, <a href="https://github.com/27yw">叶雯 (25' 中科院自所PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (深大本科生)</a>, <a href="https://github.com/ShijiaPeng03">彭时佳 (深大本科生)</a>, <a href="https://gkw0010.github.io/">王冠锟 (港中文-华为联培PhD)</a>, <a href="https://ngchikit.github.io">吴志杰 (港中文PhD)</a>, <a href="https://github.com/csyufei">朱宇飞 (25' 上科大Ms)</a>.</p>
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

* 具身智能会投稿的较高质量会议与期刊：RSS, TRO, Science Robotics, IROS, ICRA, ICCV, ECCV, ICRA, AAAI, ICML, CVPR, NIPS, ICLR, IJRR, ACL等。

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

* 点云降采样: [zhihu](https://zhuanlan.zhihu.com/p/558683732?utm_campaign=shareopn&utm_medium=social&utm_psn=1772067996070236160&utm_source=wechat_session), 包括随机降采样、均匀降采样、最远点降采样、法线空间降采样等，需要了解清楚每一种降采样的优劣，这个技巧的选择对于3D应用来说是至关重要的。
* 手眼标定：[github](https://github.com/fishros/handeye-calib)，手眼标定用于确定相机和机械臂之间以及相机与相机之间的相对位置，大部分Project的开始都需要做一次手眼标定，分为眼在手上和眼在手外。


<section id="foundation-models"></section>

## 3.2 Foundation Models - 基础模型

> 以下是部分具身智能中常用的基础模型, 计算机视觉中发展的非常好的工具可以直接赋能具身智能的下游应用。

* CLIP: [website](https://github.com/openai/CLIP), 来自OpenAI的研究, 最基本的应用是可以计算图像与语言描述的相似度, 中间层的视觉特征对各种下游应用非常有帮助。

* DINO: [DINO repo](https://github.com/facebookresearch/dino), [DINO-v2 repo](https://github.com/facebookresearch/dinov2), 来自Meta的研究, 可以提供图像的高层视觉特征, 对corresponding之类的信息提取非常有帮助, 比如不同个体之间的鼻子都有类似的几何特征, 这个时候不同图像中关于不同鼻子的视觉特征值可能是近似的。

* SAM: [website](https://segment-anything.com/), 来自Meta的研究, 可以基于提示点或者框, 对图像的物体进行分割。

* SAM2: [website](https://ai.meta.com/sam2/), 来自Meta的研究, SAM的升级版, 可以在视频层面持续对物体进行分割追踪。

* Grounding-DINO: [repo](https://github.com/IDEA-Research/GroundingDINO), [在线尝试](https://deepdataspace.com/playground/grounding_dino), **这个DINO与上面Meta的DINO没有关系**, 是一个由IDEA研究院（做了很多不错开源项目的机构）开发集成的图像目标检测的框架，很多时候需要对目标物体进行检测的时候可以考虑使用。

* Grounded-SAM: [repo](https://github.com/IDEA-Research/Grounded-SAM-2), 比Grounding-DINO多了一个分割功能, 也就是支持检测后分割, 也有很多下游应用, 具体可以翻一下README。

* FoundationPose: [website](https://github.com/NVlabs/FoundationPose), 来自Nvidia的研究, 物体姿态追踪模型。

* Stable Diffusion: [repo](https://github.com/CompVis/stable-diffusion), [website](https://ommer-lab.com/research/latent-diffusion-models/), 22年的文生图模型, 现在虽然不是SOTA了, 但是依然可以作为不错的应用, 例如中间层特征支持下游应用、生成Goal Image (目标状态) 等等。

* Depth Anything (v1 & v2): [repo](https://github.com/LiheYoung/Depth-Anything), [repo](https://github.com/DepthAnything/Depth-Anything-V2), 港大和字节的研究工作，单目深度估计模型。

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
  * 实践[gymnasium](https://gymnasium.farama.org/)，可以尝试一下把玩一下登月着陆等经典强化学习场景，思考+动手，观察阶段agent的表现并分析，有助于深入理解强化学习
<!-- * UCB CS285 深度强化学习: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [youtube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps)<br> -->
<!-- * 强化学习的数学原理 - 西湖大学赵世钰: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665)<br> -->

<section id="il"></section>

### 3.3.2 Imitation Learning - 模仿学习

* 《模仿学习简洁教程》 - 南京大学LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
* Supervised Policy Learning for Real Robots, RSS 2024 Workshop 教程：真实机器人的监督策略学习, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if/?buvid=XY415384A771A6C681C9BEB3817566ED57724&is_story_h5=false&mid=ORgXkVzTHaOKTsml0RX5Gw%3D%3D&plat_id=240&share_from=ugc&share_medium=android&share_plat=android&share_source=WEIXIN&share_tag=s_i&spmid=dt.space-dt.0.0&timestamp=1721464513&unique_k=Cqj5d9J&up_id=2185804&vd_source=ab9cf5374617c2867aaea34af29b53c9)

<!-- * 实践[RoboTwin]() -->

<section id="llm_robot"></section>

## 3.4 LLM for Robotics - 大模型在机器人学中的应用
* Robotics+LLM系列通过大语言模型控制机器人 [2]: [zhihu](https://zhuanlan.zhihu.com/p/668053911)<br>
* Embodied Agent wiki: [website](https://en.wikipedia.org/wiki/Embodied_agent)<br>
* Lilian Weng 个人博客 - AI Agent 系统综述 [5]: 中文: [website](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) 英文: [website](https://lilianweng.github.io/posts/2023-06-23-agent/)<br>


<section id="cv"></section>

## 3.5 Computer Vision - 计算机视觉

CS231n (斯坦福计算机视觉课程): [website](https://cs231n.stanford.edu/schedule.html), 该课程对深度学习在计算机视觉的应用有较为全面的介绍。因为已经在具体实现某个论文的算法了，所以这个阶段可以不用做作业，只需要看课程视频和课程讲义即可。<br>

<section id="2dv"></section>

### 3.5.1 2D Vision - 二维视觉

* CNN (卷积神经网络): [link](https://easyai.tech/ai-definition/cnn/)

<section id="3dv"></section>

### 3.5.2 3D Vision - 三维视觉
第一阶段：学习最基础的3DV知识，追求广度，了解一些基础的概念和算法<br>
* 三维视觉导论 - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) （重点是完成课程里面的作业） <br>
* GAMES203 - 三维重建和理解: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS/?share_source=copy_web&vd_source=0b7603f37af6d369a97df34525b149be)<br>

第二阶段：细分方向，追求深度，上手一些项目<br>
* 如果对传统图形学感兴趣，可以看下面两门（闫令琪老师开的课，讲得特别好）:<br>
  * GAMES101 - 现代计算机图形学入门: [website](https://games-cn.org/intro-graphics/)<br>
  * GAMES202 - 高质量实时渲染: [website](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html)<br>
* 如果对motion synthesis/computer animation感兴趣，可以看:
  * GAMES105 - 计算机角色动画基础: [website](https://games-105.github.io/)<br>
* 如何对三维重建感兴趣，可以看下面两门:
  * Nerf原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1CC411V7oq/?spm_id_from=333.337.search-card.all.click&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
  * 3DGS原理代码讲解: [bilibili](https://www.bilibili.com/video/BV1zi421v7Dr?spm_id_from=333.788.recommend_more_video.-1&vd_source=930ef08bfb2ff0db87ec20bf72a99855)
* 三维预训练最新综述:
  * Advances in 3D pre-training and downstream tasks: a survey: [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>
* 3DGS在具身上的综述:
  * 3D Gaussian Splatting in Robotics: A Survey: [PDF](https://arxiv.org/pdf/2410.12262v2)<br>


<section id="embodied-ai-4-x"></section>

## 3.6 Embodied AI for X - 具身智能+X

<section id="medical"></section>

### 3.6.1 Embodied AI for Healthcare - 具身智能+医疗



#### 3.6.1.1 MLLM for Medical - 多模态大语言模型在医学中的应用
* SkinGPT-4 for dermatological diagnosis: [website](https://www.nature.com/articles/s41467-024-50043-3)<br>
* PneumoLLM for pneumoconiosis diagnosis: [website](https://www.sciencedirect.com/science/article/abs/pii/S1361841524001737)<br>
* BiomedGPT: [website](https://github.com/taokz/BiomedGPT)<br>
* LLAVA-Med: [website](https://github.com/microsoft/LLaVA-Med?tab=readme-ov-file)<br>
* RoboNurse-VLA: [website](https://robonurse-vla.github.io)<br>
Coming Soon...

<section id="hardware"></section>

# 4. Hardware - 硬件

> 具身智能硬件方面涵盖多个技术栈，如嵌入式软硬件设计，机械设计，机器人硬件系统设计，这部分知识比较繁杂，适合想要专注此方向的人

> 关于硬件部分的学习，最好从实践出发！

<section id="embedded"></section>

## 4.1 Embedded - 嵌入式
* 嵌入式学习路线:[CSDN](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452)
* 51单片机：[BiliBili](https://www.bilibili.com/video/BV1Mb411e7re/)经典江科大自动协出品
* Stm32单片机：[BiliBili](https://www.bilibili.com/video/BV1th411z7sn/)经典江科大自动协出品
* Stm32电机驱动：[BiliBili](https://www.bilibili.com/video/BV1AZ4y1V7wt/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)野火
* 野火Stm32标准库：[BiliBili](https://www.bilibili.com/video/BV1yW411Y7Gw/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)野火
* 正点原子Stm32：[BiliBili](https://www.bilibili.com/video/BV1Lx411Z7Qa/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)正点原子
* 韦东山嵌入式Linux：[BiliBili](https://www.bilibili.com/video/BV1w4411B7a4/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)韦东山

<section id="mechanical"></section>

## 4.2 Mechanical design - 机械设计

* SoildWorks教学：[BiliBili](https://www.bilibili.com/video/BV1iw411Z7HZ/?spm_id_from=333.337.search-card.all.click&vd_source=a83ed9f5a5c724720d224bdca866789e)
* URDF生成：[CSDN](https://blog.csdn.net/weixin_45168199/article/details/105755388)，指导如何通过SolidWorks装配体出发生成机器人URDF文件。
  
<section id="robosystem"></section>

## 4.3 机器人系统设计

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

  * 机械臂运动学
  > 想要快速了解什么是IK FK的同学可以看这个7分钟的短片，可以对此建立一个粗略的认知：[BiliBili](https://www.bilibili.com/video/BV18E411v7F9/?spm_id_from=333.337.search-card.all.click&vd_source=b14220472557bfa1918f3d0faa38bdc1)<br>
  > 较为简单的过一遍IK和FK的原理可以看这个：[CSDN](https://blog.csdn.net/Dwzsa/article/details/142386529?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&utm_relevant_index=6) 
    * IK (Inverse Kinematics) 逆运动学
      * 较为详细的视频课
        * [BiliBili IK(1)](https://www.bilibili.com/video/BV1PD4y1t7xP/?spm_id_from=333.337.search-card.all.click&vd_source=b14220472557bfa1918f3d0faa38bdc1)
        * [BiliBili IK(2)](https://www.bilibili.com/video/BV1Tt4y1T79Z?spm_id_from=333.788.recommend_more_video.0&vd_source=b14220472557bfa1918f3d0faa38bdc1)
      * 文字教学
        * [Book](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html)，较为详细的IK理论
      
    * FK (Forward Kinematics) 正运动学
      * 较为详细的视频课
        * [BiliBili FK(1)](https://www.bilibili.com/video/BV1Ve4y127Uf?spm_id_from=333.788.recommend_more_video.0&vd_source=b14220472557bfa1918f3d0faa38bdc1)
        * [BiliBili FK(2)](https://www.bilibili.com/video/BV1a14y157uL?spm_id_from=333.788.videopod.sections&vd_source=b14220472557bfa1918f3d0faa38bdc1)
   
    
    * 常用的库 
      * cuRobo：[cuRobo](https://curobo.org/)cuRobo是Nvidia的一个利用 CUDA 加速的机器人库，提供了一套高效的机器人算法，主要通过并行计算显著提升性能，包括但不限于IK，碰撞检测，路径规划等。
      * IKFast：[IKFast](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html)，经典IK库。
      * mplib：[mplib](https://github.com/haosulab/mplib)，Maniskill Benchmark以及Sapien仿真平台的IK库。

* ROS多传感器时间戳同步：[website](https://blog.csdn.net/qq_43495930/article/details/125649446)

* 动手实践LeRobot SO-100：[website](https://huggingface.co/lerobot)


<section id="sensors"></section>

## 4.5 Sensors - 传感器
Coming Soon ！

<section id="companies"></section>

## 4.6 Companies - 公司

| 公司 | 主营产品 | Others |
|-------|------|------|
| [松灵AgileX](https://www.agilex.ai/) | [pipper机械臂](https://www.agilex.ai/chassis/16)<br>移动底盘 | 面向教育科研
| [宇树Unitree](https://www.unitree.com/cn) | [Go2机器狗](https://www.unitree.com/cn/go2)<br>[通用人形H1](https://www.unitree.com/cn/h1)<br>[通用人形G1](https://www.unitree.com/cn/g1)<br> | 许多产出使用宇树的机器人作为硬件基础
| [方舟无限ARX](https://www.arx-x.com/?product/) | [X5机械臂](https://www.arx-x.com/?product/21.html)<br>[X7双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5机械臂](https://www.arx-x.com/?product/22.html)  | 适合复现很多经典的工作，eg. [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin松灵底盘+方舟臂](https://github.com/TianxingChen/RoboTwi)
| [波士顿动力](https://bostondynamics.com/)  | [spot机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas通用人形](https://bostondynamics.com/atlas/)  | 具身智能本体制造商，从液压驱动转向电机驱动 |
| [灵心巧手](https://www.linkerbot.cn/index) |  |  |
| [灵巧智能DexRobot](https://www.dex-robot.com/)| [Dexhand 021灵巧手](https://www.dex-robot.com/productionDexhand) | 19自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) |  | 已完成多轮融资 |
| [星海图Galaxea](http://galaxea.tech/) | [A1机械臂](http://galaxea.tech/Introducing_Galaxea_Robot/product_info/A1/#discover-more) |  |
| [World Labs](https://www.worldlabs.ai/) | | 专注于空间智能，致力于打造大型世界模型（LWM），以感知、生成并与 3D 世界进行交互。 [相关介绍](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1人形](https://www.robotera.com/goods/1.html)<br> [XHAND1灵巧手](https://www.robotera.com/goods/2.html) | |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1人形](https://boosterobotics.com/zh/store/)|  |
| [青龙机器人](https://www.openloong.net/) |  |  |
| [科技云深处](https://www.deeprobotics.cn/) |  [绝影X30四足机器人](https://www.deeprobotics.cn/robot/index/product3.html)<br> [Dr.01人形机器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技)](http://www.orca3d.cn/) |  | 具身智能仿真平台供应商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能数据平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [A2人形机器人](https://www.zhiyuan-robot.com/products/A2)<br>[A2-D数据采集机器人（轮式人形）](https://www.zhiyuan-robot.com/products/A2_D) |  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://air.tsinghua.edu.cn/info/1147/2175.htm)  |  |  |
| [穹彻智能](https://www.noematrix.ai/) | | |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) | | |
| [具身风暴机器人](https://www.robotstorm.tech) | |  |

<section id="software"></section>

# 5. Software - 软件

<section id="benchmarks"></section>

## 5.1 Benchmarks & Simulators - 基准 & 仿真器
具身智能常用benchmark总结 [1]: [zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
常见仿真器wiki: [wiki](https://simulately.wiki/)
| 仿真器 | 基准 |
|-------|------|
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K(可跨平台)](https://behavior.stanford.edu/behavior-1k)+[omniGibson(工具链)](https://behavior.stanford.edu/omnigibson/)<br>[ARNOID](https://arnold-benchmark.github.io/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html)+[robomimic(工具链)](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics(Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](Docs.qq.com/sheet/DYmppSU55cFNpaVJo?tab=BB08J2)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| [Genesis](https://genesis-embodied-ai.github.io/) ||

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
本文转载/引用了一些博主的文章，我们对他们的知识分享表示感谢，引用列表如下：
[1] 知乎 [穆尧](https://www.zhihu.com/people/mu-yao-12-34), [2] 知乎 [东林钟声](https://www.zhihu.com/people/dong-lin-zhong-sheng-76), Github [Yunlong Dong](https://github.com/yunlongdong), [3] 知乎 [强化学徒](https://www.zhihu.com/people/heda-he-28), [4] 知乎 [Biang哥](https://www.zhihu.com/people/qi-da-guang), [5] OpenAI [Lilian Weng](https://lilianweng.github.io/), [6] B站 [木木具身](https://space.bilibili.com/350563565), [7] Github [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file), [8] 知乎 [Flood Sung](https://www.zhihu.com/people/flood-sung), [9] Github [Sida Peng](https://github.com/pengsida/learning_research)

# 🏷️ License - 许可证
This repository is released under the MIT license. See LICENSE for additional details.

