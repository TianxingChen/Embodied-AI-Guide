<h1 align="center">具身智能中文指南</h1>

<p align="center">【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Github Repo</a>, Latest Update: Dec 17, 2024 】 <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Ftianxingchen%2FEmbodied-AI-Guide&count_bg=%232B8DD9&title_bg=%237834C6&icon=github.svg&icon_color=%23E7E7E7&title=Page+Viewers&edge_flat=false"/></a></p>

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (25' 港大PhD)</a>, <a href="https://yudezou.github.io/">邹誉德 (25' 上交-浦江实验室联培PhD)</a>, <a href="">陈思翔 (25' 北大PhD)</a>, <a href="https://github.com/27yw">叶雯 (25'  中科院自动化所PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (深大本科生)</a>, <a href="https://github.com/ShijiaPeng03">彭时佳 (深大本科生)</a></p>

> Embodied AI (具身智能)入门的路径以及useful信息的总结，期望是按照路线走完后，新手可以快速建立关于这个领域的认知，希望能帮助到各位入门具身智能的朋友,欢迎star与PR🌟~<br>文章中引用文章的原作者，我们在[🙏 Acknowledgement - 致谢](#acknowledgement)部分进行了致谢，感谢他们的分享🌹<br><a href="https://hits.seeyoufarm.com">

## Contents - 目录
<nav>
  <ul>
    <li><a href="#start">Start Up - 从这里开始</a></li>
    <li><a href="#info">Useful Info - 有利于搭建认知的资料</a></li>
    <li><a href="#paper_list">Paper Lists - 论文列表</a></li>
    <li><a href="#rl">Reinforcement Learning - 强化学习</a></li>
    <li><a href="#il">Imitation Learning - 模仿学习</a></li>
    <li><a href="#llm_robot">LLM for Robotics - 大模型在机器人学中的应用</a></li>
    <li><a href="#3dv">3D Vision - 三维视觉</a></li>
    <li><a href="#control">Control - 控制学</a></li>
    <li><a href="#benchmarks">Benchmarks & Simulators - 基准 & 仿真器</a></li>
    <li><a href="#communities">Communities - 社区</a></li>
    <li><a href="#companies">Companies - 公司</a></li>
    <li><a href="#acknowledgement">🙏 Acknowledgement - 致谢</a></li>
  </ul>
</nav>

<section id="start"></section>

## Start Up - 从这里开始

**什么是具身智能？**<br>
具身智能是指一种基于物理身体进行感知和行动的智能系统，其通过智能体与环境的交互获取信息、理解问题、做出决策并实现行动，从而产生智能行为和适应性。


<section id="info"></section>

## Useful Info - 有利于搭建认知的资料
具身智能基础技术路线-YunlongDong [2]: [PDF](./files/具身智能基础技术路线-YunlongDong.pdf), [bilibili](https://www.bilibili.com/video/BV1d5ukedEsi/?buvid=XXCD799C01878A6CFDECF3FB4427E2F070877&from_spmid=default-value&is_story_h5=false&mid=iWFclAyh36UYMh2G6ZcsDw%3D%3D&p=1&plat_id=114&share_from=ugc&share_medium=android&share_plat=android&share_session_id=9c0dccf5-ec0b-4369-8b89-ff1d848467ee&share_source=WEIXIN&share_tag=s_i&spmid=united.player-video-detail.0.0&timestamp=1716466406&unique_k=Q0CaIUj&up_id=249218043)

AI领域值得关注的博主列表 [3]: [zhihu](https://zhuanlan.zhihu.com/p/682110383)

Robotics实验室总结 [4]: [zhihu_1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608), [zhihu_2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)

<section id="paper_list"></section>

## Paper Lists - 论文列表

* Paper List For EmbodiedAI - Tianxing Chen: [https://github.com/TianxingChen/Paper-List-For-EmbodiedAI](https://github.com/TianxingChen/Paper-List-For-EmbodiedAI)
* Awesome Humanoid Robot Learning - Yanjie Ze: [https://github.com/YanjieZe/awesome-humanoid-robot-learning](https://github.com/YanjieZe/awesome-humanoid-robot-learning)
* Paper List - Yanjie Ze: [https://github.com/YanjieZe/Paper-List](https://github.com/YanjieZe/Paper-List)
* Paper Reading List - DeepTimber Community: [https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List](https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List)


<section id="rl"></section>

## Reinforcement Learning - 强化学习
UCB CS285 深度强化学习: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [youtube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps)<br>
台湾大学李宏毅公开课: [bilibili](https://www.bilibili.com/video/BV1XP4y1d7Bk/?spm_id_from=333.337.search-card.all.click&vd_source=ab9cf5374617c2867aaea34af29b53c9)<br>
EasyRL - 蘑菇书: [website](https://datawhalechina.github.io/easy-rl/#/)<br>
强化学习的数学原理 - 西湖大学赵世钰: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665)<br>
实践[gymnasium](https://gymnasium.farama.org/)，可以尝试一下把玩一下登月着陆等经典强化学习场景，思考+动手，观察阶段agent的表现并分析，有助于深入理解强化学习

<section id="il"></section>

## Imitation Learning - 模仿学习
模仿学习简洁教程 - 南京大学LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
Supervised Policy Learning for Real Robots, RSS 2024 Workshop 教程：真实机器人的监督策略学习, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if/?buvid=XY415384A771A6C681C9BEB3817566ED57724&is_story_h5=false&mid=ORgXkVzTHaOKTsml0RX5Gw%3D%3D&plat_id=240&share_from=ugc&share_medium=android&share_plat=android&share_source=WEIXIN&share_tag=s_i&spmid=dt.space-dt.0.0&timestamp=1721464513&unique_k=Cqj5d9J&up_id=2185804&vd_source=ab9cf5374617c2867aaea34af29b53c9)

<section id="llm_robot"></section>

## LLM for Robotics - 大模型在机器人学中的应用
Robotics+LLM系列通过大语言模型控制机器人 [2]: [zhihu](https://zhuanlan.zhihu.com/p/668053911)<br>
PDDL-wiki: [website](https://planning.wiki/)<br>
An Introduction to PDDL: [PDF](https://www.cs.toronto.edu/~sheila/2542/s14/A1/introtopddl2.pdf)<br>
AI Agent from IBM: An artificial intelligence (AI) agent refers to a system or program that is capable of autonomously performing tasks on behalf of a user or another system by designing its workflow and utilizing available tools.<br>
Embodied Agent wiki: [website](https://en.wikipedia.org/wiki/Embodied_agent)<br>
Awesome-LLM-Robotics: A repo contains a curative list of papers using Large Language/Multi-Modal Models for Robotics/RL. [website](https://github.com/GT-RIPL/Awesome-LLM-Robotics)<br>
Lilian Weng 个人博客 - AI Agent 系统综述 [5]: 中文: [website](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) 英文: [website](https://lilianweng.github.io/posts/2023-06-23-agent/)<br>


<section id="3dv"></section>

## 3D Vision - 三维视觉
三维视觉导论 - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/)<br>
GAMES203 - 三维重建和理解: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS/?share_source=copy_web&vd_source=0b7603f37af6d369a97df34525b149be)<br>
Advances in 3D pre-training and downstream tasks: a survey. [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>

### 3DGS
3D Gaussian Splatting原理速通: [bilibili](https://www.bilibili.com/video/BV11e411n79b/?spm_id_from=333.788&vd_source=ab9cf5374617c2867aaea34af29b53c9)

<section id="control"></section>

## Control - 控制学
PID控制：[CSDN](https://blog.csdn.net/name_longming/article/details/115093338)
彻底搞懂阻抗控制、导纳控制、力位混合控制: [CSDN](https://blog.csdn.net/a735148617/article/details/108564836)<br>
具身智能ROS1基础: [website](http://www.autolabor.com.cn/book/ROSTutorials/)<br>
具身智能ROS2基础: [website](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)<br>
机器人系统教材: [website](https://motion.cs.illinois.edu/RoboticSystems/)<br>
动手实践Lerobot SO-100：[website](https://github.com/huggingface/lerobot/blob/main/examples/10_use_so100.md)<br>
斯坦福机器人学导论：[website](https://www.bilibili.com/video/BV17T421k78T/?spm_id_from=333.337.search-card.all.click)<br>
台大机器人学导论：[website](https://www.bilibili.com/video/BV1Z34y1q7sZ/?spm_id_from=333.337.search-card.all.click)<br>
共建全网最全具身智能知识库：[website](https://yv6uc1awtjc.feishu.cn/wiki/WPTzw9ON0ivIVrkLjVocNZh8nLf)<br>
ROS多传感器时间戳同步：[website](https://blog.csdn.net/qq_43495930/article/details/125649446)

关于控制部分的学习，最好从实践出发！

<section id="benchmarks"></section>

## Benchmarks & Simulators - 基准 & 仿真器
具身智能常用benchmark总结 [1]: [zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
常见仿真器wiki: [wiki](https://simulately.wiki/)
| 仿真器 | 基准 |
|-------|------|
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K(可跨平台)](https://behavior.stanford.edu/behavior-1k)+[omniGibson(工具链)](https://behavior.stanford.edu/omnigibson/)<br>[ARNOID](https://arnold-benchmark.github.io/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html)+[robomimic(工具链)](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics(Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](Docs.qq.com/sheet/DYmppSU55cFNpaVJo?tab=BB08J2)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |


<section id="communities"></section>

## Communities - 社区
> 以下部分资料引用自[7]

DeepTimber Robotics Innovations Community, 深木科研交流社区: [website](https://gamma.app/public/DeepTimber-Robotics-Innovations-Community-A-Community-for-Multi-m-og0uv8mswl1a3q7?mode=doc)

宇树具身智能社群: [website](https://www.unifolm.com/#/)

Simulately: Handy information and resources for physics simulators for robot learning research: [website](https://simulately.wiki/)

DeepTimber-地瓜机器人社区: [website](https://cn.developer.d-robotics.cc/forumList?id=156&title=Deeptimber)

HuggingFace LeRobot (Europe, check the Discord): [website](https://github.com/huggingface/lerobot)

K-scale labs (US, check the Discord): [website](https://kscale.dev/)




<section id="companies"></section>

## Companies - 公司

| 公司 | 主营产品 | Others |
|-------|------|------|
| [松灵AgileX](https://www.agilex.ai/) | [pipper机械臂](https://www.agilex.ai/chassis/16)<br>移动底盘 | 面向教育科研
| [宇树Unitree](https://www.unitree.com/cn) | [Go2机器狗](https://www.unitree.com/cn/go2)<br>[通用人形H1](https://www.unitree.com/cn/h1)<br>[通用人形G1](https://www.unitree.com/cn/g1)<br> | 许多产出使用宇树的机器人作为硬件基础
| [方舟无限ARX](https://www.arx-x.com/?product/) | [X5机械臂](https://www.arx-x.com/?product/21.html)<br>[X7双臂平台](https://www.arx-x.com/?product/23.html)<br>[R5机械臂](https://www.arx-x.com/?product/22.html)  | 适合复现很多经典的工作，eg. [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin松灵底盘+方舟臂](https://github.com/TianxingChen/RoboTwi)
| [波士顿动力](https://bostondynamics.com/)  | [spot机器狗](https://bostondynamics.com/products/spot/)<br>[Atlas通用人形](https://bostondynamics.com/atlas/)  | 具身智能本体制造商，从液压驱动转向电机驱动 |
| [灵心巧手]|  |  |
| [灵巧智能DexRobot](https://www.dex-robot.com/)| [Dexhand 021灵巧手](https://www.dex-robot.com/productionDexhand) | 19自由度量产灵巧手 |
| [银河通用](https://www.galbot.com/about) |  | 已完成多轮融资 |
| [星海图Galaxea](http://galaxea.tech/) | [A1机械臂](http://galaxea.tech/Introducing_Galaxea_Robot/product_info/A1/#discover-more) |  |
| [World Labs](https://www.worldlabs.ai/) | | 专注于空间智能，致力于打造大型世界模型（LWM），以感知、生成并与 3D 世界进行交互。 [相关介绍](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1人形](https://www.robotera.com/goods/1.html)<br> [XHAND1灵巧手](https://www.robotera.com/goods/2.html) | 由清华叉院陈建宇教授创建 |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1人形](https://boosterobotics.com/zh/store/)|  |

<section id="acknowledgement"></section>

<a name="acknowledgement"></a>

## 🙏 Acknowledgement - 致谢
本文转载/引用了大量博主的文章，我们对他们的知识分享表示感谢，引用列表如下：
| Since 2024 🌹 |  |  |  |  |
|------|------|------|------|------|
| [1] 知乎[穆尧](https://www.zhihu.com/people/mu-yao-12-34) | [2] 知乎[东林钟声](https://www.zhihu.com/people/dong-lin-zhong-sheng-76), Github[Yunlong Dong](https://github.com/yunlongdong) | [3] 知乎[强化学徒](https://www.zhihu.com/people/heda-he-28) | [4] 知乎[Biang哥](https://www.zhihu.com/people/qi-da-guang) | [5] OpenAI [Lilian Weng](https://lilianweng.github.io/) 
| [6] B站[木木具身](https://space.bilibili.com/350563565) | [7] [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file) |  |  |  |

## 🏷️ License - 许可证
This repository is released under the MIT license. See LICENSE for additional details.
