![](./files/Embodied-AI-Guide-logo.png)
<h1 align="center">Embodied AI Technology Guide Embodied-AI-Guide</h1>

<p align="center"> </p>


> Embodied AI (Embodied Intelligence) entry path and summary of high-quality information. Expecting that by following this path, newcomers can quickly establish an understanding of this field. Hope to help friends who want to enter embodied AI. Welcome to star, share, and submit PR 🌟~<br>【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Embodied-AI-Guide</a>, Latest Update: May 1, 2025 】<img alt="GitHub repo stars" src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide"> ![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FTianxingChen%2FEmbodied-AI-Guide&label=Total%20Visitors&labelColor=%232ccce4&countColor=%23d9e3f0)


**Language:** English | [简体中文](README.md) | [繁體中文](README_zh-TW.md)


# Lumina Embodied AI Community: [Click to Visit](https://lumina-embodied.ai)

> The Embodied-AI-Guide project will soon be uploaded as a wiki webpage on the Lumina Embodied AI Community website, stay tuned. If you are interested in collaborating to build the Lumina Embodied AI Community (currently more inclined towards institutional/community cooperation), please contact via email <a href="mailto:lumina.embodiedai@gmail.com">lumina.embodiedai@gmail.com</a> or WeChat <code>TianxingChen_2002</code> (please note institution + name and purpose)

**Scan the bottom right image to follow `Lumina Embodied AI` Community**:

<img src="./files/images/Lumina.png" alt="Task Descriptions">


# Contents - Table of Contents

<nav>
  <ul>
    <li><a href="#start-from-here">1. Start From Here</a></li>
    <li><a href="#info">2. Useful Info - Resources for Building Domain Knowledge</a></li>
    <li><a href="#algorithm">3. Algorithm - Algorithms</a>
      <ul>
        <li><a href="#common-tools">3.1 Common Tools - Common Tools</a></li>
        <li><a href="#foundation-models">3.2 Foundation Models - Foundation Models</a></li>
        <li><a href="#robot-learning">3.3 Robot Learning - Robot Learning</a>
          <ul>
            <li><a href="#robot_autonomy">3.3.1 ETH & TTIC & UdeM Robot Autonomy - Autonomous Robots</a></li>
            <li><a href="#mpc">3.3.2 Model Predictive Control - Model Predictive Control</a></li>
            <li><a href="#rl">3.3.3 Reinforcement Learning - Reinforcement Learning</a></li>
            <li><a href="#il">3.3.4 Imitation Learning - Imitation Learning</a></li>
            <li><a href="#mila_robot_learning">3.3.5 MILA & UdeM Robot Learning - Robot Learning Course</a></li>
            <li><a href="#cmu_robot_learning">3.3.6 CMU 16-831 Introduction to Robot Learning - Introduction to Robot Learning</a></li>
            <li><a href="#usc_robot_learning">3.3.7 USC CSCI 699: Robot Learning - Robot Learning</a></li>
            <li><a href="#mit_robot_manipulation">3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - Robotic Manipulation</a></li>
            <li><a href="#underactuated_robotics">3.3.9 MIT 6.8210: Underactuated Robotics - Underactuated Robotics</a></li>
          </ul>
        </li>
        <li><a href="#llm_robot">3.4 LLM for Robotics - LLM for Robotics</a></li>
        <li><a href="#vla">3.5 Vision-Language-Action Models - Vision-Language-Action Models</a></li>
        <li><a href="#cv">3.6 Computer Vision - Computer Vision</a>
          <ul>
            <li><a href="#2dv">3.6.1 2D Vision - 2D Vision</a></li>
            <li><a href="#3dv">3.6.2 3D Vision - 3D Vision</a></li>
            <li><a href="#4dv">3.6.3 4D Vision - 4D Vision</a></li>
            <li><a href="#vp">3.6.4 Visual Prompting - Visual Prompting</a></li>
            <li><a href="#ag">3.6.5 Affordance Grounding - Affordance Grounding</a></li>
          </ul>
        </li>
        <li><a href="#cg">3.7 Computer Graphics - Computer Graphics</a></li>  
        <li><a href="#mm">3.8 Multimodal Models - Multimodal Models</a></li>  
        <li><a href="#navigation">3.9 Robot Navigation - Robot Navigation</a></li>  
        <li><a href="#embodied-ai-4-x">3.10 Embodied AI for X - Embodied AI for X</a>
          <ul>
            <li><a href="#medical">3.10.1 EAI for Healthcare - Embodied AI for Healthcare</a></li>
            <li><a href="#uav">3.10.2 UAV - UAV</a></li>
            <li><a href="#ad">3.10.3 Autonomous Driving - Autonomous Driving</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#control">4 Control and Robotics - Control and Robotics Fundamentals</a>
      <ul>
        <li><a href="#41-control-theory-fundamentals">4.1 Control Theory Fundamentals</a></li>
        <ul>
          <li><a href="#411-classical-control-principles">4.1.1 Classical Control Principles</a></li>
          <li><a href="#412-modern-control-theory-linear-system-control">4.1.2 Modern Control Theory (Linear System Control)</a></li>
          <li><a href="#413-advanced-control-techniques">4.1.3 Advanced Control Techniques</a></li>
        </ul>
        <li><a href="#42-introduction-to-robotics">4.2 Introduction to Robotics</a></li>
        <ul>
          <li><a href="#421-recommended-materials">4.2.1 Recommended Materials</a></li>
          <li><a href="#422-robot-kinematics-and-dynamics">4.2.2 Robot Kinematics and Dynamics</a></li>
          <li><a href="#423-odometry-and-slam">4.2.3 Odometry and SLAM (Odometry & SLAM)</a></li>
          <li><a href="#424-miscellaneous">4.2.4 Miscellaneous</a></li>
        </ul>
      </ul>
    </li> 
    <li><a href="#hardware">5. Hardware - Hardware</a>
      <ul>
        <li><a href="#embedded">5.1 Embedded - Embedded</a></li>
        <li><a href="#mechanical">5.2 Mechanical Design - Mechanical Design</a></li>
        <li><a href="#robosystem">5.3 Robot System Design - Robot System Design</a></li>
        <li><a href="#sensors">5.4 Sensors - Sensors</a></li>
        <li><a href="#tactile">5.5 Tactile Sensing - Tactile Sensing</a></li>
        <li><a href="#companies">5.6 Companies - Companies</a></li>
      </ul>
    </li>
    <li><a href="#software">6. Software - Software</a>
      <ul>
        <li><a href="#simulators">6.1 Simulators - Simulators</a></li>
        <li><a href="#benchmarks">6.2 Benchmarks - Benchmarks</a></li>
        <li><a href="#datasets">6.3 Datasets - Datasets</a></li>
      </ul>
    </li>
    <li><a href="#paper_list">7. Paper Lists - Paper Lists</a></li>
    <li><a href="#acknowledgement">8. Acknowledgement - Acknowledgement</a></li>
    <li><a href="#cite">👍 Citation - Citation</a></li>
    <li><a href="#license">🏷️ License - License</a></li>
    <li><a href="#star-history">⭐️ Star History - Star History</a></li>
  </ul>
</nav>



<section id="start-from-here"></section>

# 1. Start From Here

> Embodied AI refers to an intelligent system based on a physical body for perception and action. It acquires information, understands problems, makes decisions, and implements actions through the interaction between the agent and the environment, thereby generating intelligent behavior and adaptability.

## How - How to Learn This Guide

We hope to help newcomers quickly establish an understanding of the field, so the design philosophy is: **briefly** introduce the main technologies currently involved in embodied AI, so that everyone knows what problems different technologies can solve, and have a clue when they want to develop in depth in the future.

## About us - About Us
We are a team composed of embodied AI beginners, hoping to provide some help to later generations through our own learning experience, and accelerate the popularization of embodied AI. We welcome more friends to join our project, and also welcome making friends and academic cooperation. For any questions, please contact the email `chentianxing2002@gmail.com`.

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (HKU PhD)</a>, <a href="https://github.com/kxwangzju">王开炫 (HKU PhD)</a>, <a href="https://jiayueru.github.io/">贾越如 (Peking University Ms)</a >, <a href="https://metaphysicist0.github.io/">姚天亮 (CUHK PhD)</a>, <a href="https://c7w.tech/about/">高焕昂 (Tsinghua PhD)</a>, <a href="https://axi404.top/">高宁 (Xi'an Jiaotong BS)</a>, <a href="https://github.com/guo-cq">郭常青 (Tsinghua Ms)</a>, <a href="https://shijiapeng03.github.io/">彭时佳 (SUSTech BS)</a>, <a href="https://yudezou.github.io/">邹誉德 (SJTU AILab Joint PhD)</a>, <a href="">陈思翔 (Peking University PhD)</a>, <a href="https://github.com/csyufei">朱宇飞 (SJTU Ms)</a>, <a href="https://github.com/LambdaGuard">韩翊飞 (Tsinghua Ms)</a>, <a href="https://hao-starrr.github.io/">王文灏 (UPenn Ms)</a>, <a href="https://github.com/StarCycle">李卓恒 (HKU PhD)</a>, <a href="https://github.com/GihhArwtw">邱一航 (HKU PhD)</a>, <a href="https://github.com/Henry-lsy">梁升一 (HKUST PhD)</a>, <a href="https://scholar.google.com/citations?user=azPXbWcAAAAJ&hl=en">林俊晓 (ZJU Ms)</a>, <a href="https://gkw0010.github.io/">王冠锟 (CUHK PhD)</a>, <a href="https://ngchikit.github.io">吴志杰 (CUHK PhD)</a>, <a href="https://github.com/27yw">叶雯 (CAS PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (SUSTech BS)</a>, <a href="https://hbhalpha.github.io">侯博涵 (SDU BS)</a>, <a href="https://github.com/Scodive">江恒乐 (SUSTech PhD)</a>, <a href="https://yongchao98.github.io/YongchaoChen/">陈勇超 (MIT+Harvard PhD)</a>, <a href="https://aaron617.github.io/">胡梦康 (HKU PhD)</a>, <a href="https://liang-zx.github.io/">梁志烜 (HKU PhD)</a>, <a href="https://yimouwu.github.io/">吴贻谋 (CUHK MPhil)</a>, <a href="https://warshallrho.github.io/">吴睿海 (Peking University PhD)</a>, <a href="https://yaomarkmu.github.io/">穆尧 (SJTU AP)</a>.</p> 

<a href="https://github.com/TianxingChen/Embodied-AI-Guide/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=TianxingChen/Embodied-AI-Guide" />
</a>

<section id="info"></section>

# 2. Useful Info - Resources for Building Domain Knowledge

* Embodied AI Basic Technology Roadmap - YunlongDong [2]: [PDF](./files/具身智能基础技术路线-YunlongDong.pdf), [bilibili](https://www.bilibili.com/video/BV1d5ukedEsi)

* Social Media:

  * WeChat Official Accounts to Follow: **Diary of Stone and Hemp (Super High Quality!!!)**, Machine Heart, New Intelligence, Quantum Bits, Xbot Embodied Knowledge Base, Embodied AI Heart, Autonomous Driving Heart, 3D Vision Workshop, Venture Capital Will, RLCN Reinforcement Learning Research, CVHub

  * List of Influential Bloggers in AI Field [3]: [zhihu](https://zhuanlan.zhihu.com/p/682110383)

* Robotics Lab Summary [4]: [zhihu_1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608), [zhihu_2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)

* High-quality conferences and journals for embodied AI submissions: Science Robotics, TRO, IJRR, JFR, RSS, IROS, ICRA, ICCV, ECCV, ICML, CVPR, NeurIPS, ICLR, AAAI, ACL, etc.

* Stanford Introduction to Robotics: [website](https://www.bilibili.com/video/BV17T421k78T)

* Cyber Nachos, [website](https://cybernachos.github.io/)

* Co-build the Most Comprehensive Embodied AI Knowledge Base on the Internet [6]: [website](https://yv6uc1awtjc.feishu.cn/wiki/WPTzw9ON0ivIVrkLjVocNZh8nLf)

* Awesome-Embodied-AI-Job (Embodied AI Job Board): [Repo](https://github.com/StarCycle/Awesome-Embodied-AI-Job/tree/main)

* Embodied Intelligence Chinese High-Impact Scholars List: [Repo](https://github.com/Will-Gao/Embodied_Intelligence)
  
* Communities:
  * Lumina Embodied AI Community: [website](https://lumina-embodied.ai)
  * DeepTimber Robotics Innovations Community: [website](https://gamma.app/public/DeepTimber-Robotics-Innovations-Community-A-Community-for-Multi-m-og0uv8mswl1a3q7?mode=doc)
  * Unitree Embodied AI Community: [website](https://www.unifolm.com/#/)
  * Simulately: Handy information and resources for physics simulators for robot learning research: [website](https://simulately.wiki/)
  * DeepTimber - Sweet Potato Robotics Community: [website](https://developer.d-robotics.cc/forumList?id=156&title=Deeptimber)
  * HuggingFace LeRobot (Europe, check the Discord): [website](https://github.com/huggingface/lerobot)
  * K-scale labs (US, check the Discord): [website](https://kscale.dev/)
  * OpenLoong Open Source Community: [website](https://www.openloong.org.cn/cn)

<section id="algorithm"></section>

# 3. Algorithm - Algorithms

<section id="common-tools"></section>

## 3.1 Common Tools - Common Tools

> This section shares common techniques in embodied AI.

* Point Cloud Downsampling: [zhihu](https://zhuanlan.zhihu.com/p/558683732?utm_campaign=shareopn&utm_medium=social&utm_psn=1772067996070236160&utm_source=wechat_session), including random downsampling, uniform downsampling, farthest point downsampling, normal space downsampling, etc. It is crucial to understand the pros and cons of each downsampling method, as the choice of this technique is vital for 3D applications.
* Hand-Eye Calibration: [github](https://github.com/fishros/handeye-calib), Hand-eye calibration is used to determine the relative positions between cameras and robotic arms, as well as between cameras. Most projects require hand-eye calibration at the beginning, divided into eye-in-hand and eye-to-hand.


<section id="foundation-models"></section>

## 3.2 Vision Foundation Models - Vision Foundation Models

> The following are some foundation models commonly used in embodied AI. Excellent tools developed in computer vision can directly empower downstream applications in embodied AI.

* CLIP: [website](https://github.com/openai/CLIP), From OpenAI's research, the most basic application is to calculate the similarity between images and language descriptions. The visual features of intermediate layers are very helpful for various downstream applications.

* DINO: [DINO repo](https://github.com/facebookresearch/dino), [DINO-v2 repo](https://github.com/facebookresearch/dinov2), [DINO-v3 repo](https://github.com/facebookresearch/dinov3), From Meta's research, it can provide high-level visual features of images, which is very helpful for information extraction like correspondences. For example, different individuals have similar geometric features for noses, so the visual feature values for different noses in different images may be similar.

* SAM: [website](https://segment-anything.com/), From Meta's research, it can segment objects in images based on prompt points or boxes.

* SAM2: [website](https://ai.meta.com/sam2/), From Meta's research, an upgraded version of SAM, which can continuously segment and track objects at the video level.

* SAM3: [website](https://ai.meta.com/sam3/), From Meta's research, an upgraded version of SAM2, capable of exhaustive segmentation of all instances specified by short text phrases.

* Grounding-DINO: [repo](https://github.com/IDEA-Research/GroundingDINO), [Try Online](https://deepdataspace.com/playground/grounding_dino), **This DINO is unrelated to the Meta DINO above**, it is an integrated image object detection framework developed by IDEA Research (an institution that has produced many good open-source projects). It can be considered when detecting target objects.

* OmDet-Turbo: [repo](https://github.com/om-ai-lab/OmDet), An open-source research by OmAI Lab, providing OVD (Open Vocabulary Detection) capabilities. The advantage is very fast inference speed (100+FPS), suitable for custom object detection scenarios requiring high FPS.

* Grounded-SAM: [repo](https://github.com/IDEA-Research/Grounded-SAM-2), It has an additional segmentation function compared to Grounding-DINO, that is, it supports segmentation after detection, and also has many downstream applications. You can check the README for details.

* FoundationPose: [website](https://github.com/NVlabs/FoundationPose), From Nvidia's research, an object pose tracking model.

* Stable Diffusion: [repo](https://github.com/CompVis/stable-diffusion), [website](https://ommer-lab.com/research/latent-diffusion-models/), A 2022 text-to-image model. Although not SOTA now, it can still be used for good applications, such as intermediate layer features supporting downstream applications, generating Goal Images (target states), etc.

* Depth Anything (v1 & v2 & v3): [repo](https://github.com/LiheYoung/Depth-Anything), [repo](https://github.com/DepthAnything/Depth-Anything-V2), [repo](https://github.com/ByteDance-Seed/Depth-Anything-3) Research work from HKU and ByteDance, a monocular depth estimation model.

* Point Transformer (v3): [repo](https://github.com/Pointcept/PointTransformerV3), Work on point cloud feature extraction.

* RDT-1B: [website](https://rdt-robotics.github.io/rdt-robotics/), Work by Tsinghua Professor Zhu Jun's team, a foundation model for dual-arm robotic manipulation, with strong few-shot capabilities.

* SigLIP: [huggingface](https://huggingface.co/docs/transformers/en/model_doc/siglip), Similar to CLIP.

<section id="robot-learning"></section>

## 3.3 Robot Learning - Robot Learning

The development of Robot Learning: [zhihu](https://zhuanlan.zhihu.com/p/26988866)

<section id="robot_autonomy"></section>

### 3.3.1 ETH & TTIC & UdeM Robot Autonomy - Autonomous Robots

[Course Video](https://www.edx.org/learn/technology/eth-zurich-self-driving-cars-with-duckietown) | [Course Website](https://duckietown.com/self-driving-cars-with-duckietown-mooc/)

This course is jointly offered by ETH Zurich, TTIC, and University of Montreal, explaining the construction process of autonomous robots around the Duckietown platform system, covering modules such as perception, control, modeling, and reinforcement learning. It emphasizes the complete perception-decision-control closed-loop system design, and promotes students to master building and deploying a robotic agent with autonomous navigation capabilities from scratch through project practice. Suitable for those who want to get a preliminary understanding of robotic systems and Robot Learning.

<section id="mpc"></section>

### 3.3.2 Model Predictive Control (MPC) - Model Predictive Control

Model Predictive Control (MPC) is an advanced control strategy that uses the system's explicit dynamic model to predict future behavior over a finite time horizon. At each control cycle, MPC determines the control input by solving an optimization problem to optimize the specified performance index while satisfying input and output constraints. The first control input in the optimized sequence is applied to the system, and the process is repeated at the next time step with the new system state measurement or estimate.

* Recommended introductory video:

    - Model Predictive Control from formulas to code - Huazhong University of Science and Technology Robotics Lab: [bilibili](https://www.bilibili.com/video/BV1U54y1J7wh); Simulation source code: [Gitee](https://gitee.com/clangwu/mpc_control.git) This course is suitable as an introductory course from PID to MPC, suitable for beginners who only understand PID control principles but not MPC principles; from formula derivation to CoppeliaSim (V-REP) simulation tutorial and MATLAB code writing, easy to understand.
    
* Classic works:
  
    **Theoretical Foundations**:
    - [Model predictive control: Theory and practice—A survey](https://www.sciencedirect.com/science/article/abs/pii/0005109889900022): This comprehensive survey paper discusses the theoretical foundations and practical applications of MPC, laying the foundation for future research.

    **Nonlinear MPC**:
    - [An Introduction to Nonlinear Model Predictive Control](https://pure.tue.nl/ws/files/3079152/555518.pdf#page=120): Provides a concise introduction to nonlinear MPC, extending MPC applications in systems with significant nonlinearity.

    **Explicit MPC**:
    - [The explicit linear quadratic regulator for constrained systems](https://www.sciencedirect.com/science/article/abs/pii/S0005109801001741): Discusses the formulation of explicit MPC solutions, crucial for systems requiring fast real-time control.

    **Robust MPC**:
    - [Predictive End-Effector Control of Manipulators on Moving Platforms Under Disturbance](https://ieeexplore.ieee.org/document/9425004): Uses time series analysis to predict base motion and accordingly transform the desired trajectory, allowing the manipulator to achieve active base motion under disturbance. It is a classic work using quadratic programming (QP) to formulate MPC problems.
    - [Min-max feedback model predictive control for constrained linear systems](https://ieeexplore.ieee.org/abstract/document/704989): Addresses robustness in MPC, proposing methods to handle model uncertainty and ensure performance under disturbances.

    **Learning-Based MPC**:
    - [Learning-Based Model Predictive Control for Safe Exploration](https://ieeexplore.ieee.org/abstract/document/8619572): Combines machine learning with MPC, representing the modern trend of incorporating data-driven models and learning into control.
    - [Confidence-Aware Object Capture for a Manipulator Subject to Floating-Base Disturbances](https://ieeexplore.ieee.org/document/10684104): Uses wavelet neural networks for real-time motion prediction, and introduces confidence evaluation to achieve optimal trajectory planning in short cycles, enabling excellent performance of the manipulator in capturing UAVs on disturbed platforms with good robustness.

<section id="rl"></section>

### 3.3.3 Reinforcement Learning - Reinforcement Learning

* Mathematical Principles of Reinforcement Learning - Xihu University Shi Yu Zhao: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665) [GitHub](https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning) This course is very suitable as an introductory course to reinforcement learning, suitable for beginners who have some understanding of machine learning but have not learned reinforcement learning. It allows understanding the mathematical principles of reinforcement learning, and the textbook is also very well written.

#### Deep Reinforcement Learning - Deep Reinforcement Learning

Here are three popular courses related to deep reinforcement learning. These courses have some overlap, with different lengths and teaching styles, so readers can choose the one that suits them. In addition, papers on classic algorithms in deep reinforcement learning are also in the must-read list: such as [PPO](https://arxiv.org/abs/1707.06347), [SAC](https://proceedings.mlr.press/v80/haarnoja18b/haarnoja18b.pdf), [TRPO](https://arxiv.org/abs/1502.05477), [A3C](https://arxiv.org/abs/1602.01783), etc.

* The Foundations of Deep RL in 6 Lectures [YouTube](https://www.youtube.com/watch?v=2GwBez0D20A) This online course is taught by the famous Pieter Abbeel professor in the RL field, introducing the main knowledge of deep reinforcement learning in six lectures starting from MDP.

* UC Berkeley CS285 Deep Reinforcement Learning: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [YouTube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps) The instructor of this course is the famous Sergey Levine professor from Berkeley in the RL field, and many famous works in DRL such as SAC come from him. Sergey is very attentive in teaching, and this course provides a very detailed introduction to DRL.

* Teacher Li Hongyi also has a set of courses on reinforcement learning: Watch on bilibili + consolidate with the Mushroom Book + practice with gymnasium, focus on understanding PPO.

  * National Taiwan University Li Hongyi Open Course: [bilibili](https://www.bilibili.com/video/BV1XP4y1d7Bk)

  * EasyRL - Mushroom Book: [website](https://datawhalechina.github.io/easy-rl/#/), basically accompanying Teacher Li Hongyi's course

  * Practice [gymnasium](https://gymnasium.farama.org/), you can try playing with classic reinforcement learning scenarios like lunar landing, think and do it yourself, observe the agent's performance at each stage and analyze it, which helps deepen understanding of reinforcement learning

However, reward tuning and parameter adjustment in deep reinforcement learning are very experience-dependent. It is recommended that after having relevant experience in deep reinforcement learning, readers can try training a policy themselves and deploying it on a robot to experience the Sim-to-Real Gap. Commonly used simulation platforms include [MuJoCo PlayGround](https://playground.mujoco.org/), [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html), [SAPIEN](https://sapien.ucsd.edu/), [Genesis](https://github.com/Genesis-Embodied-AI/Genesis), etc.

Common codebases include [legged-gym](https://github.com/leggedrobotics/legged_gym) (developed by ETH RSL, based on IsaacGym), etc. You can also find similar codebases based on the task you want to do.

<section id="il"></section>

### 3.3.4 Imitation Learning - Imitation Learning

* "Concise Tutorial on Imitation Learning" - Nanjing University LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
* Supervised Policy Learning for Real Robots, RSS 2024 Workshop Tutorial: Supervised Policy Learning for Real Robots, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if)

<section id="mila_robot_learning"></section>

### 3.3.5 MILA & UdeM Robot Learning - Robot Learning Course

[Course Video](https://www.youtube.com/playlist?list=PLMe2pHxzxHp-UJ1jd-uuGSGK7P7Phtm-f) | [Course Website](https://fracturedplane.notion.site/Robot-Learning-IFT6163-Scaling-Learning-for-Real-World-Agents-Apprentissage-robotique-Apprentiss-14a2148572768017864af202952c4b7e)

A course offered by MILA and University of Montreal, focusing on extending methods like deep reinforcement learning to robotic agents in the real world, mainly exploring the limitations of existing learning technologies and studying how to build more robust and generalizable agent systems. Suitable for students who want to understand the cutting-edge applications of machine learning and reinforcement learning algorithms in the robotics field.

<section id="cmu_robot_learning"></section>

### 3.3.6 CMU 16-831 Introduction to Robot Learning - Introduction to Robot Learning

[Lecture Slides](https://16-831-s24.github.io/lectures/) | [Homework](https://github.com/kavin-cmu/16831-S24-HW)

A course offered by CMU Robotics Institute. Although there are no videos, the lecture slides are concise and insightful, providing a comprehensive coverage of Robot Learning, highly recommended.

<section id="usc_robot_learning"></section>

### 3.3.7 USC CSCI 699: Robot Learning - Robot Learning

[Course Homepage](https://liralab.usc.edu/csci699/)

A course offered by the University of Southern California, rich in RL-related content, emphasizing connections between concepts, with a lot of intuition.

<section id="mit_robot_manipulation"></section>

### 3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - Robotic Manipulation

[Course Homepage](https://manipulation.csail.mit.edu/Fall2024/index.html) | [E-book](https://manipulation.mit.edu/)

A course offered by MIT CSAIL, rich and hardcore content, providing a comprehensive introduction to robotic manipulation, including perception, planning, dynamics, and control. Recommended prerequisites: mathematics, programming, machine learning, introduction to robotics.

<section id="underactuated_robotics"></section>

### 3.3.9 MIT 6.8210: Underactuated Robotics - Underactuated Robotics

[Course Homepage](https://underactuated.csail.mit.edu/Spring2024/index.html) | [Course Video](https://www.youtube.com/watch?v=v04rn86Dehg&t=4319s)

A course offered by MIT CSAIL, introducing nonlinear dynamics and control of underactuated mechanical systems. There are YouTube videos with high recording quality.

<section id="llm_robot"></section>

## 3.4 LLM for Robotics - LLM for Robotics
To enable robots to plan better, modern embodied AI works often utilize the powerful information processing and generalization capabilities of large language models for planning.
* Robotics+LLM series controlling robots through large language models [2]: [zhihu](https://zhuanlan.zhihu.com/p/668053911)<br>
* Embodied Agent wiki: [website](https://en.wikipedia.org/wiki/Embodied_agent)<br>
* Lilian Weng's personal blog - AI Agent System Overview [5]: Chinese: [website](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) English: [website](https://lilianweng.github.io/posts/2023-06-23-agent/)<br>
* A series of past works often only used LLM as a High-Level policy generator for High-Level planning
  * Classic work (1) PaLM-E: [Arxiv](https://arxiv.org/abs/2303.03378)<br>
  * Classic work (2) DO AS I CAN, NOT AS I SAY: [Arxiv](https://arxiv.org/abs/2204.01691)<br>
  * Classic work (3) Look Before You Leap: [Arxiv](https://arxiv.org/abs/2311.17842)<br>
  * Classic work (4) EmbodiedGPT: [Arxiv](https://arxiv.org/abs/2305.15021)<br>
* At the same time, some works unify High-Level policy planning with Low-Level action generation
  * Classic work (1) RT-2: [Arxiv](https://arxiv.org/abs/2307.15818)<br>
* Another representative direction combines LLM with traditional algorithm-based Planners for task and motion planning
  * Classic work (1) LLM+P: [Arxiv](https://arxiv.org/abs/2304.11477)<br>
  * Classic work (2) AutoTAMP: [Arxiv](https://arxiv.org/abs/2306.06531)<br>
  * Classic work (3) Text2Motion: [Arxiv](https://arxiv.org/abs/2303.12153)<br>
* Utilizing LLM's code capabilities to achieve embodied AI is an interesting idea
  * Classic work (1) Code as Policy: [Arxiv](https://arxiv.org/abs/2209.07753)<br>
  * Classic work (2) Instruction2Act: [Arxiv](https://arxiv.org/abs/2305.11176)<br>
* Some works combine 3D visual perception with LLM to jointly promote embodied AI planning
  * VoxPoser [Arxiv](https://arxiv.org/abs/2307.05973)<br>
  * OmniManip [Arxiv](https://arxiv.org/abs/2501.03841)<br>
* Some works try to extend LLM-based robot planning to multi-robot collaborative scenarios
  * Classic work (1) RoCo: [Arxiv](https://arxiv.org/abs/2307.04738)<br>
  * Classic work (2) Scalable-Multi-Robot: [Arxiv](https://arxiv.org/abs/2309.15943)<br>

<section id="vla"></section>

## 3.5 Vision-Language-Action Models - Vision-Language-Action Models
**Vision-Language-Action Models (VLA Models)** are models that combine VLM (Vision-Language Model) with robot control, aiming to directly use pre-trained VLM to generate robot actions (defined in RT-2). Unlike previous methods of using VLM for planning and building from scratch, VLA does not require redesigning a new architecture, tokenizes actions, and fine-tunes VLM.

**VLA Features**: End-to-end, using LLM/VLM backbone, loading pre-trained models, etc.

Current VLAs can be distinguished from the following aspects: model structure & size (e.g., action head design, tokenization methods like FAST), pre-training and fine-tuning strategies and datasets, input and output (2D vs. 3D | TraceVLA input visual trace), different application scenarios, etc.

**Reference Materials:**

* Blog: [Thoughts on Vision-Language-Action in Embodied AI](https://zhuanlan.zhihu.com/p/9880769870), [zhihu](https://www.zhihu.com/question/655570660/answer/87040917575)

* Survey:
  - A Survey on Vision-Language-Action Models: An Action Tokenization Perspective ([paper](https://arxiv.org/abs/2507.01925) | [repo](https://github.com/Psi-Robot/Awesome-VLA-Papers), 2025.07.02)
  - A Survey on Vision-Language-Action Models for Embodied AI ([paper](https://arxiv.org/abs/2405.14093), 2024.11.28)

### **3.5.1 Classic Works**:

* **Autoregressive Models**

  - **RT Series (Robotic Transformers)**:
    - **RT-1** ([paper](https://arxiv.org/abs/2212.06817))
    - **RT-2** ([page](https://robotics-transformer2.github.io/) | [paper](https://arxiv.org/abs/2307.15818), Google Deepmind, 2023.7): 55B
    - **RT-Trajectory** ([paper](https://arxiv.org/pdf/2311.01977), Google Deepmind, UCSD, Stanford 2023.11)
    - **AUTORT** ([paper](https://arxiv.org/abs/2401.12963), Google Deepmind, 2024.1)

  - **RoboFlamingo** ([paper](https://arxiv.org/abs/2311.01378) | [code](https://github.com/roboflamingo), ByteDance, Tsinghua, 2024.2)

  - **OpenVLA** ([paper](https://arxiv.org/pdf/2406.09246) | [code](https://github.com/openvla), Stanford, 2024.6): 7B

  - **TinyVLA** ([paper](https://arxiv.org/abs/2409.12514), Shanghai University, 2024.11)
  - **TraceVLA** ([paper](https://arxiv.org/pdf/2412.10345) | [code](https://github.com/umd-huang-lab/tracevla), Microsoft, 2024.12)

* **Diffusion Models for Action Head:**

  - **Octo** ([paper](https://arxiv.org/pdf/2405.12213) | [code](https://octo-models.github.io/), Stanford, Berkeley, 2024.5): Octo-base (93M)

  - **π0** ([paper](https://arxiv.org/pdf/2410.24164) | [code](https://github.com/Physical-Intelligence/openpi), Stanford, Physical Intelligence, ): 3.3B; flow-based diffusion VLA; PaliGemma (3B VLM);

  - **CogACT** ([paper](https://arxiv.org/pdf/2411.19650) | [code](https://github.com/microsoft/CogACT.git), Tsinghua, MSRA, 2024.11): 7B

  - **Diffusion-VLA** ([paper](https://arxiv.org/abs/2412.03293) | [code](https://arxiv.org/pdf/2410.07864), East China Normal University, Shanghai University, Midea, 2024.12)

* **3D Vision:**
  - **3D-VLA** ([paper](https://arxiv.org/pdf/2403.09631) | [code](https://github.com/UMass-Foundation-Model/3D-VLA/tree/main), UMass, 2024.3): 3D-based LLM
  - **SpatialVLA** ([paper](https://arxiv.org/pdf/2501.15830) | [code](https://github.com/SpatialVLA/SpatialVLA) , Shanghai AI Lab, 2025.1): Adaptive Action Grid

* **VLA-related:**

  - **FAST (π0)** ([paper](https://arxiv.org/pdf/2410.24164), [code](https://github.com/Physical-Intelligence/openpi.git), Stanford, Berkeley, Physical Intelligence, 2025.1): autoregressive VLA

  - **RLDG** ([paper](https://generalist-distillation.github.io/static/high_performance_generalist.pdf) | [code](https://arxiv.org/abs/2410.01971), Berkeley, 2024.12): Reinforcement Learning (RL) generates high-quality training data for fine-tuning

  - **BYO-VLA** ([paper](https://arxiv.org/abs/2410.01971) | [code](https://github.com/irom-princeton/byovla), Princeton University, 2024.10): Runtime image intervention, effectively reducing VLA model's sensitivity to task-irrelevant visual interference

* **Different Locomotion:**

  - **RDT-1B (Dual Arms)** ([paper](https://arxiv.org/pdf/2410.07864) | [code](https://github.com/thu-ml/RoboticsDiffusionTransformer), Tsinghua): Diffusion model for dual-arm control

  - **QUAR-VLA (Quadruped Robot)** ([paper](https://arxiv.org/pdf/2312.14457), Xihu University, Zhejiang University, 2025.2.4)

  - **CoVLA (Autonomous Driving)** ([paper](https://arxiv.org/abs/2408.10845) | [page](https://turingmotors.github.io/covla-ad/), Turing, 2024.12)

  - **Mobility-VLA (Navigation)** ([paper](https://arxiv.org/pdf/2407.07775), Google Deepmind, 2024.7)

  - **NaVILA (Legged Robot Navigation)** ([paper](https://arxiv.org/pdf/2412.04453) | [code](https://navila-bot.github.io/), USCD, 2024.12)

### **3.5.2 Hierarchical Dual-System VLA**: (Updated 2025.5) ⭐

Currently, a major paradigm of VLA is adopting a hierarchical dual-system architecture, simulating human fast reaction (System 1) and deep thinking (System 2) mechanisms. System 2 uses Vision-Language Models (VLM) for environment understanding and task planning, receiving multimodal inputs such as vision and language, and passes information to System 1 through language or latent vectors. System 1 then converts these plans into precise robot actions.
Currently, the main differences in adopting dual-system architecture are:
- *Single model vs dual model architecture*: For example, Hi-Robot adopts a VLM + VLA dual-model architecture, while pi-0.5 adopts a single-model architecture.
- *Communication method between fast and slow systems*: When the fast and slow systems are layered, communication can be through low-level commands or latent vectors.
- *Use of simulation training data*: For example, GROOT N-1 uses simulator data and synthetic data, while the pi series relies entirely on real robot data.
- In terms of *model performance*, you can focus on the following aspects: model size, action output frequency, and task difficulty (such as humanoid, long-range tasks, flexible object handling, cross-embodiment performance, etc.).

**Industry-level VLA**:

- **Figure: Helix** (link: [Figure](https://www.figure.ai/news/helix), 2025.2.20): Full upper body control for robots
- **Zhiyuan: GO-1** (link: [Zhiyuan Official](https://www.zhiyuan-robot.com/article/189/detail/56.html), 2025.3.10): ViLLA: VLM+MoE, vision-language-latent-action model
- **Physical Intelligence**: code https://github.com/Physical-Intelligence/openpi
  - **pi-0.5** ([paper](https://arxiv.org/abs/2504.16054) | blog: CSDN, 2025.4.22): After high-level task decomposition, low-level tasks are executed by a single model
  - **Hi Robot** ([paper](https://arxiv.org/abs/2502.19417) | blog: CSDN, 2025.2.26): Use VLM for high-level reasoning, VLA for low-level tasks
- **Nvidia: GROOT-N1** (code: [Nvidia Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) | [paper](https://arxiv.org/abs/2503.14734) | blog, 2025.3.27): Full-body robot control, 2B, NVIDIA-Eagle architecture and SmolLM-1.7B
- **Lingchu Intelligence: Psi-R1** ([blog](https://www.jiqizhixin.com/articles/2025-03-03-9), 2025.4.27): Hierarchical end-to-end VLA + reinforcement learning algorithm model, validating test-time scaling
- **Google DeepMind: Gemini Robotics** ([paper](https://arxiv.org/pdf/2503.20020), 2025.3.25): Gemini Robotics-ER (Embodied Reasoning Model) and Gemini Robotics main model built on Gemini 2.0, 50 Hz; **Gemini Robotics on device** ([report](https://deepmind.google/discover/blog/gemini-robotics-on-device-brings-ai-to-local-robotic-devices/), 2025.6.24) Easily deploy the model on-device


### **3.5.3 Latest VLA Works**:

- **VQ-VLA** ([paper](https://arxiv.org/pdf/2507.01016) | [code](https://github.com/xiaoxiao0406/VQ-VLA), Shanghai AI Lab, Tongji, USTC, Zhejiang University, Nanjing University, Shanghai Jiao Tong University, ICCV 25, 2025.7.1): Use VQ action tokenizer to improve VLA performance
- **WorldVLA** ([paper](https://arxiv.org/pdf/2506.21539) | [code](https://github.com/alibaba-damo-academy/WorldVLA), Alibaba DAMO Academy, Hupan Lab, Zhejiang University, 2025.6.21): Unify VLA and World Model in one framework
- **BridgeVLA** ([paper](https://arxiv.org/abs/2506.07961) | [code](https://github.com/BridgeVLA/BridgeVLA), CASIA, ByteDance Seed, UCAS, FiveAges, Nanjing University, 2025.6.7): Align 3D information in 2D space
- **TrackVLA** ([paper](https://arxiv.org/pdf/2505.23189) | [code](https://github.com/wsakobe/TrackVLA), Peking University, Galbot, Beihang University, Beijing Normal University, BAAI, 2025.5.29): Achieve real-time target detection and navigation
- **OneTwoVLA** ([paper](https://arxiv.org/pdf/2505.11917) | [code](https://github.com/Fanqi-Lin/OneTwoVLA), Tsinghua, Shanghai Qizhi, Shanghai AI Lab, Fudan, Spirit AI, 2025.5.17): Simultaneously achieve reasoning and action execution
- **MoManipVLA** ([paper](https://arxiv.org/pdf/2503.13446) | [project](https://gary3410.github.io/momanipVLA/), BUPT, NTU, Tsinghua, CVPR 25, 2025.3.17): VLA for solving mobile manipulation tasks
- **TLA** ([paper](https://arxiv.org/pdf/2503.08548) | [project](https://sites.google.com/view/tactile-language-action/), Samsung, Institute of Automation, BAAI, 2025.3.11): Introduce additional tactile modality for more precise grasping
- **PointVLA** ([paper](https://arxiv.org/pdf/2503.07511) | [project](https://pointvla.github.io/), Midea, Shanghai University, ECNU, 2025.3.10): Use point clouds to fine-tune 2D VLA to learn better spatial adaptability
- **SafeVLA** ([paper](https://arxiv.org/abs/2503.03480) | [code](https://github.com/PKU-Alignment/SafeVLA), Peking University, 2025.3.5): Solve unsafe behaviors in traditional VLA models for grasping and navigation tasks
- **HybridVLA** ([paper](https://arxiv.org/pdf/2503.10631) | [code](https://github.com/PKU-HMI-Lab/Hybrid-VLA), Peking University, 2025.3.17): Use a unified model to integrate diffusion and autoregressive action prediction, 2.7B and 7B models
- **DexVLA** ([paper](https://arxiv.org/pdf/2502.05855) | [code](https://github.com/juruobenruo/DexVLA), Midea, Southeast University, 2025.2.9): Diffusion expert 1B, using multiple action heads
- **DexGraspVLA** ([paper](https://arxiv.org/abs/2502.20900) | [code](https://github.com/Psi-Robot/DexGraspVLA), Peking University, 2025.2.28): Dexterous hand grasping VLA
- **UP-VLA** ([paper](https://arxiv.org/pdf/2501.18867), Tsinghua, 2025.2.3): Add goal-image prediction task to help action generation
- **CoT-VLA** ([paper](https://arxiv.org/pdf/2503.22020) ,  Nvidia, Stanford, CVPR2025): Integrate CoT into VLA, predict future image frames autoregressively as visual targets, 7B
- **UniAct** ([paper](https://arxiv.org/abs/2501.10105) | [code](https://github.com/2toinf/UniAct), CVPR2025, Tsinghua): Embodied foundation model based on universal action space
- **UniVLA** ([paper](https://arxiv.org/pdf/2505.06111) | [code](https://github.com/OpenDriveLab/UniVLA), HKU, Shanghai AI Lab, Zhiyuan, 2025.5.9): Use latent action models to extract task core representations from diverse data, improve generalization ability, reduce computation and data requirements


<section id="cv"></section>

## 3.6 Computer Vision - Computer Vision

CS231n (Stanford Computer Vision Course): [website](https://cs231n.stanford.edu/schedule.html), This course provides a comprehensive introduction to the application of deep learning in computer vision. Since you are already implementing algorithms from specific papers, you can skip the homework at this stage and just watch the course videos and lecture notes.<br>

<section id="2dv"></section>

### 3.6.1 2D Vision - 2D Vision
* Classic representative works in the 2D Vision field
  * CNN (Convolutional Neural Network): [link](https://easyai.tech/ai-definition/cnn/)
  * ResNet (Deep Residual Network): [bilibili](https://www.bilibili.com/video/BV1P3411y7nn)
  * ViT (The first to use Transformer in the visual field): [bilibili](https://www.bilibili.com/video/BV15P4y137jb)
  * Swin Transformer (CNN in Transformer skin): [bilibili](https://www.bilibili.com/video/BV13L4y1475U)
  * Contrastive Learning Paper Review: [bilibili](https://www.bilibili.com/video/BV19S4y1M7hm)
* Discriminative perception tasks such as recognition, classification, segmentation, detection, etc., just take a look, not much point in continuing now
* Generative models
  * Autoregressive Review: [PDF](https://arxiv.org/pdf/2411.05902)
  * Diffusion Model Review: [PDF](https://arxiv.org/pdf/2209.00796)
  * If interested in the theoretical derivation of diffusion models, check out Su Jianlin's blog - A Chat about Generative Diffusion Models (very clear derivation): [link](https://kexue.fm/archives/9119)

<section id="3dv"></section>

### 3.6.2 3D Vision - 3D Vision

* Introduction to 3D Vision - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) (Focus on course assignments) <br>
* GAMES203 - 3D Reconstruction and Understanding: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS)<br>
* Some classic papers on 3D generation:
  * Diffusion Model for 2D/3D Generation related paper classification: [link](https://zhuanlan.zhihu.com/p/617510702)
  * 3D Generation related papers - 2024: [link](https://zhuanlan.zhihu.com/p/700895749)

<section id="4dv"></section>

### 3.6.3 4D Vision - 4D Vision
* Video understanding
  * Groundbreaking work: [bilibili](https://www.bilibili.com/video/BV1mq4y1x7RU)
  * Paper Review: [bilibili](https://www.bilibili.com/video/BV1fL4y157yA)
  * Video Understanding Survey in the LLM Era: [PDF](https://arxiv.org/pdf/2312.17432)
* 4D Generation
  * Video Generation Blog (English): [link](https://lilianweng.github.io/posts/2024-04-12-diffusion-video/)
  * 4D Generation Paper List: [website](https://github.com/cwchenwang/awesome-4d-generation)

<section id="vp"></section>

### 3.6.4 Visual Prompting - Visual Prompting

Visual prompting is a method of using visual input to guide large models to complete specific tasks, commonly used in the embodied AI field. It provides example images, annotations, or visual cues to help the model understand task requirements without additional training. For example, in robot navigation and manipulation scenarios, visual prompting can help the model adapt to new environments and improve generalization ability. Compared to traditional methods, visual prompting has stronger flexibility and scalability, enabling embodied AI systems to quickly adapt to complex tasks through visual information.

- Visual Prompting Review: [paper](https://arxiv.org/abs/2409.15310)
- **PIVOT**, [page](https://pivot-prompt.github.io): By transforming tasks into iterative visual Q&A, achieve zero-shot control of robot systems and spatial reasoning without fine-tuning on specific task data.
- **Set-of-Mark Visual Prompting for GPT-4V**: [page](https://som-gpt4v.github.io)

<section id="ag"></section>

### 3.6.5 Affordance Grounding - Affordance Grounding

The goal of affordance grounding is to locate areas on objects that can interact with them from images, serving as a bridge between perception and action, an important part of embodied AI. It not only requires the model to detect and recognize objects and their local structures, but also requires the model to understand the potential interaction relationships between objects and humans or robots. For example, in robot grasping scenarios, affordance grounding helps the model find the best grasping positions on objects, thereby determining the best grasping angles. This direction integrates computer vision and multimodal large model technologies to achieve precise positioning of object interaction possibilities under weak supervision or zero-shot conditions, improving the performance of robot grasping, manipulation, and human-robot interaction tasks.

* **2D**
  - Cross-view affordance learning: **Cross-View-AG**, [paper](https://arxiv.org/pdf/2203.09905): Third-person view images provide information on how others interact with objects, helping the model learn how to interact with objects in first-person view images.
  - Single-view affordance learning: **AffordanceLLM**, [paper](https://arxiv.org/pdf/2401.06341): By utilizing the rich knowledge in pre-trained large-scale vision-language models, significantly improving the generalization ability of object affordance grounding on unseen objects and actions.
  - Dataset: **AGD20K**, [page](https://github.com/lhc1224/Cross-View-AG)

* **3D**
  - Point cloud-based affordance grounding: **OpenAD**, [paper](https://arxiv.org/pdf/2203.09905)
  - Articulated object affordance grounding: **Where2Act**, [paper](https://arxiv.org/abs/2101.02692); **VAT-Mart**, [paper](https://openreview.net/pdf?id=iEx3PiooLy)
  - Deformable object affordance grounding: **DeformableAffordance**, [paper](https://arxiv.org/pdf/2303.11057); **UniGarmentManip**, [paper](https://arxiv.org/abs/2405.06903)
  - Affordance grounding in indoor environment tasks: **SceneFun3D**, [paper](https://arxiv.org/pdf/2401.06341)
  - Point cloud dataset: **3D AffordanceNet**, [page](https://github.com/lhc1224/Cross-View-AG), focusing on object-level affordance grounding.
  - Real object dataset: **SceneFun3D**, [page](https://scenefun3d.github.io/), emphasizing applications in real indoor environments.

<section id="cg"></section>

## 3.7 Computer Graphics - Computer Graphics

If computer vision considers changes between images and from images to 3D models (3D reconstruction and generation), then computer graphics mainly studies changes between 3D models and the rendering process from 3D models to images. Embodied AI cannot do without simulators during development and testing, and simulation also belongs to the research category of graphics. Fast, high-quality rendering, parallelization, and accurate simulation have always been the goals pursued by robot simulators, and all of this is achieved through computer graphics.

* If interested in traditional graphics, check out these two courses (taught by Yan Lingqi, very well taught):<br>
  * **GAMES101 - Introduction to Modern Computer Graphics**: [website](https://games-cn.org/intro-graphics/)<br>
  * GAMES202 - High-Quality Real-Time Rendering: [website](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html)<br>
* If interested in motion synthesis/computer animation, check out:
  * GAMES105 - Fundamentals of Computer Character Animation: [website](https://games-105.github.io/)<br>
* If interested in 3D reconstruction, check out these two:
  * NeRF Principle Code Explanation: [bilibili](https://www.bilibili.com/video/BV1CC411V7oq)
  * 3DGS Principle Code Explanation: [bilibili](https://www.bilibili.com/video/BV1zi421v7Dr)
* Latest review on 3D pre-training:
  * Advances in 3D pre-training and downstream tasks: a survey: [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>
* Survey of 3D Gaussian Splatting in Robotics:
  * 3D Gaussian Splatting in Robotics: A Survey: [PDF](https://arxiv.org/pdf/2410.12262v2)<br>

<section id="mm"></section>

## 3.8 Multimodal Models - Multimodal Models

> Multimodal aims to unify representations from different modalities of information. In embodied AI, due to facing different modalities of information such as machine-recognized visual information and human natural language guidance, multimodal technology is increasingly important.
* The most classic work CLIP: [zhihu](https://zhuanlan.zhihu.com/p/493489688)<br>
* Classic work of multimodal large language models LLaVA: [website](https://llava-vl.github.io/)<br>
* Multimodal generative models review: [pdf](https://arxiv.org/pdf/2503.04641)<br>
* Multimodal large language model reinforcement learning project: VLM-R1: [repo](https://github.com/om-ai-lab/VLM-R1) From OmAI Lab's multimodal large language model DeepSeek R1-style reinforcement learning open-source project, using GRPO reinforcement learning algorithm to optimize multimodal large language models, with better results than regular SFT, a new direction for training embodied AI models.<br>

<section id="navigation"></section>

## 3.9 Robot Navigation - Robot Navigation
**Robot Navigation** is a class of tasks that require the agent to achieve path planning to reach a certain goal in **known or unknown** scenes by acquiring and processing environmental information. Robot navigation is an important capability in embodied tasks and is an indispensable basic technology for completing complex tasks. In robot navigation tasks, the agent generally receives information such as RGB, depth, GPS provided by sensors and related target instructions, and the output is a series of action instructions.

Classified by task type, robot navigation can be divided into the following parts:

- **Object-Goal Navigation**: The most common and widespread navigation task. The instruction received by the agent is a description of a specific object, and the goal is to find that object.
- **Image-Goal Navigation**: The instruction received by the agent is an image, and the goal is to find the scene described by that image.
- **Vision-Language Navigation (VLN)**: The instruction received by the agent is a natural language instruction description, and the goal is to follow that instruction to proceed.

Classified by model architecture, robot navigation can be divided into the following categories:

- **End-to-End Model**: The model directly maps sensor input to action instructions through reinforcement learning or imitation learning. The model first encodes sensor information into visual representations, combines historical actions as input, and finally learns action decision-making through interaction with the environment to obtain rewards. End-to-end models are mainly optimized for two aspects: one is to improve visual representation capabilities, and the other is to solve problems such as sparse rewards in action decision-making. The advantage of end-to-end models is that they are straightforward, but they face serious overfitting and low generalization problems, making their application in real life challenging.

    - Classic works:

        - [Learning Object Relation Graph and Tentative Policy for Visual Navigation](https://arxiv.org/abs/2007.11018)
        - [VTNet: Visual Transformer Network for Object Goal Navigation](https://openreview.net/forum?id=DILxQP08O3B)

- **Modular Model**: Sensor information is input into different modules, and modules interact through interfaces to output action instructions. Modules include mapping modules (Mapping, building semantic and occupancy maps), long-term decision modules (Global Policy, deciding long-term navigation goals), short-term decision modules (Local Policy, deciding specific operations to achieve long-term goals), etc. The mapping module is the core of the model, including grid maps, grid maps with predictions, graph representation maps, etc. The advantage of modular models is the decoupling between modules, greatly enhancing the model's interpretability. At the same time, the independent mapping module also makes the model easier to generalize to unknown environments. However, the mapping modules of modular models are still filled with manually designed rules, which to some extent also limits the model's universality.
  
    - Classic works:
      
        - [Object Goal Navigation using Goal-Oriented Semantic Exploration](https://arxiv.org/abs/2007.00643): SemExp, the earliest work to propose the concept of semantic maps, learning semantic priors of associations between regions and objects, enabling the agent to better judge the direction where the target object may be.
        - [PONI: Potential Functions for ObjectGoal Navigation with Interaction-free Learning](https://openaccess.thecvf.com/content/CVPR2022/papers/Ramakrishnan_PONI_Potential_Functions_for_ObjectGoal_Navigation_With_Interaction-Free_Learning_CVPR_2022_paper.pdf): PONI, proposed semantic map prediction based on potential functions, that is, learning to "complete" the complete map based on the existing semantic map, imagining where the object is most likely to be in the entire room, enabling the agent to transfer knowledge observed in other samples.
        - [3D-Aware Object Goal Navigation via Simultaneous Exploration and Identification](https://arxiv.org/abs/2212.00338): A classic work that encodes 3D information into navigation, through more refined point cloud segmentation information, avoiding the loss of information on the z-axis in 2D semantic maps, achieving more accurate semantic map construction.

- **Zero-shot Model**: The model does not contact training data and completes the task directly in the testing phase. Zero-shot models often utilize large-scale pre-trained models (CLIP, LLM, etc.) with knowledge priors. The proposal of zero-shot models aims to solve the overfitting and low generalization problems faced by learning-based methods, and is also more suitable for migration to real scenarios. However, the drawback of zero-shot models is that the inference speed is slower, and the performance is limited, requiring further fine-tuning to achieve better performance.

    - Classic works:

        - [CoWs on Pasture: Baselines and Benchmarks for Language-Driven Zero-Shot Object Navigation](https://arxiv.org/abs/2203.10421): The proposed work for open semantic object navigation. The idea is simple: use CLIP to find the target object, and go towards it when found. It achieves good results on uncommon objects and complex descriptions, and also has the ability to distinguish objects of the same category with different attributes.
        - [L3MVN: Leveraging Large Language Models for Visual Target Navigation](https://arxiv.org/abs/2304.05501): Use LLM to decide "which boundary I should go to". Utilize LLM's human knowledge priors to judge which room the object may be in, and the correlation with other objects, achieving faster and more effective navigation.
        - [ESC: Exploration with Soft Commonsense Constraints for Zero-shot Object Navigation](https://arxiv.org/abs/2301.13166): Explicitly proposes the impact of regions on navigation, annotates the positions occupied by regions on the semantic map, and inputs it as part of the input to LLM. Combines the advantages of semantic map continuity and LLM's rich knowledge.
        - [SG-Nav: Online 3D Scene Graph Prompting for LLM-based Zero-shot Object Navigation](https://arxiv.org/abs/2410.08189): Online construction of multi-layer scene graphs (Scene Graph) and input to LLM, using CoT to achieve LLM's reasoning about object positions.

Common Datasets:

- [MatterPort3D(MP3D)](https://niessner.github.io/Matterport/)：Real scene collection, complex and vast scenes, large data volume, high difficulty.
- [Habitat-Matterport3D(HM3D)](https://aihabitat.org/datasets/hm3d/)：Same as above
- [RoboTHOR](https://ai2thor.allenai.org/robothor/)：Simulation environment, small and simple scenes.


Other References:

- [Object Goal Navigation Survey](https://orca.cardiff.ac.uk/id/eprint/167432/1/ObjectGoalNavigationSurveyTASE.pdf)
- [awesome vision-language navigation](https://github.com/eric-ai-lab/awesome-vision-language-navigation)
- [Habitat Navigation Challenge](https://github.com/facebookresearch/habitat-challenge)(The Habitat framework integrates many common agent skills, such as semantic map construction, FBE, and some heuristic methods, very suitable for modular method development)

<section id="embodied-ai-4-x"></section>

## 3.10 Embodied AI for X

<section id="medical"></section>

### 3.10.1 EAI for Healthcare

> The rapid development of embodied AI technology is leading medical services towards a revolutionary new era. As a cutting-edge interdisciplinary field integrating AI algorithms, advanced robotics, and biomedicine, Embodied AI + Healthcare not only breaks through the boundaries of traditional medicine but also creates a new paradigm for intelligent healthcare. Its multidisciplinary collaborative innovation is reshaping the entire process of medical services, bringing unprecedented development opportunities for precision medicine, telemedicine, and personalized health management, driving the medical industry towards a more intelligent and humane direction. The breakthroughs in this field mark that medical technology is entering a new era of intelligence.
> 
* Survey on Embodied AI in Healthcare: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/abs/2501.07468)<br>

#### 3.10.1.1 MLLM for Medical
* General AI Survey for Medical Image Analysis: [website](https://arxiv.org/pdf/2306.05480)<br>
* General Segmentation Model for Medical Images - MedSAM: [website](https://www.nature.com/articles/s41467-024-44824-z.pdf)<br>
* 2024 Review: Medical AI Large Models, from General Vision to Medical Imaging: [NEJM Medical Frontier](https://mp.weixin.qq.com/s?__biz=MzIxNTc4NzU0MQ==&mid=2247550230&idx=1&sn=6baa8dcba12f3f70f4c8205a0f23b6a0&chksm=966df4ca45c8cbcaa0a5d2e42fbb4de92e6881f92981071ce7fda3bd1e13e4715f92415a9258&scene=27)<br>
* Opportunities and Challenges in the Development of Foundation Models in the Medical Field: [website](https://arxiv.org/pdf/2404.03264)<br>
* SkinGPT-4 for dermatological diagnosis: [website](https://www.nature.com/articles/s41467-024-50043-3)<br>
* PneumoLLM for pneumoconiosis diagnosis: [website](https://www.sciencedirect.com/science/article/abs/pii/S1361841524001737)<br>
* BiomedGPT: [website](https://github.com/taokz/BiomedGPT)<br>
* LLaVA-Med: [website](https://github.com/microsoft/LLaVA-Med?tab=readme-ov-file)<br>
* RoboNurse-VLA: [website](https://robonurse-vla.github.io)<br>
* PathChat Pathology Large Model from Harvard Medical School Faisal Mahmood's team. In clinical practice, pathology is called the gold standard for diagnosis: [website](https://www.nature.com/articles/s41586-024-07618-3)<br>
* DeepDR-LLM Specialized Multimodal Large Model for Diabetic Retinopathy (DR): [website](https://www.nature.com/articles/s41591-024-03139-8)<br>
* VisionFM General Ophthalmology AI Multimodal Multitask Vision Foundation Model: [website](https://ai.nejm.org/doi/full/10.1056/AIoa2300221)<br>
* Medical-CXR-VQA Large-scale Chest X-ray Dataset for Medical Visual Question Answering Tasks: [website](https://github.com/Holipori/Medical-CXR-VQA)<br>

#### 3.10.1.2 Medical Robotics
* Five Levels of Automation in Medical Robotics (Industry Consensus in Medical Robotics Field), Professor Yang Guangzhong's 2017 Paper in Science Robotics: [Medical robotics—Regulatory, ethical, and legal considerations for increasing levels of autonomy](https://www.science.org/doi/pdf/10.1126/scirobotics.aam8638)<br>
* Ten-Year Retrospective of Medical Robotics (Including Different Classifications of Medical Robots), Professor Yang Guangzhong's Review in Science Robotics: [A decade retrospective of medical robotics research from 2010 to 2020](https://www.science.org/doi/epdf/10.1126/scirobotics.abi8017)<br>
* Grading of Medical Embodied AI: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/pdf/2501.07468?)<br>
* Artificial Intelligence Meets Medical Robotics, Paper Published in Science in 2023: [website](https://www.science.org/doi/abs/10.1126/science.adj3312)<br>
* Robotic Surgery: Breakthrough from Theory to Practice (Nature Reviews Bioengineering): [Robotic surgery](https://www.nature.com/articles/s44222-025-00294-6)

* Machine Vision for Medical Robots
  * Review of 3DGS Applications in Laparoscopic Surgery: [website](https://arxiv.org/pdf/2408.04426)<br>
  * Review on Large Vision Models (LVM) in Surgical Robots by Professor Yan Hongliang's Team from The Chinese University of Hong Kong in Nature Reviews Electrical Engineering [website](https://www.nature.com/articles/s44287-025-00166-6)

* The da Vinci surgical robot is the most commonly used surgical robot, and research on autonomous skill operation for this type of robot is the most extensive
  * Introduction to da Vinci Surgical Robot Research Kit dVRK: [website](https://ieeexplore.ieee.org/abstract/document/9531355)<br>
  * Learning Surgical Operation Tasks on da Vinci Robot through Imitation Learning Surgical Robot Transformer (SRT): [website](https://surgical-robot-transformer.github.io/)<br>
  * Domain-specific Simulators - Simulators in the field of surgical robot skill learning
    * SurRoL: RL-Centered and dVRK Compatible Platform for Surgical Robot Learning [website](https://med-air.github.io/SurRoL/)<br>
    * Surgical Gym: A high-performance GPU-based platform for surgical robot learning (ICRA 2024, work in progress, based on NVIDIA Omniverse): [website](https://github.com/SamuelSchmidgall/SurgicalGym)<br>
    * ORBIT-Surgical: An Open-Simulation Framework for Learning Surgical Augmented Dexterity  (ICRA 2024, based on NVIDIA Omniverse): [website](https://orbit-surgical.github.io/)<br>
    * Suturing is a key subtask in surgical robot operation, and achieving its autonomy has been studied in many ways. For a review of autonomous suturing skill operation, refer to: [website](https://link.springer.com/article/10.1007/s00464-024-10788-w)<br>

* Continuum and soft surgical robots, as an important branch of flexible medical robots, demonstrate significant advantages in the field of minimally invasive interventional diagnosis and treatment due to their unique structural design and material properties. They can flexibly enter narrow body cavities for precise operations, while minimizing surgical incisions, reducing postoperative recovery time and infection risk for patients, providing innovative technical solutions for modern minimally invasive surgery.
  * Application of Continuum Robots in Medical Field (Nabil Simaan; Howie Choset et al.): [Continuum Robots for Medical Interventions](https://ieeexplore.ieee.org/abstract/document/9707607)<br>
  * Application of Soft Surgical Robots in Minimally Invasive Interventional Surgery (Ka-wai Kwok; Kaspar Althoefer et al.): [Soft Robot-Assisted Minimally Invasive Surgery and Interventions: Advances and Outlook](https://ieeexplore.ieee.org/abstract/document/9765966/authors#authors)<br>
  * Embodied AI for Vascular Interventional Surgical Robots (Perception, Decision-making, Skill Learning for Specific Scenarios and Tasks of Vascular Intervention): [Advancing Embodied Intelligence in Robotic-Assisted Endovascular Procedures: A Systematic Review of AI Solutions](https://arxiv.org/abs/2504.15327)
* Due to their hyper-redundant degrees of freedom and highly nonlinear structural characteristics, continuum and soft robots face significant computational complexity and modeling limitations when constructing forward and inverse kinematics equations using traditional control and sensing methods. Traditional methods are difficult to accurately describe their multi-degree-of-freedom coupled motion and dynamic response in environmental interaction. For this reason, data-driven intelligent control methods (such as deep learning, reinforcement learning, and adaptive control algorithms) have become the cutting-edge direction to solve this problem. These methods can efficiently learn the nonlinear mapping relationships of the system through large amounts of data training, significantly improving the accuracy, adaptability, and robustness of motion control, providing more reliable technical support for robot operations in complex medical scenarios.
    * What is a soft robot? Definition of embodied AI in soft robots: [Zhihu, by Ke WU from MBUZAI](https://www.zhihu.com/question/61637360/answer/92834447300?utm_psn=1870238291607040000)<br>
    * Paper by Professor Cecilia Laschi from National University of Singapore, IROS 2024 Program Chair: [Learning-Based Control Strategies for Soft Robots: Theory, Achievements, and Future Challenges](https://ieeexplore.ieee.org/abstract/document/10136428)<br>
    * Concise Guide to Physical Modeling of Embodied Intelligence in Soft Robotics (also from NUS Cecilia's team): [A concise guide to modelling the physics of embodied intelligence in soft robotics](https://inria.hal.science/hal-03921606/document)<br>
    * Application of Data-Driven Methods in Soft Robot Modeling and Control: [Data-driven methods applied to soft robot modeling and control: A review](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10477253)<br>

* Micro-nano robot technology is a class of miniature robot systems integrating multidisciplinary cutting-edge technologies such as micro-nano manufacturing, bioengineering, and intelligent control. With its unique micro-nano scale size, excellent biocompatibility, and precise manipulation performance, this cutting-edge technology brings breakthrough innovations to modern medical diagnosis and treatment paradigms. In the field of precision diagnosis, micro-nano robots can penetrate the microscopic environment of the human body to achieve real-time monitoring at the cellular and even molecular level; in the field of targeted therapy, they can serve as intelligent drug carriers to achieve precise positioning and controllable release at lesion sites; in minimally invasive surgery applications, micro-nano robot systems provide unprecedented precise operation platforms for complex surgical operations. These innovative applications not only significantly improve diagnostic and treatment efficiency, but also provide new technical approaches to conquer major diseases, promoting modern medicine towards a more precise, minimally invasive, and intelligent direction.
    * Machine Learning for Micro- and Nano-Robots (Paper by Professor Zhang Li's team from CUHK in Nature Machine Intelligence): [Machine learning for micro- and nanorobots](https://www.nature.com/articles/s42256-024-00859-x)<br>

<section id="uav"></section>

### 3.10.2 UAV - Unmanned Aerial Vehicles
The development of UAVs originates from:
1. From protecting external sensing equipment to onboard sensing and computation;
2. From remote control/pre-programmed to autonomous.

Unlike legged locomotion and manipulation, in the UAV field, data-driven methods and model-based/modular methods have different advantages in different tasks, still in a competitive stage. This is mainly because UAV models and drive modes are relatively simple (e.g., quadrotor drive mechanism has only four motors), and traditional UAVs (i.e., those without manipulation equipment) do not interact with the environment, so model-based, optimization, and hierarchical methods, through good state machine/rule design and efficient local optimization techniques, can still be endowed with strong performance. However, the difficulty of UAVs lies in their state estimation (usually required), perception, and underlying drive being full of noise, because miniaturized UAVs have very limited payload capacity and costs are kept as low as possible, so in some tasks, data-driven/end-to-end methods have shown performance far exceeding traditional methods. Therefore, the following introduction to UAV data-driven materials will intersperse comparisons with traditional methods to help everyone understand the motivation for the development of the entire field.

Overall, UAV research is divided into three parts:
1. Skill implementation/learning, such as obstacle avoidance, racing, high-maneuverability flight/acrobatics, etc.;
2. Task implementation/learning, such as exploration, reconstruction, tracking, etc.;
3. Aerial robot body design.

Open-source code for UAV work is not abundant and varies in quality, most need to be learned through papers.

### 3.10.2.1 Skill Implementation/Learning
- **Simulators Supporting RL**
  
  UAV simulators are generally not powerful, and there are almost no open-source RL sim2real projects. Based on open-source code, significant modifications are needed to achieve ideal sim2real performance.
  - **AirSim** (https://microsoft.github.io/AirSim/)：Based on UE4 engine, with relatively realistic dynamics transition simulation. Disadvantages are that UE4 underlying functions are difficult to modify and run slowly.
  - **Flightmare** (https://github.com/uzh-rpg/flightmare)：Based on Unity rendering, CPU parallel dynamics.
  - **AerialGym** (https://github.com/ntnu-arl/aerial_gym_simulator)：Based on IsaacSim, GPU parallel dynamics.

- **Representative Works on Classic Skills**

  We mainly introduce some applications of data-driven methods in classic tasks. It is worth mentioning that in the following works, some methods have emerged that break free from the dependence on SLAM systems and odometry (and the initial rise of UAVs was precisely due to the increasing maturity of SLAM/odometry systems), which will become an interesting progress direction in UAV skill learning.
  - **Obstacle Avoidance in Unknown Scenes**
    - Learning Monocular Reactive UAV Control in Cluttered Natural Environments. ICRA 2013, CMU. Inspired by autonomous driving development, the first system to use supervised learning to map images to discrete upstream control commands.
    - CAD2RL: Real Single-Image Flight without a Single Real Image. RSS 2017，UCB. The first to use sim2real RL, performing extensive domain randomization on monocular RGB images, outputting velocity commands in corridors.
    - DroNet: Learning to Fly by Driving. RAL 2018, UZH. Using automatic assumption datasets to let the aircraft output velocity commands, code open source ( https://github.com/uzh-rpg/rpg_public_dronet ).
    - Learning High-Speed Flight in the Wild. SciRob 2021, UZH. Using dagger to utilize traditional trajectory planning for supervised learning. The article claims that the low latency of network inference can enable faster flight in unknown environments. Code open source ( https://github.com/uzh-rpg/agile_autonomy ).
    - Back to Newton's Laws: Learning Vision-based Agile Flight via Differentiable Physics, Arxiv 2024, SJTU. Using first-order gradients provided by differentiable physics for policy optimization, no need for explicit position and velocity estimation. The article uses low-resolution depth maps, training obstacle avoidance more efficiently than RL, achieving high-speed flight.
    - [Flying on Point Clouds using Reinforcement Learning](https://arxiv.org/abs/2503.00496) [[Video](https://www.bilibili.com/video/BV1xeRpYnEYT)].Arxiv 2025, ZJU. Using onboard radar and sim2real RL to achieve autonomous obstacle avoidance.
    - It is worth mentioning that as the most commonly used task for UAVs, obstacle avoidance now most commonly uses traditional method systems such as the open-source ego-planner ( https://github.com/ZJU-FAST-Lab/ego-planner ), since such schemes are sufficient for most scenarios (unlike quadruped MPC), so data-driven schemes are rarely used in practical applications.

  - **Drone Racing**
    - Champion-level drone racing using deep reinforcement learning. Nature 23, UZH. Using reinforcement learning to defeat human champion pilots, the most influential article in the UAV field in recent years, the result of UZH RPG lab's deep engineering accumulation over the years, the RL scheme is relatively simple and direct.
    - Reaching the Limit in Autonomous Racing: Optimal Control versus Reinforcement Learning. SciRob 23, UZH. Comparison of reinforcement learning and optimal control methods in racing flight.
    - Demonstrating Agile Flight from Pixels without State Estimation. RSS 2024, UZH. Using vision, real-world racing demo without explicit state estimation.
    - UZH's Perception and Robotics Group (RPG) has many attempts in racing using optimal control and RL methods, enabling UAVs to achieve the fastest flight speeds on fixed tracks.

  - **High-Maneuverability/Acrobatic Flight**
    - Deep Drone Acrobatics. RSS 2020, UZH. Using imitation learning to learn MPC trajectory tracking from visual feature points, achieving acrobatic flight with drastic attitude changes.
    - [Whole-Body Control Through Narrow Gaps From Pixels to Action](https://arxiv.org/abs/2409.00895). ICRA 2025, ZJU. Using reinforcement learning to achieve end-to-end visual narrow gap traversal, no need for explicit position and velocity estimation, surpassing traditional method performance.

- **Representative Works on Classic Task Implementation**
  - **Pursuit**
    - HOLA-Drone: Hypergraphic Open-ended Learning for Zero-Shot Multi-Drone Cooperative Pursuit. Arxiv 2024, University of Manchester.
    - Multi-UAV Pursuit-Evasion with Online Planning in Unknown Environments by Deep Reinforcement Learning. Arxiv 2024, THU.
  - **Exploration**
    - Deep Reinforcement Learning-based Large-scale Robot Exploration, RAL 2024, National University of Singapore (NUS). Using attention mechanisms to learn dependencies at different spatial scales, implicitly predicting unknown areas, optimizing exploration strategies for known spaces, improving exploration efficiency.
    - ARiADNE: A Reinforcement learning approach using Attention-based Deep Networks for Exploration, ICRA 2023, National University of Singapore (NUS). Learning the interdependencies of known areas at multiple spatial scales, and implicitly predicting the potential benefits of exploring these areas. This enables the agent to arrange action sequences to balance the natural trade-off between developing/refining maps in known areas and exploring new areas.
    - DARE: Diffusion Policy for Autonomous Robot Exploration. ICRA 2025, National University of Singapore (NUS). The DARE method uses self-attention to learn map spatial information, and generates trajectories to unknown areas through diffusion, improving the exploration efficiency of autonomous robots.

### 3.10.2.2 UAV Hardware Platform Construction
Hand-building a remote-controlled racing drone is not a difficult thing, there are many hobbyist tutorials online. But building a UAV with autonomous navigation capabilities is not easy, it's a systems engineering task. Here we recommend the open-source tutorial from ZJU FAST-lab:

- [Building an Autonomous Aerial Robot from Scratch](https://www.bilibili.com/video/BV1WZ4y167me)

### 3.10.2.3 New Configuration UAV Design
In addition to conventional quadrotor UAVs used for aerial photography and environmental exploration, to make UAVs have more capabilities and apply to broader embodied AI scenarios, in addition to algorithmic innovations, it is also necessary to innovate the UAV configuration at the hardware level.

- **Aerial Manipulator**

    Aerial manipulator, also called aerial manipulation UAV, combines the fast spatial mobility of UAVs and the precise manipulation capability of robotic arms, making it an ideal carrier for embodied AI. The group of Professor Zhao Shiyu from Westlake University has a series of articles on Zhihu introducing it:

    - [Aerial Work Robots, the Next Generation of UAV Technology?](https://zhuanlan.zhihu.com/p/442331197)
    - [Aerial Work Robots—Not That Simple!](https://zhuanlan.zhihu.com/p/487203757)
    - [Aerial Manipulation Robots: How to Design the Robotic Arm?](https://zhuanlan.zhihu.com/p/509669272)
    - [What Applications Do Aerial Work Robots Have?](https://zhuanlan.zhihu.com/p/517471760)

    * Representative Works
        * [Past, Present, and Future of Aerial Robotic Manipulators](https://ieeexplore.ieee.org/document/9462539). TRO 2022. The most comprehensive review article in the aerial manipulator field so far, essential for entry-level understanding.
        * [Millimeter-Level Pick and Peg-in-Hole Task Achieved by Aerial Manipulator](https://ieeexplore.ieee.org/abstract/document/10339889). TRO 2023, BHU. Using quadrotor plus serial robotic arm to achieve millimeter-precision peg-in-hole task.
        * [NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122) [[Video](https://www.bilibili.com/video/BV16Zt5eBEPW)]. ICRA 2025, SYU. Using quadrotor plus parallel robotic arm to achieve millimeter-precision grasping.
        * [A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7) [[Video](https://www.bilibili.com/video/BV1CC4y1Z7xS)]. JIRS 2024, BHU. Using aerial manipulator for some interesting applications, such as grabbing eggs, opening doors, etc.

- **Fully-Actuated UAV**

    Common quadrotor UAVs have under-actuated characteristics, meaning position and attitude are coupled. Fully-actuated UAVs with decoupled position and attitude control are theoretically more suitable as aerial operation platforms.

    * Representative Works
        * [Fully Actuated Multirotor UAVs: A Literature Review](https://ieeexplore.ieee.org/document/8978486/?arnumber=8978486). RAM 2020. The most comprehensive review article in the fully-actuated UAV field so far, essential for entry-level understanding.
        * [Design, modeling and control of an omni-directional aerial vehicle](https://ieeexplore.ieee.org/document/7487497). ICRA 2016, ETH. The first fixed-tilt fully-actuated UAV to achieve omnidirectional flight.
        * [The Voliro omniorientational hexacopter: An agile and maneuverable tiltable-rotor aerial vehicle](https://ieeexplore.ieee.org/document/8485627). RAM 2018, ETH. The first tiltable-rotor fully-actuated UAV to achieve omnidirectional flight 
        * [FLOAT Drone: A Fully-actuated Coaxial Aerial Robot for Close-Proximity Operations](https://arxiv.org/abs/2503.00785) [[Website](https://zju-jxlin.github.io/float-drone.github.io/)]. Arxiv 2025, ZJU. Small-sized fully-actuated UAV suitable for close-proximity operations.

- **Deformable UAV**

    In addition to installing robotic arms on the flight platform, making the UAV body deformable is also a method to enable more functions.

    * Representative Works
        * [Design, Modeling, and Control of an Aerial Robot DRAGON: A Dual-Rotor-Embedded Multilink Robot With the Ability of Multi-Degree-of-Freedom Aerial Transformation](https://ieeexplore.ieee.org/document/8258850). RAL 2018，东京大学. Best paper award on UAV in ICRA 2018, multi-joint deformable UAV.
        * [The Foldable Drone: A Morphing Quadrotor That Can Squeeze and Fly](https://ieeexplore.ieee.org/document/8567932?arnumber=8567932). RAL 2019, Uzh. A servo is installed on each arm of the quadrotor to achieve body deformation flight.
        * [Ring-Rotor: A Novel Retractable Ring-Shaped Quadrotor With Aerial Grasping and Transportation Capability](https://ieeexplore.ieee.org/document/10044964) [[Video](https://www.bilibili.com/video/BV1gY4y1K723)]. RAL 2023, ZJU. A deformable ring-shaped quadrotor, usable for grasping, transportation, and other tasks.
        * [Design and Control of a Passively Morphing Quadcopter](https://ieeexplore.ieee.org/document/8794373) [[Video](https://www.youtube.com/watch?v=MSvoQT__c9U)]. ICRA 2019, UCB. A passively morphing quadrotor UAV.

- **Multi-Modal UAV**

    Compared to ground robots, UAVs have the advantage of 3D spatial mobility, but the disadvantage of poor endurance. Therefore, some research focuses on the configuration design, motion control, and autonomous navigation of multi-modal UAVs. Multi-modal UAVs have motion capabilities in air, ground, underwater, and other domains. This not only solves the endurance problem of UAVs but also allows UAVs to have more application potential.

    * Representative Works
        * [A bipedal walking robot that can fly, slackline, and skateboard](https://www.science.org/doi/10.1126/scirobotics.abf8136). SR 2021, Caltech. Multi-modal air-ground legged robot.
        * [Multi-Modal Mobility Morphobot (M4) with appendage repurposing for locomotion plasticity enhancement](https://www.nature.com/articles/s41467-023-39018-y). NC 2023, Northeastern University. Multi-modal UAV with many motion modes.
        * [Skater: A Novel Bi-Modal Bi-Copter Robot for Adaptive Locomotion in Air and Diverse Terrain](https://ieeexplore.ieee.org/document/10538378) [[Video](https://www.bilibili.com/video/BV1y2421M7HM)]. RAL 2024, ZJU. Multi-modal air-ground dual-rotor UAV adapted to diverse terrains.
        * [Autonomous and Adaptive Navigation for Terrestrial-Aerial Bimodal Vehicles](https://ieeexplore.ieee.org/document/9691888). RAL 2022, ZJU. Achieving autonomous navigation for air-ground multi-modal UAVs.


<section id="ad"></section>

### 3.10.3 Autonomous Driving - Autonomous Driving

[Heart of Autonomous Driving](https://www.zdjszx.com/) (also has a WeChat public account)

Autonomous driving is called the "smallest embodied AI verification scenario" because within the embodied AI framework, it has a complete perception, decision-making, and action closed loop, but with clear task objectives, simple physical interaction, and relatively low scene complexity. As a technology verification scenario, autonomous driving not only embodies the core characteristics of embodied AI but also provides technical accumulation and theoretical support for more complex embodied AI tasks.

#### Model: Autonomous Driving Simulation

[Generative Simulation Unleashes Infinite Inspiration for Embodied AI](https://bydrug.pharmcube.com/news/detail/80b67b2227879864af934e5f81835776)

Autonomous driving simulation is an indispensable part of autonomous driving technology development. By providing a safe, efficient, and controllable testing environment, it not only reduces R&D costs and risks but also accelerates technology iteration and large-scale deployment. At the same time, simulation can cover a large number of scenarios that are difficult to reproduce in reality, providing important guarantees for the safety, reliability, and generalization ability of autonomous driving systems.

1. 3D/4D Scene Reconstruction

* Classic Works: NSG, MARS, StreetGaussians, OmniRe
  * **NSG**: CVPR 2021, [github](https://github.com/princeton-computational-imaging/neural-scene-graphs), [arxiv](https://arxiv.org/abs/2011.10379), [paper](https://openaccess.thecvf.com/content/CVPR2021/html/Ost_Neural_Scene_Graphs_for_Dynamic_Scenes_CVPR_2021_paper.html)
  * **MARS**: [github](https://open-air-sun.github.io/mars/), [arxiv](https://arxiv.org/abs/2307.15058)
  * **StreetGaussians**: [github](https://github.com/zju3dv/street_gaussians), [arxiv](https://arxiv.org/abs/2401.01339)
  * **OmniRe**: ICLR 2025 Spotlight, [demo page](https://ziyc.github.io/omnire), [github](https://github.com/ziyc/drivestudio), [arxiv](https://arxiv.org/abs/2408.16760)

2. Controllable Scene Generation (World Model)

* Classic Works: GAIA-1, GenAD (OpenDV Dataset), Vista, SCP-Diff, MagicDrive -> MagicDriveDiT, UniScene, VaVAM
  * **GAIA-1**: [demo page](https://wayve.ai/thinking/introducing-gaia1/), [arxiv](https://arxiv.org/abs/2309.17080)
  * **GenAD**: CVPR 2024 Highlight, OpenDV Dataset, [github](https://github.com/OpenDriveLab/DriveAGI?tab=readme-ov-file#opendv), [arxiv](https://arxiv.org/abs/2403.09630)
  * **Vista**: NeurIPS 2025, [demo page](https://opendrivelab.com/Vista), [github](https://github.com/OpenDriveLab/Vista), [arxiv](https://arxiv.org/abs/2405.17398)
  * **SCP-Diff**: [demo page](https://air-discover.github.io/SCP-Diff/), [github](https://github.com/AIR-DISCOVER/SCP-Diff-Toolkit), [arxiv](https://arxiv.org/abs/2403.09638)
  * **MagicDrive** -> MagicDriveDiT: [demo page](https://gaoruiyuan.com/magicdrive-v2/), [arxiv](https://arxiv.org/abs/2411.13807)
  * **UniScene**: CVPR 2025, [demo page](https://arlo0o.github.io/uniscene/),  [arxiv](https://arxiv.org/abs/2412.05435)
  * **VaVAM**: [github](https://github.com/valeoai/VideoActionModel)


#### Policy: Autonomous Driving Policy

1. From Modular to End-to-End

* In the classic modular pipeline, each model acts as an independent component responsible for the corresponding specific task (3D object detection and tracking & BEV mapping -> object motion prediction -> trajectory planning), this design has gradually been replaced by end-to-end models.

[End-to-end Autonomous Driving: Challenges and Frontiers](https://arxiv.org/pdf/2306.16927)

2. Parallel Fast and Slow Systems

[Ideal End-to-End - VLM Dual System](https://www.sohu.com/a/801987742_258768)

* Fast System Classic Papers: UniAD (CVPR 2023 Best Paper), VAD, SparseDrive, DiffusionDrive
  * **UniAD**: CVPR 2023 Best Paper, [github](https://github.com/OpenDriveLab/UniAD), [arxiv](https://arxiv.org/abs/2212.10156)
  * **VAD**: ICCV 2023, [github](https://github.com/hustvl/VAD), [arxiv](https://arxiv.org/abs/2303.12077)
  * **SparseDrive**: [github](https://github.com/swc-17/SparseDrive), [arxiv](https://arxiv.org/abs/2405.19620)
  * **DiffusionDrive**: CVPR 2025, [github](https://github.com/hustvl/DiffusionDrive), [arxiv](https://arxiv.org/abs/2411.15139)
  * Fast System Scale Up Feature Exploration: https://arxiv.org/pdf/2412.02689
* Slow System Classic Papers: DriveVLM, EMMA
  * **DriveVLM**: CoRL 2024, [arxiv](https://arxiv.org/abs/2402.12289)
  * **EMMA**: [arxiv](https://arxiv.org/abs/2410.23262)
    - **[Open-EMMA](https://github.com/taco-group/OpenEMMA)** is an open-source implementation of EMMA, providing an end-to-end framework for autonomous vehicle motion planning.


#### Future Development Directions

[AIR ApolloFM Technology Full Interpretation](https://air.tsinghua.edu.cn/info/1007/2258.htm)

<section id="control"></section>

## 4. Control Theory and Robotics Fundamentals
**Classic Courses**
  - [video](https://www.bilibili.com/video/BV1GJ411k7fE) Northwestern University Modern Robotics: This course focuses on basic robotics theory, involving concepts such as **Cartesian coordinate system**, **joint coordinate system**, **degrees of freedom**, **homogeneous rotation matrices**, **forward kinematics (FK)**, **inverse kinematics (IK)**, etc., suitable for beginners with zero foundation.
  - [video](https://www.bilibili.com/video/BV1h7411A7B9) UC Berkeley Advanced Robotics by Pieter Abbeel: This course is an advanced robotics course, suitable for further study after learning 'Modern Robotics' or having relevant foundation. The parts involved include **Markov decision processes**, **LQR control**, **optimization problems under constraints**, **optimization-based control**, **motion planning**, **Kalman filtering**, **imitation learning**, **reinforcement learning**, **Sim2Real**, etc. The course also includes many practical demonstrations, which help to further understand the application of theory in the real world.
## 4.1. Control Theory Fundamentals

### 4.1.1 Classic Control Principles
* Understand systems, feedback
* Time domain and frequency domain analysis
* Transfer function
* Understand feedforward control, feedback control
* **PID Control**: [CSDN](https://blog.csdn.net/name_longming/article/details/115093338) [BiliBili](https://www.bilibili.com/video/BV1B54y1V7hp)

### 4.1.2 Modern Control Theory (Linear Systems Control)
* Modern Control Systems (14th edition), Robert. H. Bishop, Richard. C, Dorf. z: [Book](http://103.203.175.90:81/fdScript/RootOfEBooks/E%20Book%20collection%20-%202024/EEE/Modern_control_systems_Robert_H_Bishop_Richard_C_Dorf_z_lib_org.pdf#page=1.00&gsr=0)
* State equations
* State feedback and optimal control
* **LQR Control** [BiliBili](https://www.bilibili.com/video/BV1Ng4y1V7JQ)
* **CMU 16-745 Optimal Control** covers from numerical optimization to optimization theory, [Website](https://optimalcontrol.ri.cmu.edu/), [Youtube](https://www.youtube.com/playlist?list=PLZnJoM76RM6IAJfMXd1PgGNXn3dxhkVgI), [Bilibili](https://space.bilibili.com/504273533/lists/6271656?type=season)

### 4.1.3 Advanced Control Techniques
* Robust control
* Thoroughly understand impedance control, admittance control, hybrid force-position control: [CSDN](https://blog.csdn.net/a735148617/article/details/108564836)
* **Model Predictive Control MPC**
* Intelligent control (including deep learning-based control)

## 4.2. Introduction to Robotics

### 4.2.1 Recommended Materials
* Modern Robotics (highly recommended!) [video](https://www.youtube.com/watch?v=29LhXWjn7Pc&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx&index=11)
* Classic Textbooks
  * "Geometric Foundations of Mechanism and Robotics with Screw Algebra" by Academician Dai Jiansen
  * "Modern Robotics: Mechanics, Planning, and Control" by Kevin M. Lynch, Frank C. Park
  * "Modern Mathematical Theory Foundations of Robotics" by Ding Xilun

### 4.2.2 Robotics Kinematics (Kinematics) and Dynamics (Dynamics)
1. Robotics Kinematics
> For students who want to quickly understand what IK FK is, you can watch this 7-minute short video to establish a rough understanding: [BiliBili](https://www.bilibili.com/video/BV18E411v7F9)<br>
> For a relatively simple review of the principles of IK and FK, you can watch this: [CSDN](https://blog.csdn.net/Dwzsa/article/details/142386529?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&utm_relevant_index=6) 

* IK (Inverse Kinematics)
  * More detailed video courses
    * [BiliBili IK(1)](https://www.bilibili.com/video/BV1PD4y1t7xP)
    * [BiliBili IK(2)](https://www.bilibili.com/video/BV1Tt4y1T79Z)
  * Text teaching
    * [Book](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html), more detailed IK theory

* FK (Forward Kinematics)
  * More detailed video courses
    * [BiliBili FK(1)](https://www.bilibili.com/video/BV1Ve4y127Uf)
    * [BiliBili FK(2)](https://www.bilibili.com/video/BV1a14y157uL)

2. Robotics Dynamics (**Important!!!**)
* Understand skew-symmetric matrices, Twist and Exponential of a twist, screw algebra

### 4.2.3 Odometry and Simultaneous Localization and Mapping (Odometry&SLAM)
Odometry is used to provide real-time positioning for robots. Odometry is often implemented based on Extended Kalman Filter (EKF), fusing multiple observations from various sensors commonly used for robot pose perception, such as Inertial Measurement Unit (IMU), camera, LiDAR, encoder, millimeter-wave radar, Ultra-Wideband (UWB), optical flow sensor, etc., to achieve robot pose estimation at high frequency.

The most common odometries are Visual-Inertial Odometry (VIO) and LiDAR-Inertial Odometry (LIO), as well as some recently emerging methods using 4D millimeter-wave radar as the main sensor. Classic works include the VINS series [VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono), [ORB-SLAM](https://github.com/UZ-SLAMLab/ORB_SLAM3), [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion), [LOAM](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf), [FAST-LIO](https://github.com/hku-mars/FAST_LIO), etc. In addition, there are odometries that fuse IMU, camera, and LiDAR sensors, such as the [FAST-LIVO](https://github.com/hku-mars/FAST-LIVO2) series.

SLAM (Simultaneous Localization And Mapping) completes map construction while positioning, making Loop Closure detection possible. The existence of loop closure detection allows correcting part of the accumulated error when the robot revisits a location, improving positioning accuracy during long-term operations. SLAM implementations mainly include filter-based and optimization-based, generally divided into front-end and back-end in implementation, and SLAM based on different sensors has their own characteristics. Here are some learning resources, mainly books:

* [SLAM Handbook](https://github.com/SLAM-Handbook-contributors/slam-handbook-public-release)
* [Past, Present, and Future of Simultaneous Localization And Mapping: Towards the Robust-Perception Age](https://arxiv.org/abs/1606.05830): Classic review in the SLAM field
* Gao Xiang's ["Visual SLAM Fourteen Lectures"](https://github.com/gaoxiang12/slambook2)
* Gao Xiang's ["SLAM Technology for Autonomous Driving and Robotics"](https://github.com/gaoxiang12/slam_in_autonomous_driving)

In addition, SLAM also has end-to-end implementations [DROID-SLAM](https://arxiv.org/abs/2108.10869).

Other thoughts on SLAM can refer to [awesome-and-novel-works-in-slam](https://github.com/runjtu/awesome-and-novel-works-in-slam)

### 4.2.4 Misc

* ROS Basics:
  * Embodied AI ROS1 Basics: [website](http://www.autolabor.com.cn/book/ROSTutorials/)
  * Embodied AI ROS2 Basics: [website](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)
  * ROS2 Humble 3-Hour Beginner Tutorial: [ROS2 Humble Crash Course from Open Robotics Discourse](https://discourse.openrobotics.org/t/ros2-humble-3h-tutorial-for-beginners/28500/)
  * Open Robotics Official Website: [Open Robotics](https://openrobotics.org/) is the organization behind open-source robotics software platforms such as ROS, Gazebo, and Open-RMF. The official website provides official entry points, documentation, and community updates for ROS / Gazebo / Open-RMF, suitable as the general entry for the ROS ecosystem.

* Commonly Used Libraries
  * cuRobo: [cuRobo](https://curobo.org/), cuRobo is Nvidia's CUDA-accelerated robotics library, providing a set of efficient robotics algorithms, mainly significantly improving performance through parallel computing, including but not limited to IK, collision detection, path planning, etc.
  * IKFast: [IKFast](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html), classic IK library.
  * mplib: [mplib](https://github.com/haosulab/mplib), IK library for ManiSkill Benchmark and Sapien simulation platform.
* ROS Multi-Sensor Timestamp Synchronization: [website](https://blog.csdn.net/qq_43495930/article/details/125649446)
* Hands-on Practice with LeRobot SO-100: [website](https://huggingface.co/lerobot)


<section id="hardware"></section>

# 5. Hardware

> The hardware aspect of embodied AI covers multiple technology stacks, such as embedded software and hardware design, mechanical design, robot system design. This part of the knowledge is quite complex, suitable for those who want to focus on this direction.
> For learning the hardware part, it's best to start from practice!

<section id="embedded"></section>

## 5.1 Embedded
* Embedded Learning Roadmap: [CSDN](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452)
* 51 Microcontroller: [BiliBili](https://www.bilibili.com/video/BV1Mb411e7re), Classic from Jiangke University Automation
* Stm32 Microcontroller: [BiliBili](https://www.bilibili.com/video/BV1th411z7sn), Classic from Jiangke University Automation
* Stm32 Motor Drive: [BiliBili](https://www.bilibili.com/video/BV1AZ4y1V7wt), Wildfire
* Wildfire Stm32 Standard Library: [BiliBili](https://www.bilibili.com/video/BV1yW411Y7Gw), Wildfire
* Punctual Atom Stm32: [BiliBili](https://www.bilibili.com/video/BV1Lx411Z7Qa), Punctual Atom
* 韦东山嵌入式Linux：[BiliBili](https://www.bilibili.com/video/BV1w4411B7a4), 韦东山

<section id="mechanical"></section>

## 5.2 Mechanical Design
* SolidWorks Teaching: [BiliBili](https://www.bilibili.com/video/BV1iw411Z7HZ)
* URDF Generation: [CSDN](https://blog.csdn.net/weixin_45168199/article/details/105755388), Guide on how to generate robot URDF files from SolidWorks assemblies.
  
<section id="robosystem"></section>

## 5.3 Robot System Design

* "Introduction to Robotics", high-quality textbook from [2]: [PDF](./files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf)
* "Robotics Systems Textbook": [website](https://motion.cs.illinois.edu/RoboticSystems/)


<section id="sensors"></section>

## 5.4 Sensors
### 5.4.1 Depth Camera

RealSense, [RealSense ROS Development Kit](https://github.com/IntelRealSense/realsense-ros/tree/ros1-legacy)

<section id="tactile"></section>

## 5.5 Tactile Sensing

### 1. Vision-Based Tactile Sensors

Vision-based tactile sensors capture tactile information through cameras, mapping the deformation of the touch surface to visual data to estimate contact force, deformation, etc. Their design involves **sensor shape** (affecting contact range and adaptability), **marker point setup** (tracking surface deformation, improving resolution), **material selection** (such as silicone or elastomer, improving sensitivity), and **lighting and camera system** (enhancing visual signal quality).

* **Advantages**: Provide high-resolution tactile information, non-invasive perception, do not affect object surface properties, and can be integrated with visual systems to improve multimodal perception capabilities.
* **Disadvantages**: High computational load, dependent on visual processing and machine learning; susceptible to ambient light; complex optical design, limited encapsulation and durability.

 **Reference Literature Review**: Very detailed, respectively algorithm and structural design
- Algorithm: *[When Vision Meets Touch: A Contemporary Review for Visuotactile Sensors From the Signal Processing Perspective](https://ieeexplore.ieee.org/document/10563188)*
- Structure: *[On the Design and Development of Vision-Based Tactile Sensors](https://link.springer.com/article/10.1007/s10846-021-01431-0)*

### 2. Electronic Skin

The main paths for tactile perception are these two categories. Electronic skin simulates the tactile capabilities of human skin, usually using flexible electronic materials (such as pressure sensing films, nano-sensor networks, etc.) to perceive external pressure, temperature, and deformation, enabling robots to have tactile perception closer to biological.

* **Advantages**: Electronic skin can **cover large areas** of the robot surface, achieving whole-body tactile perception; has **high sensitivity**, capable of detecting minute force changes for precise feedback; at the same time, **stretchability** allows it to adapt to complex surfaces, improving durability.
* **Disadvantages**: Electronic skin has **complex manufacturing**, high material and process requirements, higher cost; **data processing challenges**, large-scale tactile data requires efficient computing and storage solutions; in addition, **stability issues** may lead to decreased sensitivity after long-term use, affecting reliability.

 **Reference Literature Review**: *[Toward an AI Era: Advances in Electronic Skins](https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00049)*

### 3. Applications and Algorithms for Tactile Perception (Visuotactile)

* 3.1 Pose Estimation
  * Estimate in-hand object pose
    * *[3D Shape Perception from Monocular Vision, Touch, and Shape Priors](https://arxiv.org/abs/1808.03247)*
  * In scene
    * *[Fast Model-Based Contact Patch and Pose Estimation for Highly Deformable Dense-Geometry Tactile Sensors](https://ieeexplore.ieee.org/document/8936859)*

* 3.2 Object Classification
  * Distinguish different liquids, materials, or transparent objects.
    * *[Understanding Dynamic Tactile Sensing for Liquid Property Estimation](https://arxiv.org/abs/2205.08771)*
    * *[Multimode Fusion Perception for Transparent Glass Recognition](https://www.semanticscholar.org/paper/Multimode-fusion-perception-for-transparent-glass-Zhang-Shan/90109f2eabba717d152a599fc8d8d5a3677c85e5)*

* 3.3 Tactile Manipulation
  * Object assembly
    * *[Active Extrinsic Contact Sensing: Application to General Peg-in-Hole Insertion](https://ieeexplore.ieee.org/abstract/document/9812017)*
    * *[Building a Library of Tactile Skills Based on Fingervision](https://ieeexplore.ieee.org/abstract/document/9035000)*
  * Cable organization
    * *[Cable Manipulation with a Tactile-Reactive Gripper](https://arxiv.org/abs/1910.02860)*
  * Fine hand operations
    * *[Manipulation by Feel: Touch-Based Control with Deep Predictive Models](https://arxiv.org/abs/1903.04128)*
    * *[NeuralFeels with Neural Fields: Visuotactile Perception for In-Hand Manipulation](https://www.science.org/doi/10.1126/scirobotics.adl0628)*

* 3.4 Large Tactile Models
  * To unify multimodal tactile representation, improve universality.
    * *[Binding Touch to Everything: Learning Unified Multimodal Tactile Representations](https://openaccess.thecvf.com/content/CVPR2024/papers/Yang_Binding_Touch_to_Everything_Learning_Unified_Multimodal_Tactile_Representations_CVPR_2024_paper.pdf)*

### 4. Sensor Purchase

There are some mature vision-based tactile sensors available on the market 🔗 **[GelSight Official Website](https://gelsight.com/)**

<section id="companies"></section>

## 5.6 Companies

| Company | Main Products | Others |
|-------|------|------|
| [AgileX](https://www.agilex.ai/) | [Piper 6-axis robotic arm](https://www.agilex.ai/chassis/16)<br> [PIKA data collection solution](https://www.agilex.ai/chassis/22)<br>[Cobot Magic dual-arm teleoperation platform](https://www.agilex.ai/chassis/27)<br>Mobile chassis| Oriented towards education and research
| [Unitree](https://www.unitree.com/cn) | [Quadruped robot development guide](https://www.yuque.com/ironfatty/nly1un/luo9gb)<br>[Go2 robot dog](https://www.unitree.com/cn/go2)<br>[AlienGo robot dog](https://www.yuque.com/ironfatty/nly1un/dqcz3u)<br>[General humanoid H1](https://www.unitree.com/cn/h1)<br>[General humanoid G1](https://www.unitree.com/cn/g1)<br> | Many outputs use Unitree's robots as hardware foundation
| [ARX](https://www.arx-x.com/?product/) | [X5 robotic arm](https://www.arx-x.com/?product/21.html)<br>[X7 dual-arm platform](https://www.arx-x.com/?product/23.html)<br>[R5 robotic arm](https://www.arx-x.com/?product/22.html)  | Suitable for reproducing many classic works, e.g. [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin AgileX chassis + ARX arm](https://github.com/TianxingChen/RoboTwi)
| [Boston Dynamics](https://bostondynamics.com/)  | [Spot robot dog](https://bostondynamics.com/products/spot/)<br>[Atlas general humanoid](https://bostondynamics.com/atlas/)  | Embodied AI body manufacturer, transitioning from hydraulic drive to motor drive |
| [Linkerbot](https://www.linkerbot.cn/index) | [Linker Hand L30 (tendon-driven)](https://www.linkerbot.cn/product?page=L30)<br>[Linker Hand L20 (linkage-driven)](https://www.linkerbot.cn/product?page=L20) | Specializing in various dexterous hands |
| [DexRobot](https://www.dex-robot.com/)| [Dexhand 021 dexterous hand](https://www.dex-robot.com/productionDexhand) | 19-DOF mass-produced dexterous hand |
| [Galbot](https://www.galbot.com/about) | [GALBOT G1](https://www.galbot.com/g1) | Focused on embodied AI multimodal large model general robot R&D |
| [Galaxea](https://galaxea.ai/) | [A1 6-axis robotic arm](https://galaxea.ai/A1)<br>[R1-Pro humanoid robot](https://galaxea.ai/R1-Pro) | Both software and hardware products are independently developed, focused on creating 'one brain, multiple forms' |
| [World Labs](https://www.worldlabs.ai/) | | Focused on spatial intelligence, committed to building large world models (LWM) to perceive, generate, and interact with the 3D world. [Related Introduction](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [Robotera](https://www.robotera.com) | [Star1 humanoid](https://www.robotera.com/goods/1.html)<br> [XHAND1 dexterous hand](https://www.robotera.com/goods/2.html) | |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1 Humanoid](https://boosterobotics.com/zh/store/)|  |
| [人形机器人（上海）有限公司](https://www.openloong.net/) | [Qinglong Robot](https://www.openloong.org.cn/cn) | Full-size general humanoid robot, providing open-source hardware design drawings, software framework code, algorithm packages, and full-chain simulation tools. |
| [云深处科技](https://www.deeprobotics.cn/) |  [Jueying X30 Quadruped Robot](https://www.deeprobotics.cn/robot/index/product3.html)<br> [Dr.01 Humanoid Robot](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | Embodied AI simulation platform provider |
| [光轮智能](https://lightwheel.net/) |  | Embodied AI data platform |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [Expedition A2 Humanoid Robot](https://www.zhiyuan-robot.com/products/A2)<br>[Expedition A2-W Wheeled Humanoid](https://www.zhiyuan-robot.com/products/A2_W)<br>[Lingxi X1 Humanoid Robot](https://www.zhiyuan-robot.com/products/X1)<br>[Jingling G1 Wheeled Humanoid](https://www.zhiyuan-robot.com/products/A2_D)|  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | Embodied AI infrastructure company |
| [求之科技](https://airbots.online/)  | [TOK2 Mobile Master-Slave Arm Platform](https://airbots.online/zh/tok)<br>[MMK2 Mobile Lifting Dual-Arm Platform](https://airbots.online/zh/mmk2)<br> Play 6-Axis Robotic Arm|  |
| [穹彻智能](https://www.noematrix.ai/) | | |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) | | |
| [具身风暴](https://www.robotstorm.tech) | | Implementing embodied AI general massage robot |
| [众擎机器人](https://engineai.com.cn/) |[SE 01](https://engineai.com.cn/product_one)<br>[PM 01](https://engineai.com.cn/product_fore)| |
| [魔法原子](https://www.magiclab.top/) |[MagicBot](https://www.magiclab.top/human)<br>[MagicDog](https://www.magiclab.top/dog)| |
| [帕西尼](https://www.paxini.com/) |[PX-6AX GEN2 Tactile Sensor](https://www.paxini.com/ax/gen2)<br>[DexH13 GEN2 Dexterous Hand](https://www.paxini.com/dex/gen2)<br>[TORA-ONE Humanoid Robot](https://www.paxini.com/robot) | |
<section id="software"></section>

# 6. Software

<section id="simulators"></section>

## 6.1 Simulators
Common simulators wiki: [wiki](https://simulately.wiki/)
| Simulator | Corresponding Benchmarks |
|-------|------|
| [IsaacGym](https://developer.nvidia.com/isaac-gym) | [legged gym](https://github.com/leggedrobotics/legged_gym)<br>[parkour (including distillation and real machine deployment)](https://github.com/ZiwenZhuang/parkour)<br>[extreme-parkour](https://github.com/chengxuxin/extreme-parkour) |
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K (cross-platform)](https://behavior.stanford.edu/behavior-1k)+[omniGibson (toolchain)](https://behavior.stanford.edu/omnigibson/)<br>[ARNOLD](https://arnold-benchmark.github.io/) <br> [GarmentLab](https://garmentlab.github.io/) and [DexGarmentLab](https://wayrise.github.io/DexGarmentLab/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html)+[robomimic (toolchain)](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics (Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](https://github.com/robocasa/robocasa?tab=readme-ov-file)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| [Genesis](https://genesis-embodied-ai.github.io/) ||
| [SOFA](https://github.com/sofa-framework/sofa/)| Commonly used for soft robot simulation |
| [GenieSim](https://github.com/AgibotTech/genie_sim)| [A simulation and benchmark framework from AgiBot.](http://agibot-world.com/sim-evaluation/docs) |
| [Gazebo](https://gazebosim.org) | General robot simulation platform, maintained by [Open Robotics](https://openrobotics.org/), deeply integrated with ROS / ROS 2, suitable for simulation of mobile robots, warehousing and logistics, etc. |

**Tutorials**:
- **Isaac 101:** [Blog](https://axi404.top/tags/isaac%20101) by Axi404.

<section id="benchmarks"></section>

## 6.2 Benchmarks
Summary of commonly used benchmarks in embodied AI [1]: [zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
* **CALVIN**, [github](https://github.com/mees/calvin), [website](http://calvin.cs.uni-freiburg.de/) 2022, the first publicly available benchmark that combines natural language control, high-dimensional multimodal input, 7-DOF robotic arm control, and long-horizon robotic manipulation. Supports different language instructions, different camera inputs, different control methods, mainly used to evaluate the multimodal input capabilities and long-term planning capabilities of embodied AI models.
* **Meta-World**, [webpage](https://meta-world.github.io/): Evaluates robot performance in multi-task and meta reinforcement learning scenarios. 50 robot manipulation tasks (such as grasping, pushing objects, opening doors, etc.), organized into different benchmark sets (such as ML1, ML10, ML45, MT10, MT50, etc.), each set has clear training tasks and test tasks. Comprehensive surroundings and documentation, based on MuJoCo, with complete API and tools, can run with python import.
* **Embodied Agent Interface: Benchmarking LLMs for Embodied Decision Making**, [website](https://embodied-agent-interface.github.io/): Mainly evaluates the performance of large language models (LLMs) in embodied decision making, focusing on the decision process, including goal interpretation, sub-goal decomposition, action serialization, and state transition modeling, without involving specific execution.
* **RoboGen**, [repo](https://github.com/Genesis-Embodied-AI/RoboGen), [website](https://robogen-ai.github.io/): Does not generate policy, but generates tasks, scenes, and labeled data, which can be directly used for supervised learning.
* **LIBERO**, [repo](https://github.com/Lifelong-Robot-Learning/LIBERO), [website](https://libero-project.github.io/intro.html): Uses a programmatic generation pipeline to generate tasks, this pipeline can theoretically generate an unlimited number of manipulation tasks, and provides: three visual motion strategy network architectures (RNN, Transformer, and ViLT) and three lifelong learning algorithms, as well as benchmarks for sequential fine-tuning and multi-task learning.
* **RoboTwin**, [repo](https://github.com/TianxingChen/RoboTwin): Uses programmatic generation of infinite dual-arm robot manipulation task data, and provides evaluation benchmarks for all tasks.

<section id="datasets"></section>

## 6.3 Datasets
* **Open X-Embodiment: Robotic Learning Datasets and RT-X Models**, [website](https://robotics-transformer-x.github.io/): Over 1 million real robot trajectory data from 22 different robot platforms, covering 527 different skills and 160,266 tasks, mainly focusing on grasping and placing.
* **AgiBot World Datasets (智元机器人)**, [website](https://agibot-world.com/): Over 80 kinds of diversified skills in daily life, over 1 million trajectory data, collected from **homogeneous robots**, multi-level quality control and full human-in-the-loop strategy, from professional training of collectors, to strict management during collection, to data screening, review, and annotation, every link has been carefully designed and strictly controlled.
* **RoboMIND**, [website](https://x-humanoid-robomind.github.io/): Contains 107,000 real-world demonstration trajectories involving 96 unique object categories in 479 different tasks, from four different collaborative arms, tasks divided into five major categories: basic skills, precise operations, scene understanding, cabinet operations, and collaborative tasks.
* **All Robots in One,** [website](https://imaei.github.io/project_pages/ario/): ARIO dataset, containing perception data of **5 modalities: 2D, 3D, text, tactile, sound**, covering **manipulation** and **navigation** two major task categories, with both **simulation data** and **real scene data**, and including various robot hardware, with high richness. While reaching a data scale of three million, it also ensures unified data format, and is currently the open-source dataset in the embodied AI field that achieves high quality, diversity, and large scale simultaneously.
* **MimicGen** [26 Oct 2023, CoRL 2023],[repo](https://github.com/NVlabs/mimicgen),[website](https://mimicgen.github.io/)：An efficient data generation framework developed based on Robosuite and MuJoCo, mainly focusing on single-arm robot desktop operation tasks, supporting multiple mainstream robot models. MimicGen proposes an automated data augmentation method that can automatically generate a large amount of simulation data from a small number of real human demonstrations, for example, using only 200 real human demonstrations to generate more than 50,000 simulation demonstration data, covering 18 common robot tasks.
* **RoboCasa** [4 Jun 2024],[repo](https://github.com/robocasa/robocasa), [website](https://robocasa.ai/): A high-fidelity kitchen task simulation platform built in MuJoCo based on RoboSuite and MimicGen. RoboCasa provides 120 diversified kitchen environments, containing more than 2500 3D object models. The platform supports single-arm, dual-arm, humanoid robots, and mobile base-mounted robotic arm robot systems. In addition, RoboCasa has 25 built-in basic atomic tasks and 75 composite tasks, capable of realistically simulating diverse operational behaviors of robots in complex kitchen scenarios.
* **DexMimicGen** [6 Mar 2025, ICRA 2025],[repo](https://github.com/NVlabs/dexmimicgen/), [website](https://dexmimicgen.github.io/): A high-fidelity dual-arm desktop operation task simulation environment built on the MuJoCo platform based on RoboSuite and MimicGen. DexMimicGen covers 9 typical dual-arm tasks, proposes an enhanced real2sim2real data automatic generation technology, requiring only 60 real human demonstrations to generate 21,000 high-quality simulation data. Compared to the original MimicGen, this framework significantly improves data generation efficiency and realism, making simulation training for robot dual-arm collaboration tasks more practical.
* **FUSE Dataset** [ICRA 2025] [website](https://fuse-model.github.io/) Contains 26,866 remote operation trajectories, covering three types of tasks: desktop grasping, grasping inside shopping bags, and button pressing. The robot operates through Meta Oculus Quest 2 VR headset, tasks combine language instructions and complex visual occlusions, supporting multi-sensor and language fusion robot strategy research.
* **BiPlay Dataset** [website](https://dit-policy.github.io/): To solve the problems of single tasks and fixed environments in existing dual-arm datasets, the BiPlay dataset uses random objects and backgrounds to collect diversified dual-arm operation trajectories. The data is split from multiple 3.5-minute robot operation videos into 7023 clips with language task descriptions, totaling 10 hours of data, supporting dual-arm operation generalization research.
* **DROID (Distributed Robot Interaction Dataset)**[website](https://droid-dataset.github.io/)：Contains 76,000 demonstration trajectories, about 350 hours of interaction data, covering 564 scenes and 86 tasks. Data collected by 50 collectors in North America, Asia, and Europe over 12 months, significantly improving scene and task diversity. Strategies trained based on DROID have better performance, robustness, and generalization ability. Dataset, training code, and hardware setup guide are all open source.
* **BridgeData V2**[website](https://rail-berkeley.github.io/bridgedata/)：Contains 60,096 trajectory data, covering 24 environments and 13 types of skills, supporting multi-task open vocabulary learning based on target images or natural language instructions. Data is mainly collected from 7 toy kitchen environments and diverse desktop, washing machine and other scenes, trajectories include 50,365 remote control demonstrations and 9,731 scripted policy executions. Each trajectory is annotated with corresponding natural language task descriptions, promoting cross-environment and cross-institutional skill generalization research.
* **Ego4DSounds** [website](https://ego4dsounds.github.io/)：As a multimodal subset of the large-scale first-person perspective dataset Ego4D, it contains over 1.2 million video clips, covering more than 3000 different daily scenes and behaviors, such as cooking, cleaning, shopping, and socializing. The data emphasizes the high correspondence between actions and environmental sounds, equipped with timestamped action narratives, supporting research on action perception, multimodal fusion, and sound generation in embodied AI.
* **RH20T**[website](https://rh20t.github.io/)：Human-robot interaction dataset, containing rich facial and voice information, note privacy protection when using, limited to model training only. Original data scale about 40TB, provides reduced size version (about 5TB RGB, 10TB RGB-D). Contains 7 sets of RGB videos and corresponding depth data, with camera calibration and robot joint angle information. Data publicly available for download via Google Drive and Baidu Cloud.
* **White Tiger Dataset** [website](https://www.openloong.org.cn/cn/dataset): Large-scale **heterogeneous robot** dataset, the first batch of open-source data focuses on four mainstream robot bodies (Qinglong Robot, Zhiyuan A2D, Fourier GR2, Leju Kuafu) and two types of typical end-effectors, covering five scenarios: industrial manufacturing, home housekeeping, catering services, supermarkets and pharmacies, and general grasping and placing, with task types exceeding 30 categories, a total of more than 100,000 high-quality task data released, providing a solid foundation for embodied AI algorithm training, model validation, and cross-platform evaluation.


<section id="paper_list"></section>

# 7. Paper Lists

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
* Embodied-AI-Paper-TopConf - Wenxuan Song, Jiayi Chen, Xiaoquan Sun: [repo](https://github.com/Songwxuan/Embodied-AI-Paper-TopConf)
<section id="acknowledgement"></section>

# 8. Acknowledgement
This article reprints/quotes some bloggers' articles, we thank them for their knowledge sharing, citation list as follows:
[1] Zhihu [Mu Yao](https://www.zhihu.com/people/mu-yao-12-34), [2] Zhihu [Donglin Zhongsheng](https://www.zhihu.com/people/dong-lin-zhong-sheng-76), Github [Yunlong Dong](https://github.com/yunlongdong), [3] Zhihu [Reinforcement Apprentice](https://www.zhihu.com/people/heda-he-28), [4] Zhihu [Biang Ge](https://www.zhihu.com/people/qi-da-guang), [5] OpenAI [Lilian Weng](https://lilianweng.github.io/), [6] Bilibili [Mumu Embodied](https://space.bilibili.com/350563565), [7] Github [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file), [8] Zhihu [Flood Sung](https://www.zhihu.com/people/flood-sung), [9] Github [Sida Peng](https://github.com/pengsida/learning_research)

<section id="cite"></section>

# 👍 Citation
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

# 🏷️ License
This repository is released under the MIT license. See [LICENSE](./LICENSE) for additional details.


<section id="star-history"></section>

# ⭐️ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=TianxingChen/Embodied-AI-Guide&type=Date)](https://star-history.com/#TianxingChen/Embodied-AI-Guide&Date)
