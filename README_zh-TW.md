![](./files/Embodied-AI-Guide-logo.png)
<h1 align="center">具身智能技術指南 Embodied-AI-Guide</h1>

<p align="center"> </p>


> Embodied AI（具身智能）入門的路徑以及高品質資訊的總結, 期望是按照路線走完後, 新手可以快速建立關於這個領域的認知, 希望能幫助到各位入門具身智能的朋友, 歡迎點 Star、分享與提 PR🌟~<br>【 <a href="https://github.com/tianxingchen/Embodied-AI-Guide">Embodied-AI-Guide</a>, Latest Update: May. 1, 2025 】<img alt="GitHub repo stars" src="https://img.shields.io/github/stars/TianxingChen/Embodied-AI-Guide"> ![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FTianxingChen%2FEmbodied-AI-Guide&label=Total%20Visitors&labelColor=%232ccce4&countColor=%23d9e3f0)


**語言:** [English](README_en.md) | [簡體中文](README.md) | 繁體中文


# Lumina 具身智能社群: [點擊訪問](https://lumina-embodied.ai)

> Embodied-AI-Guide 專案很快將會以網頁版 wiki 的形式上傳到 Lumina 具身智能社群網站，敬請期待。如果你對合作構建 Lumina 具身社群感興趣（目前更傾向於機構、社群間合作），歡迎郵件聯繫 <a href="mailto:lumina.embodiedai@gmail.com">lumina.embodiedai@gmail.com</a> 或聯創微信 <code>TianxingChen_2002</code>（請備註機構+姓名與來意）

**掃描右下圖關注 `Lumina 具身智能` 社群**:

<img src="./files/images/Lumina.png" alt="Task Descriptions">


# Contents - 目錄

<nav>
  <ul>
    <li><a href="#start">1. Start From Here - 從這裡開始</a></li>
    <li><a href="#info">2. Useful Info - 有利於搭建認知的資料</a></li>
    <li><a href="#algorithm">3. Algorithm - 演算法</a>
      <ul>
        <li><a href="#common-tools">3.1 Common Tools - 常用工具</a></li>
        <li><a href="#foundation-models">3.2 Foundation Models - 基礎模型</a></li>
        <li><a href="#robot-learning">3.3 Robot Learning - 機器人學習</a>
          <ul>
            <li><a href="#robot_autonomy">3.3.1 ETH & TTIC & UdeM Robot Autonomy - 自主機器人</a></li>
            <li><a href="#mpc">3.3.2 Model Predictive Control - 模型預測控制</a></li>
            <li><a href="#rl">3.3.3 Reinforcement Learning - 強化學習</a></li>
            <li><a href="#il">3.3.4 Imitation Learning - 仿人學習</a></li>
            <li><a href="#mila_robot_learning">3.3.5 MILA & UdeM Robot Learning - 機器人學習課程</a></li>
            <li><a href="#cmu_robot_learning">3.3.6 CMU 16-831 Introduction to Robot Learning - 機器人學習導論</a></li>
            <li><a href="#usc_robot_learning">3.3.7 USC CSCI 699: Robot Learning - 機器人學習</a></li>
            <li><a href="#mit_robot_manipulation">3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - 機器人操作</a></li>
            <li><a href="#underactuated_robotics">3.3.9 MIT 6.8210: Underactuated Robotics - 欠驅動機器人</a></li>
          </ul>
        </li>
        <li><a href="#llm_robot">3.4 LLM for Robotics - 大語言模型在機器人學中的應用</a></li>
        <li><a href="#vla">3.5 Vision-Language-Action Models - VLA 模型</li>
        <li><a href="#cv">3.6 Computer Vision - 電腦視覺</a>
          <ul>
            <li><a href="#2dv">3.6.1 2D Vision - 二維視覺</a></li>
            <li><a href="#3dv">3.6.2 3D Vision - 三維視覺</a></li>
            <li><a href="#4dv">3.6.3 4D Vision - 四維視覺</a></li>
            <li><a href="#vp">3.6.4 Visual Prompting - 視覺提示</a></li>
            <li><a href="#ag">3.6.5 Affordance Grounding - 可供性錨定</a></li>
          </ul>
        </li>
        <li><a href="#cg">3.7 Computer Graphics - 電腦圖形學</a></li>  
        <li><a href="#mm">3.8 Multimodal Models - 多模態模型</a></li>  
        <li><a href="#navigation">3.9 Robot Navigation - 機器人導航</a></li>  
        <li><a href="#embodied-ai-4-x">3.10 Embodied AI for X - 具身智能+X</a>
          <ul>
            <li><a href="#medical">3.10.1 EAI for Healthcare - 具身醫療</a></li>
            <li><a href="#uav">3.10.2 UAV - 無人機</a></li>
            <li><a href="#ad">3.10.3 Autonomous Driving - 自動駕駛</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li><a href="#control">4 Control and Robotics - 控制論與機器人學基礎</a>
      <ul>
        <li><a href="#41-控制理論基礎">4.1 控制理論基礎</li>
        <ul>
          <li><a href="#411-經典控制原理">4.1.1 經典控制原理</li>
          <li><a href="#412-現代控制理論線性系統控制">4.1.2 現代控制理論(線性系統控制)</li>
          <li><a href="#413-先進控制技術">4.1.3 先進控制技術</li>
        </ul>
        <li><a href="#42-機器人學導論">4.2 機器人學導論</li>
        <ul>
          <li><a href="#421-推薦材料">4.2.1 推薦資料</li>
          <li><a href="#422-機器人運動學-kinematics-與動力學-dynamics">4.2.2 機器人運動學與動力學</li>
          <li><a href="#423-里程計和同步定位與建圖-odometryslam">4.2.3 里程計和同步定位與建圖 (Odometry&SLAM)</li>
          <li><a href="#424-雜項-misc">4.2.4 雜項</li>
        </ul>
      </ul>
    </li> 
    <li><a href="#hardware">5. Hardware - 硬體</a>
      <ul>
        <li><a href="#embedded">5.1 Embedded - 嵌入式</a></li>
        <li><a href="#mechanical">5.2 Mechanical Design - 機械設計</a></li>
        <li><a href="#robosystem">5.3 Robot System Design - 機器人系統設計</a></li>
        <li><a href="#sensors">5.4 Sensors - 感測器</a></li>
        <li><a href="#tactile">5.5 Tactile Sensing - 觸覺感知</a></li>
        <li><a href="#companies">5.6 Companies - 公司</a></li>
      </ul>
    </li>
    <li><a href="#software">6. Software - 軟體</a>
      <ul>
        <li><a href="#simulators">6.1 Simulators - 模擬器</a></li>
        <li><a href="#benchmarks">6.2 Benchmarks - 基準集</a></li>
        <li><a href="#datasets">6.3 Datasets - 資料集</a></li>
      </ul>
    </li>
    <li><a href="#paper_list">7. Paper Lists - 論文列表</a></li>
    <li><a href="#acknowledgement">8. Acknowledgement - 致謝</a></li>
    <li><a href="#cite">👍 Citation - 引用</a></li>
    <li><a href="#license">🏷️ License - 許可證</a></li>
    <li><a href="#star-history">⭐️ Star History - Star 歷史</a></li>
  </ul>
</nav>



<section id="start"></section>

# 1. Start From Here - 從這裡開始

> 具身智能是指一種基於物理身體進行感知和行動的智能系統，其透過智能體與環境的交互獲取資訊、理解問題、做出決策並實現行動，從而產生智能行為和適應性。

## How - 如何學習這份指南

我們希望的是幫助新人快速建立領域認知，所以設計理念是：**簡要**介紹目前具身智能涉及到的主要技術，讓大家知道不同的技術能夠解決什麼問題，未來想要深入發展的時候能夠有頭緒。

## About us - 關於我們
我們是一個由具身初學者組成的團隊，希望能透過我們自己的學習經驗，為後來者提供一些幫助，加快具身智能的普及。歡迎更多朋友加入我們的專案，也很歡迎交友、學術合作，有任何問題，可以聯繫郵箱 `chentianxing2002@gmail.com`。

<p><b>🦉Contributors</b>: <a href="https://tianxingchen.github.io">陈天行 (港大 PhD)</a>, <a href="https://github.com/kxwangzju">王开炫 (港大 PhD)</a>, <a href="https://jiayueru.github.io/">贾越如 (北大 Ms)</a >, <a href="https://metaphysicist0.github.io/">姚天亮 (港中文 PhD)</a>, <a href="https://c7w.tech/about/">高焕昂 (清華 PhD)</a>, <a href="https://axi404.top/">高宁 (西交 BS)</a>, <a href="https://github.com/guo-cq">郭常青 (清華 Ms)</a>, <a href="https://shijiapeng03.github.io/">彭时佳 (深大 BS)</a>, <a href="https://yudezou.github.io/">邹誉德 (上交 AILab 聯培 PhD)</a>, <a href="">陈思翔 (北大 PhD)</a>, <a href="https://github.com/csyufei">朱宇飞 (上科大 Ms)</a>, <a href="https://github.com/LambdaGuard">韩翊飞 (清華 Ms)</a>, <a href="https://hao-starrr.github.io/">王文灏 (宾大 Ms)</a>, <a href="https://github.com/StarCycle">李卓恒 (港大 PhD)</a>, <a href="https://github.com/GihhArwtw">邱一航 (港大 PhD)</a>, <a href="https://github.com/Henry-lsy">梁升一 (港科廣 PhD)</a>, <a href="https://scholar.google.com/citations?user=azPXbWcAAAAJ&hl=en">林俊晓 (浙大 Ms)</a>, <a href="https://gkw0010.github.io/">王冠锟 (港中文 PhD)</a>, <a href="https://ngchikit.github.io">吴志杰 (港中文 PhD)</a>, <a href="https://github.com/27yw">叶雯 (中科院 PhD)</a>, <a href="https://github.com/zanxinchen">陈攒鑫 (深大 BS)</a>, <a href="https://hbhalpha.github.io">侯博涵 (山大 BS)</a>, <a href="https://github.com/Scodive">江恒乐 (25‘ 南科大 PhD)</a>, <a href="https://yongchao98.github.io/YongchaoChen/">陈勇超 (MIT+哈佛 PhD)</a>, <a href="https://aaron617.github.io/">胡梦康 (港大 PhD)</a>, <a href="https://liang-zx.github.io/">梁志烜 (港大 PhD)</a>, <a href="https://yimouwu.github.io/">吴贻谋 (港中文 MPhil)</a>, <a href="https://warshallrho.github.io/">吴睿海 (北大博士)</a>, <a href="https://yaomarkmu.github.io/">穆尧 (上交 AP)</a>.</p> 

<a href="https://github.com/TianxingChen/Embodied-AI-Guide/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=TianxingChen/Embodied-AI-Guide" />
</a>

<section id="info"></section>

# 2. Useful Info - 有利於搭建認知的資料

* 具身智能基礎技術路線-YunlongDong [2]: [PDF](./files/具身智能基础技术路线-YunlongDong.pdf), [bilibili](https://www.bilibili.com/video/BV1d5ukedEsi)

* 社交媒體:

  * 可以關注的公眾號: **石麻日記 (超高品質!!!)**, 機器之心, 新智元, 量子位, Xbot具身知識庫, 具身智能之心, 自動駕駛之心, 3D視覺工坊, 將門創投, RLCN強化學習研究, CVHub

  * AI 領域值得關注的博主列表 [3]: [zhihu](https://zhuanlan.zhihu.com/p/682110383)

* Robotics 實驗室總結 [4]: [zhihu_1](https://zhuanlan.zhihu.com/p/682671294?utm_psn=1782122763157188608), [zhihu_2](https://zhuanlan.zhihu.com/p/682692024?utm_psn=1782122945184796672)

* 具身智能會投稿的較高品質會議與期刊：Science Robotics, TRO, IJRR, JFR, RSS, IROS, ICRA, ICCV, ECCV, ICML, CVPR, NeurIPS, ICLR, AAAI, ACL 等。

* 史丹佛機器人學導論：[website](https://www.bilibili.com/video/BV17T421k78T)

* Cyber Nachos, [website](https://cybernachos.github.io/)

* 共建全網最全具身智能知識庫 [6]: [website](https://yv6uc1awtjc.feishu.cn/wiki/WPTzw9ON0ivIVrkLjVocNZh8nLf)

* Awesome-Embodied-AI-Job (具身智能招賢榜): [Repo](https://github.com/StarCycle/Awesome-Embodied-AI-Job/tree/main)

* 具身智能華人高引榜: [Repo](https://github.com/Will-Gao/Embodied_Intelligence)
  
* 社群:
  * Lumina 具身智能社群: [website](https://lumina-embodied.ai)
  * DeepTimber Robotics Innovations Community, 深木科研交流社群: [website](https://gamma.app/public/DeepTimber-Robotics-Innovations-Community-A-Community-for-Multi-m-og0uv8mswl1a3q7?mode=doc)
  * 宇樹具身智能社群: [website](https://www.unifolm.com/#/)
  * Simulately: Handy information and resources for physics simulators for robot learning research: [website](https://simulately.wiki/)
  * DeepTimber-地瓜機器人社群: [website](https://developer.d-robotics.cc/forumList?id=156&title=Deeptimber)
  * HuggingFace LeRobot (Europe, check the Discord): [website](https://github.com/huggingface/lerobot)
  * K-scale labs (US, check the Discord): [website](https://kscale.dev/)
  * OpenLoong 開源社群: [website](https://www.openloong.org.cn/cn)

<section id="algorithm"></section>

# 3. Algorithm - 演算法

<section id="common-tools"></section>

## 3.1 Common Tools - 常用工具

> 這個部分是關於具身中常用技巧的分享

* 點雲降採樣: [zhihu](https://zhuanlan.zhihu.com/p/558683732?utm_campaign=shareopn&utm_medium=social&utm_psn=1772067996070236160&utm_source=wechat_session), 包括隨機降採樣、均勻降採樣、最遠點降採樣、法線空間降採樣等, 需要了解清楚每一種降採樣的優劣, 這個技巧的選擇對於 3D 應用來說是至關重要的。
* 手眼標定：[github](https://github.com/fishros/handeye-calib), 手眼標定用於確定相機和機械臂之間以及相機與相機之間的相對位置, 大部分 Project 的開始都需要做一次手眼標定, 分為眼在手上和眼在手外。


<section id="foundation-models"></section>

## 3.2 Vision Foundation Models - 視覺基礎模型

> 以下是部分具身智能中常用的基礎模型, 電腦視覺中發展得非常好的工具可以直接賦能具身智能的下游應用。

* CLIP: [website](https://github.com/openai/CLIP), 來自 OpenAI 的研究, 最基本的應用是可以計算圖像與語言描述的相似度, 中間層的視覺特徵對各種下游應用非常有幫助。

* DINO: [DINO repo](https://github.com/facebookresearch/dino), [DINO-v2 repo](https://github.com/facebookresearch/dinov2), [DINO-v3 repo](https://github.com/facebookresearch/dinov3), 來自 Meta 的研究, 可以提供圖像的高層視覺特徵, 對 corresponding 之類的資訊提取非常有幫助, 比如不同個體之間的鼻子都有類似的幾何特徵, 這個時候不同圖像中關於不同鼻子的視覺特徵值可能是近似的。

* SAM: [website](https://segment-anything.com/), 來自 Meta 的研究, 可以基於提示點或者框, 對圖像的物體進行分割。

* SAM2: [website](https://ai.meta.com/sam2/), 來自 Meta 的研究, SAM 的升級版, 可以在影片層面持續對物體進行分割追蹤。

* SAM3: [website](https://ai.meta.com/sam3/), 來自 Meta 的研究, SAM2 的升級版, 能夠對由簡短文本短語所指定的所有實例進行窮舉式分割。

* Grounding-DINO: [repo](https://github.com/IDEA-Research/GroundingDINO), [線上嘗試](https://deepdataspace.com/playground/grounding_dino), **這個 DINO 與上面 Meta 的 DINO 沒有關係**, 是一個由 IDEA 研究院 (做了很多不錯開源項目的機構) 開發集成的圖像目標檢測的框架, 很多時候需要對目標物體進行檢測的時候可以考慮使用。

* OmDet-Turbo: [repo](https://github.com/om-ai-lab/OmDet), 一個由 OmAI Lab 開源的研究, 提供 OVD（開放詞表目標檢測）能力, 優點在於推理速度非常快（100+FPS）, 適合需要高 FPS 的自定義目標物體檢測場景。

* Grounded-SAM: [repo](https://github.com/IDEA-Research/Grounded-SAM-2), 比 Grounding-DINO 多了一個分割功能, 也就是支持檢測後分割, 也有很多下游應用, 具體可以翻一下 README。

* FoundationPose: [website](https://github.com/NVlabs/FoundationPose), 來自 Nvidia 的研究, 物體姿態追蹤模型。

* Stable Diffusion: [repo](https://github.com/CompVis/stable-diffusion), [website](https://ommer-lab.com/research/latent-diffusion-models/), 22 年的文生圖模型, 現在雖然不是 SOTA 了, 但是依然可以作為不錯的應用, 例如中間層特徵支持下游應用、生成 Goal Image (目標狀態) 等等。

* Depth Anything (v1 & v2 & v3): [repo](https://github.com/LiheYoung/Depth-Anything), [repo](https://github.com/DepthAnything/Depth-Anything-V2), [repo](https://github.com/ByteDance-Seed/Depth-Anything-3) 港大和字節的研究工作, 單目深度估計模型。

* Point Transformer (v3): [repo](https://github.com/Pointcept/PointTransformerV3), 點雲特徵提取的工作。

* RDT-1B: [website](https://rdt-robotics.github.io/rdt-robotics/), 清華朱軍老師團隊的工作, 機器人雙臂操作的基礎模型, 具有強大的 few-shot 能力。

* SigLIP: [huggingface](https://huggingface.co/docs/transformers/en/model_doc/siglip), 類似 CLIP。

<section id="robot-learning"></section>

## 3.3 Robot Learning - 機器人學習

機器人學習 Robot Learning 的發展: [zhihu](https://zhuanlan.zhihu.com/p/26988866)

<section id="robot_autonomy"></section>

### 3.3.1 ETH & TTIC & UdeM Robot Autonomy - 自主機器人

[課程影片](https://www.edx.org/learn/technology/eth-zurich-self-driving-cars-with-duckietown) ｜ [課程網站](https://duckietown.com/self-driving-cars-with-duckietown-mooc/)

該課程由 ETH 蘇黎世、TTIC 與蒙特利爾大學聯合開設，圍繞 Duckietown 平台系統講解自主機器人的構建過程，涵蓋感知、控制、建模、強化學習等模組。強調完整的感知-決策-控制閉環系統設計，並透過專案實踐推動學生掌握從 0 構建並部署一個具備自主導航能力的機器人智能體。適合希望初步了解機器人系統和 Robot Learning 的人。

<section id="mpc"></section>

### 3.3.2 Model Predictive Control (MPC) - 模型預測控制

模型預測控制（MPC）是一種先進的控制策略，利用系統的顯式動態模型預測有限時間範圍內的未來行為。每個控制週期，MPC 透過求解優化問題來確定控制輸入，以優化指定的性能指標，同時滿足輸入和輸出的約束條件。優化序列中的第一個控制輸入應用於系統，在下一個時間步中，結合新的系統狀態測量或估計，重複該過程。

* 入門推薦影片：

    - Model Predictive Control 模型預測控制,從公式到代碼 - 華工機器人實驗室: [bilibili](https://www.bilibili.com/video/BV1U54y1J7wh); 仿真工程原始碼:[Gitee](https://gitee.com/clangwu/mpc_control.git) 這門課程適合作為從 PID 到 MPC 的入門課程，適合只了解 PID 控制原理，但不太清楚 MPC 原理的入門者；從公式原理推導，到 CoppeliaSim（V-ERP）仿真教程以及 MatLab 代碼編寫，深入淺出。
    
* 經典工作：
  
    **理論基礎**：
    - [Model predictive control: Theory and practice—A survey](https://www.sciencedirect.com/science/article/abs/pii/0005109889900022) ： 這篇全面的綜述論文討論了 MPC 的理論基礎及其實踐應用，為未來的研究奠定了基礎。

    **非線性 MPC**：
    - [An Introduction to Nonlinear Model Predictive Control](https://pure.tue.nl/ws/files/3079152/555518.pdf#page=120) ： 提供了對非線性 MPC 的簡明介紹，擴展了 MPC 在具有顯著非線性系統中的應用。

    **顯式 MPC**：
    - [The explicit linear quadratic regulator for constrained systems](https://www.sciencedirect.com/science/article/abs/pii/S0005109801001741) ： 討論了顯式 MPC 解的公式化，對於需要快速即時控制的系統至關重要。

    **魯棒 MPC**：
    - [Predictive End-Effector Control of Manipulators on Moving Platforms Under Disturbance](https://ieeexplore.ieee.org/document/9425004) ： 使用時間序列分析預測基座運動並相應地轉換期望軌跡，使得機械臂可以達到主動在擾動下的基座運動。是使用二次規劃（QP）公式化模型預測控制（MPC）問題的經典之作。
    - [Min-max feedback model predictive control for constrained linear systems](https://ieeexplore.ieee.org/abstract/document/704989) ： 解決了 MPC 中的魯棒性，提出了處理模型不確定性並確保在擾動下性能的方法。

    **基於學習的 MPC**：
    - [Learning-Based Model Predictive Control for Safe Exploration](https://ieeexplore.ieee.org/abstract/document/8619572) ： 將機器學習與 MPC 相結合，代表了將數據驅動的模型和學習納入控制的現代趨勢。
    - [Confidence-Aware Object Capture for a Manipulator Subject to Floating-Base Disturbances](https://ieeexplore.ieee.org/document/10684104) ： 利用小波神經網路進行即時運動預測，並且引入置信度評價，實現短週期內最優軌跡規劃，使得機械臂在擾動平面上抓取無人機（UAV）表現優異，具備良好的魯棒性。

<section id="rl"></section>

### 3.3.3 Reinforcement Learning - 強化學習

* 強化學習的數學原理 - 西湖大學趙世鈺: [bilibili](https://space.bilibili.com/2044042934/channel/collectiondetail?sid=748665) [GitHub](https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning) 這門課程作為強化學習的入門課程非常合適，適合只對機器學習略有了解，但沒有了解過強化學習的初學者，可以了解強化學習的數學原理，其教材編寫也十分用心。

#### Deep Reinforcement Learning - 深度強化學習

下面列出三門比較受歡迎的深度強化學習相關的課程，這幾門課互有 overlap，時間長短和授課風格也各有不同，讀者可以選擇適合自己的課程進行學習。此外，深度強化學習的經典演算法相關的文章也在必讀清單：如 [PPO](https://arxiv.org/abs/1707.06347), [SAC](https://proceedings.mlr.press/v80/haarnoja18b/haarnoja18b.pdf), [TRPO](https://arxiv.org/abs/1502.05477), [A3C](https://arxiv.org/abs/1602.01783) 等。

* The Foundations of Deep RL in 6 Lectures [YouTube](https://www.youtube.com/watch?v=2GwBez0D20A) 本門線上課程由在 RL 領域著名的 Pieter Abbeel 教授主講，從 MDP 開始在六節課之內介紹了深度強化學習的主要知識。

* UC Berkeley CS285 深度強化學習: [website](https://rail.eecs.berkeley.edu/deeprlcourse/) | [YouTube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps) 本課程的主講老師是在 RL 領域著名的 Berkeley 的 Sergey Levine 教授，DRL 領域許多著名的工作如 SAC 就出自他之手。Sergey 在授課方面非常用心，本課程對 DRL 提供了非常詳細的介紹。

* 李宏毅老師也有一套關於強化學習的課程: bilibili 上課+刷蘑菇書鞏固+gymnasium 動手實踐, 重點了解一下 PPO。

  * 台灣大學李宏毅公開課: [bilibili](https://www.bilibili.com/video/BV1XP4y1d7Bk)

  * EasyRL - 蘑菇書: [website](https://datawhalechina.github.io/easy-rl/#/), 基本是配套李宏毅老師的課程

  * 實踐 [gymnasium](https://gymnasium.farama.org/), 可以嘗試一下把玩一下登月著陸等經典強化學習場景, 思考+動手, 觀察階段 agent 的表現並分析, 有助於深入理解強化學習

然而，深度強化學習的 Reward Tuning 和參數調整非常依賴於經驗，建議讀者在對深度強化學習有相關經驗之後，可以自己嘗試訓練一個 policy 並在機器人上部署，體會其中的 Sim-to-Real Gap。常用的仿真平台有 [MuJoCo PlayGround](https://playground.mujoco.org/), [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html), [SAPIEN](https://sapien.ucsd.edu/), [Genesis](https://github.com/Genesis-Embodied-AI/Genesis) 等。

常用的 Codebase 有 [legged-gym](https://github.com/leggedrobotics/legged_gym)（由 ETH RSL 開發，基於 IsaacGym）等，也可以根據你想做的任務找到相近的 codebase。

<section id="il"></section>

### 3.3.4 Imitation Learning - 模仿學習

* 《模仿學習簡潔教程》 - 南京大學 LAMDA: [PDF](https://www.lamda.nju.edu.cn/xut/Imitation_Learning.pdf)<br>
* Supervised Policy Learning for Real Robots, RSS 2024 Workshop 教程：真实机器人的监督策略学习, [bilibili](https://www.bilibili.com/video/BV1Fx4y1s7if)

<section id="mila_robot_learning"></section>

### 3.3.5 MILA & UdeM Robot Learning - 機器人學習課程

[課程影片](https://www.youtube.com/playlist?list=PLMe2pHxzxHp-UJ1jd-uuGSGK7P7Phtm-f) ｜ [課程網站](https://fracturedplane.notion.site/Robot-Learning-IFT6163-Scaling-Learning-for-Real-World-Agents-Apprentissage-robotique-Apprentiss-14a2148572768017864af202952c4b7e)

由 MILA 和蒙特利爾大學開設的課程，聚焦於將深度強化學習等方法擴展到現實世界中的機器人智能體，重點探討了現有學習技術的局限，並研究如何構建更強健、泛化能力更強的智能體系統。適合希望了解機器學習、強化學習演算法在機器人領域前沿應用的同學。

<section id="cmu_robot_learning"></section>

### 3.3.6 CMU 16-831 Introduction to Robot Learning - 機器人學習導論

[投影片](https://16-831-s24.github.io/lectures/) ｜ [作業](https://github.com/kavin-cmu/16831-S24-HW)

由 CMU Robotics Institute 開設的課程，雖然沒有影片，但是投影片內容簡明扼要，對整個 Robot Learning 有比較全面的覆蓋，而且內容 insights 很強，十分推薦學習。

<section id="usc_robot_learning"></section>

### 3.3.7 USC CSCI 699: Robot Learning - 機器人學習

[課程主頁](https://liralab.usc.edu/csci699/)

由南加州大學（USC）開設的課程，RL 相關內容很豐富，注重概念之間的聯繫，有很多 intuition。

<section id="mit_robot_manipulation"></section>

### 3.3.8 MIT 6.4210/6.4212: Robotic Manipulation - 機器人操作

[課程主頁](https://manipulation.csail.mit.edu/Fall2024/index.html) | [電子書](https://manipulation.mit.edu/)

由 MIT CSAIL 開設的課程，內容豐富且硬核，對機器人操作有比較全面的介紹，包含感知、規劃、動力學和控制。建議前置課程有：數學、程式設計、機器學習、機器人導論。

<section id="underactuated_robotics"></section>

### 3.3.9 MIT 6.8210: Underactuated Robotics - 欠驅動機器人

[課程主頁](https://underactuated.csail.mit.edu/Spring2024/index.html) | [課程影片](https://www.youtube.com/watch?v=v04rn86Dehg&t=4319s)

由 MIT CSAIL 開設的課程，介紹非線性動力學和欠驅動機械系統的控制。有 YouTube 影片，且錄製品質很高。

<section id="llm_robot"></section>

## 3.4 LLM for Robotics - 大語言模型在機器人學中的應用
為了促使機器人更好的規劃，現代具身智能工作常常利用大語言模型強大的資訊處理能力與泛化能力進行規劃。
* Robotics+LLM 系列透過大語言模型控制機器人 [2]: [zhihu](https://zhuanlan.zhihu.com/p/668053911)<br>
* Embodied Agent wiki: [website](https://en.wikipedia.org/wiki/Embodied_agent)<br>
* Lilian Weng 個人部落格 - AI Agent 系統綜述 [5]: 中文: [website](https://mp.weixin.qq.com/s/Jb8HBbaKYXXxTSQOBsP5Wg) 英文: [website](https://lilianweng.github.io/posts/2023-06-23-agent/)<br>
* 過去一系列工作常常僅使用 LLM 作為 High-Level 的策略生成器，用作 High-Level 規劃
  * 經典工作(1) PaLM-E: [Arxiv](https://arxiv.org/abs/2303.03378)<br>
  * 經典工作(2) DO AS I CAN, NOT AS I SAY: [Arxiv](https://arxiv.org/abs/2204.01691)<br>
  * 經典工作(3) Look Before You Leap: [Arxiv](https://arxiv.org/abs/2311.17842)<br>
  * 經典工作(4) EmbodiedGPT: [Arxiv](https://arxiv.org/abs/2305.15021)<br>
* 同時也有一些工作將 High-Level 的策略規劃與 Low-Level 的動作生成進行統一
  * 經典工作(1) RT-2: [Arxiv](https://arxiv.org/abs/2307.15818)<br>
* 另一個代表性方向的工作將 LLM 與傳統基於演算法的 Planner 結合來做任務與移動規劃
  * 經典工作(1) LLM+P: [Arxiv](https://arxiv.org/abs/2304.11477)<br>
  * 经典工作(2) AutoTAMP: [Arxiv](https://arxiv.org/abs/2306.06531)<br>
  * 經典工作(3) Text2Motion: [Arxiv](https://arxiv.org/abs/2303.12153)<br>
* 利用 LLM 的 code 能力實現具身智能是一個有趣的想法
  * 經典工作(1) Code as Policy: [Arxiv](https://arxiv.org/abs/2209.07753)<br>
  * 經典工作(2) Instruction2Act: [Arxiv](https://arxiv.org/abs/2305.11176)<br>
* 有一些工作將三維視覺感知同 LLM 結合起來，共同促進具身智能規劃
  * VoxPoser [Arxiv](https://arxiv.org/abs/2307.05973)<br>
  * OmniManip [Arxiv](https://arxiv.org/abs/2501.03841)<br>
* 還有一些工作試圖把基於 LLM 的機器人規劃擴展到多機器人協同合作的場景
  * 經典工作(1) RoCo: [Arxiv](https://arxiv.org/abs/2307.04738)<br>
  * 經典工作(2) Scalable-Multi-Robot: [Arxiv](https://arxiv.org/abs/2309.15943)<br>

<section id="vla"></section>

## 3.5 Vision-Language-Action Models - VLA 模型
**Vision-Language-Action Models (VLA 模型)** 是一種結合 VLM (Vision-Language Model) 與機器人控制的模型，旨在將預訓練的 VLM 直接用於生成機器人動作（RT-2 中定義）。和以往利用 VLM 做 planning 以及 build from scratch 的方法不同，VLA 無需重新設計新的架構，將動作轉化為 token，微調 VLM。

**VLA 的特點**：端到端，使用 LLM/VLM backbone，載入預訓練模型，etc. 

目前的 VLA 可以從以下幾個方面進行區分：模型結構與大小（如 action head 的設計，tokenize 的方法如 FAST），預訓練與微調策略和資料集，輸入與輸出（2D vs. 3D | TraceVLA 輸入 visual trace），不同的應用場景等。

**參考資料：**

* Blog:  [具身智能 Vision-Language-Action 的思考](https://zhuanlan.zhihu.com/p/9880769870), [zhihu](https://www.zhihu.com/question/655570660/answer/87040917575)

* Survey:
  - A Survey on Vision-Language-Action Models: An Action Tokenization Perspective ([paper](https://arxiv.org/abs/2507.01925) | [repo](https://github.com/Psi-Robot/Awesome-VLA-Papers), 2025.07.02)
  - A Survey on Vision-Language-Action Models for Embodied AI ([paper](https://arxiv.org/abs/2405.14093), 2024.11.28)

### **3.5.1 經典工作**：

* **Autoregressive Models**

  - **RT 系列 (Robotic Transformers)**:
    - **RT-1** ([paper](https://arxiv.org/abs/2212.06817))
    - **RT-2** ([page](https://robotics-transformer2.github.io/) | [paper](https://arxiv.org/abs/2307.15818), Google Deepmind, 2023.7)：55B
    - **RT-Trajectory** ([paper](https://arxiv.org/pdf/2311.01977), Google Deepmind, UCSD, 史丹佛大學 2023.11)
    - **AUTORT** ([paper](https://arxiv.org/abs/2401.12963), Google Deepmind, 2024.1)

  - **RoboFlamingo** ([paper](https://arxiv.org/abs/2311.01378) | [code](https://github.com/roboflamingo), 字节、清華大學, 2024.2)

  - **OpenVLA** ([paper](https://arxiv.org/pdf/2406.09246) | [code](https://github.com/openvla), Stanford, 2024.6): 7B

  - **TinyVLA** ([paper](https://arxiv.org/abs/2409.12514), 上海大學, 2024.11)
  - **TraceVLA** ([paper](https://arxiv.org/pdf/2412.10345) | [code](https://github.com/umd-huang-lab/tracevla), 微软, 2024.12)

* **Diffusion Models for Action Head:**

  - **Octo** ([paper](https://arxiv.org/pdf/2405.12213) | [code](https://octo-models.github.io/), 史丹佛大學、柏克萊大學, 2024.5): Octo-base (93M)

  - **π0** ([paper](https://arxiv.org/pdf/2410.24164) | [code](https://github.com/Physical-Intelligence/openpi), 史丹佛大學, Physical Intelligence, ) : 3.3B; flow-based diffusion VLA; PaliGemma (3B VLM);

  - **CogACT** ([paper](https://arxiv.org/pdf/2411.19650) | [code](https://github.com/microsoft/CogACT.git), 清華大學, MSRA, 2024.11): 7B

  - **Diffusion-VLA** ([paper](https://arxiv.org/abs/2412.03293) | [code](https://arxiv.org/pdf/2410.07864), 華東師範大學、上海大學、美的, 2024.12)

* **3D Vision:**
  - **3D-VLA** ([paper](https://arxiv.org/pdf/2403.09631) | [code](https://github.com/UMass-Foundation-Model/3D-VLA/tree/main), UMass, 2024.3): 3D-based LLM
  - **SpatialVLA** ([paper](https://arxiv.org/pdf/2501.15830) | [code](https://github.com/SpatialVLA/SpatialVLA) , 上海 AI Lab, 2025.1): Adaptive Action Grid

* **VLA-related:**

  - **FAST (π0)** ([paper](https://arxiv.org/pdf/2410.24164), [code](https://github.com/Physical-Intelligence/openpi.git), 史丹佛大學、柏克萊大學, Physical Intelligence, 2025.1):  autoregressive VLA

  - **RLDG** ([paper](https://generalist-distillation.github.io/static/high_performance_generalist.pdf) | [code](https://arxiv.org/abs/2410.01971), 柏克萊大學, 2024.12 ): 強化學習 (RL) 生成高品質的訓練資料進行微調

  - **BYO-VLA** ([paper](https://arxiv.org/abs/2410.01971) | [code](https://github.com/irom-princeton/byovla), 普林斯頓大學, 2024.10): 執行時影像干預，有效降低 VLA 模型對任務無關視覺干擾的敏感度

* **Different Locomotion:**

  - **RDT-1B (雙臂)** ([paper](https://arxiv.org/pdf/2410.07864) | [code](https://github.com/thu-ml/RoboticsDiffusionTransformer), 清華大學): 雙臂控制的擴散模型

  - **QUAR-VLA (四足機器人)** ([paper](https://arxiv.org/pdf/2312.14457), 西湖大學、浙江大學, 2025.2.4)

  - **CoVLA (自動駕駛)** ([paper](https://arxiv.org/abs/2408.10845) | [page](https://turingmotors.github.io/covla-ad/), Turing, 2024.12)

  - **Mobility-VLA (導航)** ([paper](https://arxiv.org/pdf/2407.07775), Google Deepmind, 2024.7)

  - **NaVILA (腿式機器人導航)** ([paper](https://arxiv.org/pdf/2412.04453) | [code](https://navila-bot.github.io/), UCSD, 2024.12)

### **3.5.2 雙系統分層 VLA**：（2025.5 更新） ⭐

目前 VLA 的一大範式是採用分層雙系統架構，模擬人類的快速反應（System 1）和深度思考（System 2）機制。System 2 利用視覺語言模型（VLM）進行環境理解和任務規劃，接收視覺、語言等多模態輸入，並透過語言或潛在向量（Latent Vector）將資訊傳遞給 System 1。System 1 則將這些規劃轉化為精確的機器人動作。
目前，採用雙系統架構的主要區別在於：
- *單模型 vs 雙模型架構*：例如，Hi-Robot 採用了 VLM + VLA 的雙模型架構，而 pi-0.5 則採用了單模型架構。
- *快慢系統的通訊方式*：快慢系統在何時分層，通訊可以透過低級指令（low-level command）或潛在向量（latent vector）進行。
- *仿真訓練資料的使用*：如 GROOT N-1 使用了模擬器資料和合成資料，而 pi 系列則完全依賴於真實機器人資料。
- 在*模型表現*方面，可以關注以下幾個方面：模型大小、動作輸出頻率以及任務的難度（如人形、長程任務、柔性物體處理、跨本體性能等）。

**產業級 VLA**：

- **Figure: Helix** (link: [Figure](https://www.figure.ai/news/helix), 2025.2.20): 機器人全身上半身控制
- **智元：GO-1** (link: [智元官网](https://www.zhiyuan-robot.com/article/189/detail/56.html), 2025.3.10)：ViLLA: VLM+MoE, vision-language-latent-action model
- **Physical Intelligence** : code https://github.com/Physical-Intelligence/openpi
  - **pi-0.5** ([paper](https://arxiv.org/abs/2504.16054) | blog: CSDN, 2025.4.22): 高級任務分解後由單一模型執行低級任務
  - **Hi Robot** ([paper](https://arxiv.org/abs/2502.19417) | blog: CSDN, 2025.2.26): 使用 VLM 進行高級推理，VLA 執行低級任務
- **Nvidia: GROOT-N1** (code: [Nvidia Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) | [paper](https://arxiv.org/abs/2503.14734) | blog, 2025.3.27): 機器人全身控制, 2B, NVIDIA-Eagle 架構和 SmolLM-1.7B
- **灵初智能：Psi-R1** ([blog](https://www.jiqizhixin.com/articles/2025-03-03-9), 2025.4.27): 分層端到端 VLA+強化學習演算法模型, 驗證 test-time scaling
- **Google DeepMind: Gemini Robotics** ([paper](https://arxiv.org/pdf/2503.20020), 2025.3.25): Gemini 2.0 構建的 Gemini Robotics-ER（具身推理模型）和 Gemini Robotics 主模型, 50 Hz; **Gemini Robotics on device** ([report](https://deepmind.google/discover/blog/gemini-robotics-on-device-brings-ai-to-local-robotic-devices/), 2025.6.24) 將模型輕鬆部署在設備端


### **3.5.3 最新 VLA 工作**：

- **VQ-VLA** ([paper](https://arxiv.org/pdf/2507.01016) | [code](https://github.com/xiaoxiao0406/VQ-VLA), 上海 AI Lab, 同濟大學, 中國科學技術大學 (中科大), 浙江大學 (浙大), 南京大學 (南大), 上海交通大學 (上交大), ICCV 25, 2025.7.1): 利用 VQ action tokenizer 提升 VLA 表現
- **WorldVLA** ([paper](https://arxiv.org/pdf/2506.21539) | [code](https://github.com/alibaba-damo-academy/WorldVLA), 阿里达摩院, 湖畔 Lab, 浙江大學 (浙大), 2025.6.21): 將 VLA 和 World Model 在一個框架中統一
- **BridgeVLA** ([paper](https://arxiv.org/abs/2506.07961) | [code](https://github.com/BridgeVLA/BridgeVLA), CASIA, 字节 Seed, UCAS, FiveAges, 南京大學 (南大), 2025.6.7): 將 3D 資訊在 2D 空間中對齊
- **TrackVLA** ([paper](https://arxiv.org/pdf/2505.23189) | [code](https://github.com/wsakobe/TrackVLA), 北京大學 (北大), Galbot, 北京航空航天大學 (北航), 北京師範大學 (北師大), BAAI, 2025.5.29): 實現即時目標檢測與導航
- **OneTwoVLA** ([paper](https://arxiv.org/pdf/2505.11917) | [code](https://github.com/Fanqi-Lin/OneTwoVLA), 清華大學, 上海期智, 上海 AI Lab, 復旦大學, Spirit AI, 2025.5.17): 同時實現推理與動作執行
- **MoManipVLA** ([paper](https://arxiv.org/pdf/2503.13446) | [project](https://gary3410.github.io/momanipVLA/), 北京郵電大學 (北郵), NTU, 清華大學, CVPR 25, 2025.3.17): 解決移動操作任務的 VLA
- **TLA** ([paper](https://arxiv.org/pdf/2503.08548) | [project](https://sites.google.com/view/tactile-language-action/), 三星, 自動化所, BAAI, 2025.3.11): 額外引入觸覺模態實現更精準的抓取
- **PointVLA** ([paper](https://arxiv.org/pdf/2503.07511) | [project](https://pointvla.github.io/), 美的, 上海大學, 華東師範大學, 2025.3.10): 利用點雲對 2D VLA 進行微調以學習更好的空間適應性
- **SafeVLA** ([paper](https://arxiv.org/abs/2503.03480) | [code](https://github.com/PKU-Alignment/SafeVLA), 北京大學 (北大), 2025.3.5): 解決傳統 VLA 模型在抓取和導航任務中的不安全行為
- **HybridVLA** ([paper](https://arxiv.org/pdf/2503.10631) | [code](https://github.com/PKU-HMI-Lab/Hybrid-VLA), 北京大學 (北大), 2025.3.17): 用統一模型整合擴散和自回歸動作預測，2.7B 和 7B 模型
- **DexVLA** ([paper](https://arxiv.org/pdf/2502.05855) | [code](https://github.com/juruobenruo/DexVLA), 美的, 東南大學, 2025.2.9): Diffusion expert 1B，採用多個 action head
- **DexGraspVLA** ([paper](https://arxiv.org/abs/2502.20900) | [code](https://github.com/Psi-Robot/DexGraspVLA), 北京大學 (北大), 2025.2.28): 靈巧手抓取 VLA
- **UP-VLA** ([paper](https://arxiv.org/pdf/2501.18867), 清華大學, 2025.2.3): 加入 goal-image 預測任務幫助動作生成
- **CoT-VLA** ([paper](https://arxiv.org/pdf/2503.22020) ,  Nvidia, Stanford, CVPR2025): 將 CoT 融入 VLA 中，透過自回歸地預測未來的影像幀作為視覺目標，7B
- **UniAct** ([paper](https://arxiv.org/abs/2501.10105) | [code](https://github.com/2toinf/UniAct), CVPR2025, 清華大學): 基於通用動作空間的具身基礎模型
- **UniVLA** ([paper](https://arxiv.org/pdf/2505.06111) | [code](https://github.com/OpenDriveLab/UniVLA), 香港大學 (港大), 上海人工智能實驗室, 智元, 2025.5.9): 利用潛在動作模型從多樣化資料中提取任務核心表徵，提升泛化能力，降低計算和資料需求


<section id="cv"></section>

## 3.6 Computer Vision - 計算機視覺

CS231n (史丹佛大學計算機視覺課程): [website](https://cs231n.stanford.edu/schedule.html), 該課程對深度學習在計算機視覺的應用有較為全面的介紹。因為已經在具體實現某篇論文的演算法了，所以這個階段可以不用做作業，只需要看課程影片和課程講義即可。<br>

<section id="2dv"></section>

### 3.6.1 2D Vision - 二維視覺
* 2D Vision 領域的經典代表作
  * CNN (卷積神經網路): [link](https://easyai.tech/ai-definition/cnn/)
  * ResNet (深度殘差網路): [bilibili](https://www.bilibili.com/video/BV1P3411y7nn)
  * ViT (第一個將 Transformer 用在視覺領域): [bilibili](https://www.bilibili.com/video/BV15P4y137jb)
  * Swin Transformer (披著 Transformer 皮的 CNN): [bilibili](https://www.bilibili.com/video/BV13L4y1475U)
  * 對比學習論文綜述: [bilibili](https://www.bilibili.com/video/BV19S4y1M7hm)
* 以判別式模型為主的感知任務，比如識別、分類、分割、檢測等等，看看即可，現在繼續刷點意義不大
* 生成式模型
  * 自回歸綜述: [PDF](https://arxiv.org/pdf/2411.05902)
  * 擴散模型綜述: [PDF](https://arxiv.org/pdf/2209.00796)
  * 如果對擴散模型的理論推導感興趣，可以看蘇劍林老師的部落格 - 生成擴散模型漫談（推導非常清楚）: [link](https://kexue.fm/archives/9119)

<section id="3dv"></section>

### 3.6.2 3D Vision - 三維視覺

* 三維視覺導論 - Andreas Geiger: [website](https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/autonomous-vision/lectures/computer-vision/) (重點關注課程作業) <br>
* GAMES203 - 三維重建與理解: [bilibili](https://www.bilibili.com/video/BV1pw411d7aS)<br>
* 三維生成的一些經典論文:
  * Diffusion Model for 2D/3D Generation 相關論文分類: [link](https://zhuanlan.zhihu.com/p/617510702)
  * 3D 生成相關論文-2024: [link](https://zhuanlan.zhihu.com/p/700895749)

<section id="4dv"></section>

### 3.6.3 4D Vision - 四維視覺
* 影片理解
  * 開山之作: [bilibili](https://www.bilibili.com/video/BV1mq4y1x7RU)
  * 論文串講: [bilibili](https://www.bilibili.com/video/BV1fL4y157yA)
  * LLM 時代的影片理解綜述: [PDF](https://arxiv.org/pdf/2312.17432)
* 4D 生成
  * 影片生成部落格 (英文): [link](https://lilianweng.github.io/posts/2024-04-12-diffusion-video/)
  * 4D 生成的論文列表: [website](https://github.com/cwchenwang/awesome-4d-generation)

<section id="vp"></section>

### 3.6.4 Visual Prompting - 視覺提示

視覺提示是一種利用視覺輸入引導大模型完成特定任務的方法，常用於具身智能領域。它透過提供示例圖像、標註或視覺線索，讓模型理解任務要求，而無需額外訓練。例如，在機器人導航、操控等場景中，視覺提示可幫助模型適應新環境，提高泛化能力。相比傳統方法，視覺提示具備更強的靈活性和可擴展性，使具身智能系統能夠透過視覺資訊快速適應複雜任務。

- 視覺提示綜述：[paper](https://arxiv.org/abs/2409.15310)
- **PIVOT**, [page](https://pivot-prompt.github.io): 透過將任務轉化為迭代式視覺問答，實現在無需特定任務資料微調的情況下，zero-shot 控制機器人系統和進行空間推理。
- **Set-of-Mark Visual Prompting for GPT-4V**: [page](https://som-gpt4v.github.io)

<section id="ag"></section>

### 3.6.5 Affordance Grounding - 可供性錨定

可供性錨定任務的目標是從圖像中定位物體上能夠與之互動的區域，充當了感知與行動之間的橋梁，是具身智能重要的一環。它不僅需要模型對物體及其局部結構的檢測與識別，還需要模型理解物體與人或機器人之間的潛在互動關係。例如，在機器人抓取場景中，可供性錨定幫助模型尋找物體上最佳的抓取位置，從而確定最佳抓取角度。該方向透過整合計算機視覺、多模態大模型技術，能夠在弱監督或零樣本條件下實現對物體互動可能性的精確定位，提升機器人抓取、操作以及人機互動等任務的性能。

* **2D**
  - 跨視角學習可供性：**Cross-View-AG**, [paper](https://arxiv.org/pdf/2203.09905): 第三視角圖像提供他者如何與物體互動的資訊，幫助模型學習如何與第一視角圖像中的物體互動。
  - 單視角學習可供性：**AffordanceLLM**, [paper](https://arxiv.org/pdf/2401.06341)：透過利用預訓練的大規模視覺語言模型中的豐富知識，顯著提升了物體可供性錨定在未見對象和動作上的泛化能力。
  - 資料集：**AGD20K**, [page](https://github.com/lhc1224/Cross-View-AG)

* **3D**
  - 基於點雲的可供性錨定：**OpenAD**, [paper](https://arxiv.org/pdf/2203.09905)
  - 鉸接物體的可供性錨定：**Where2Act**, [paper](https://arxiv.org/abs/2101.02692); **VAT-Mart**, [paper](https://openreview.net/pdf?id=iEx3PiooLy)
  - 柔性物體的可供性錨定：**DeformableAffordance**, [paper](https://arxiv.org/pdf/2303.11057); **UniGarmentManip**, [paper](https://arxiv.org/abs/2405.06903)
  - 室內環境任務中的可供性錨定：**SceneFun3D**, [paper](https://arxiv.org/pdf/2401.06341)
  - 點雲資料集：**3D AffordanceNet**, [page](https://github.com/lhc1224/Cross-View-AG)，專注於物體層面的可供性錨定。
  - 實物資料集：**SceneFun3D**, [page](https://scenefun3d.github.io/)，強調在真實室內環境的應用。

<section id="cg"></section>

## 3.7 Computer Graphics - 計算機圖形學

如果說計算機視覺是考慮圖像之間的變化以及從圖像到三維模型（三維重建和生成），那麼計算機圖形學主要研究的就是三維模型之間的變化以及從三維模型到圖像的渲染過程。具身智能在開發和測試的時候離不開模擬器，而模擬也屬於圖形學的研究範疇。快速、高品質的渲染，並行化、準確的模擬一直是機器人模擬器追求的目標，而這一切透過計算機圖形學來實現。

* 如果對傳統圖形學感興趣，可以看下面兩門（闫令琪老師開的課，講得特別好）：<br>
  * **GAMES101 - 現代計算機圖形學入門**: [website](https://games-cn.org/intro-graphics/)<br>
  * GAMES202 - 高品質即時渲染: [website](https://sites.cs.ucsb.edu/~lingqi/teaching/games202.html)<br>
* 如果對 motion synthesis/computer animation 感興趣，可以看：
  * GAMES105 - 計算機角色動畫基礎: [website](https://games-105.github.io/)<br>
* 如果對三維重建感興趣，可以看下面兩門：
  * Nerf 原理代碼講解: [bilibili](https://www.bilibili.com/video/BV1CC411V7oq)
  * 3DGS 原理代碼講解: [bilibili](https://www.bilibili.com/video/BV1zi421v7Dr)
* 三維預訓練最新綜述:
  * Advances in 3D pre-training and downstream tasks: a survey: [PDF](https://link.springer.com/content/pdf/10.1007/s44336-024-00007-4.pdf)<br>
* 3DGS 在具身上的綜述:
  * 3D Gaussian Splatting in Robotics: A Survey: [PDF](https://arxiv.org/pdf/2410.12262v2)<br>

<section id="mm"></section>

## 3.8 Multimodal Models - 多模態模型

> 多模態旨在統一來自不同模態資訊的表徵，在具身智能中由於面對著機器識別的視覺資訊與人類自然語言的引導資訊等不同模態的資訊，多模態技術愈發重要。
* 最經典的工作 CLIP: [知乎](https://zhuanlan.zhihu.com/p/493489688)<br>
* 多模態大語言模型的經典工作 LLaVA: [website](https://llava-vl.github.io/)<br>
* 多模態生成模型綜述: [pdf](https://arxiv.org/pdf/2503.04641)<br>
* 多模態大語言模型強化學習項目：VLM-R1: [repo](https://github.com/om-ai-lab/VLM-R1) 來自 OmAI Lab 的多模態大語言模型 DeepSeek R1-style 強化學習開源項目，使用 GRPO 強化學習演算法對多模態大語言模型進行優化，效果優於常規 SFT，是訓練具身智能模型的一種新方向。<br>

<section id="navigation"></section>

## 3.9 Robot Navigation - 機器人導航
**機器人導航（Robot Navigation）**是一類要求智能體在**已知或未知**場景中，透過獲取並處理環境資訊，實現達成某種目標的路徑規劃。機器人導航是具身任務中的一個重要能力，是完成複雜任務不可缺少的基礎技術。機器人導航任務中，智能體一般接受感測器提供的 RGB、深度、GPS 等資訊和相關目標指令，輸出是一系列的動作指令。

按照任務類型分類，機器人導航可以分為以下幾個部分：

- **物體目標導航（Object-Goal Navigation）**：最常見和最廣泛的導航任務。智能體接受的指令是對一個特定物體的描述，目標是找尋到這個物體。
- **圖像目標導航（Image-Goal Navigation）**：智能體接受的指令是一個圖像，目標是找尋到這個圖像所描述的場景。
- **視覺-語言導航（Vision-Language Navigation，VLN）**：智能體接受的指令是一個自然語言指令描述，目標是跟隨該指令行進。

按照模型架構分類，機器人導航可以分為以下幾個類別：

- **端到端模型（End-to-End Model）**：模型直接將感測器輸入透過強化學習或模仿學習映射到動作指令。模型會先將感測器資訊編碼為視覺表徵，結合歷史動作作為輸入，最後透過與環境互動獲得 reward 實現動作決策的學習。端到端模型主要針對兩方面進行優化：一是提升視覺表徵能力，二是解決稀疏獎勵等動作決策方面的問題。端到端模型的優勢在於直截了當，但是面臨著嚴重的過擬合和低泛化性問題，使得其在現實生活中的應用受到了挑戰。

    - 經典工作：

        - [Learning Object Relation Graph and Tentative Policy for Visual Navigation](https://arxiv.org/abs/2007.11018)
        - [VTNet: Visual Transformer Network for Object Goal Navigation](https://openreview.net/forum?id=DILxQP08O3B)

- **模組化模型（Modular Model）**：將感測器資訊輸入不同的模組，模組之間透過介面互動，輸出動作指令。模組包括建圖模組（Mapping，構建語義和佔有地圖），長期決策模組（Global Policy，決定長期的導航目標），短期決策模組（Local Policy，決定實現長期目標具體操作）等。建圖模組是模型的核心，包含有網格地圖、包含預測的網格地圖、圖表示地圖等多種形式。模組化模型的優勢在於模組之間的解耦，大大加強了模型的可解釋性。同時，獨立的建圖模組也使得模型更容易泛化到未知環境。但是模組化模型的建圖模組仍然充斥著手動設計的規則，這一定程度上也限制了模型的通用性。
  
    - 經典工作：
      
        - [Object Goal Navigation using Goal-Oriented Semantic Exploration](https://arxiv.org/abs/2007.00643) ： SemExp，最早提出語義地圖的概念，學習區域和物體之間關聯的語義先驗，使智能體能夠更好地判斷目標物體可能在的方向。
        - [PONI: Potential Functions for ObjectGoal Navigation with Interaction-free Learning](https://openaccess.thecvf.com/content/CVPR2022/papers/Ramakrishnan_PONI_Potential_Functions_for_ObjectGoal_Navigation_With_Interaction-Free_Learning_CVPR_2022_paper.pdf)：PONI，提出了基於 potential functions 的語義地圖預測，即基於已有的語義地圖學習「補全」的完整地圖，想像物體最可能在整個房間的哪個位置，使智能體能夠遷移在其他樣本中觀察到的知識。
        - [3D-Aware Object Goal Navigation via Simultaneous Exploration and Identification](https://arxiv.org/abs/2212.00338)：把 3D 資訊編碼進導航的經典工作，透過更精細的點雲分割資訊，避免了 2D 語義圖在 z 軸上的資訊損失，實現了更精確的語義地圖構建。

- **零樣本模型（Zero-shot Model）**：模型不接觸訓練資料，直接在測試階段完成任務。零樣本模型往往利用具有知識先驗的大規模預訓練模型（CLIP, LLM 等）實現。零樣本模型的提出旨在解決基於學習的方法面臨的過擬合和低泛化性問題，同時也更適合遷移到現實場景。但是零樣本模型的缺陷在於推理速度較慢，且性能受限，需要進一步微調以實現更好的性能。

    - 經典工作：

        - [CoWs on Pasture: Baselines and Benchmarks for Language-Driven Zero-Shot Object Navigation](https://arxiv.org/abs/2203.10421)：開放語義物體導航的提出工作。思路很簡單：用 CLIP 尋找目標物體，找到了就走過去。在不常見物體、複雜描述上取得了很好的效果，同時也有著對不同屬性的同類別物體的區分能力。
        - [L3MVN: Leveraging Large Language Models for Visual Target Navigation](https://arxiv.org/abs/2304.05501)：利用 LLM 決定「我要向哪個邊界前進」。利用 LLM 的人類知識先驗，判斷物體可能在的房間，以及與其他物體之間的相關關係，實現更快速更有效的導航。
        - [ESC: Exploration with Soft Commonsense Constraints for Zero-shot Object Navigation](https://arxiv.org/abs/2301.13166)：顯式提出了區域對於導航的影響，在語義地圖上標註出區域佔有的位置，作為輸入的一部分輸入給 LLM。結合了語義地圖連續性和 LLM 知識豐富的優勢。
        - [SG-Nav: Online 3D Scene Graph Prompting for LLM-based Zero-shot Object Navigation](https://arxiv.org/abs/2410.08189)：在線構建多層場景圖 (Scene Graph) 並輸入給 LLM，利用 CoT 實現 LLM 對於物體位置的推理。

常用資料集：

- [MatterPort3D(MP3D)](https://niessner.github.io/Matterport/)：真實場景採集，場景複雜龐大，資料量大，難度高。
- [Habitat-Matterport3D(HM3D)](https://aihabitat.org/datasets/hm3d/)：同上
- [RoboTHOR](https://ai2thor.allenai.org/robothor/)：模擬環境，場景小簡單。


其他參考：

- [物體目標導航綜述](https://orca.cardiff.ac.uk/id/eprint/167432/1/ObjectGoalNavigationSurveyTASE.pdf)
- [awesome vision-language navigation](https://github.com/eric-ai-lab/awesome-vision-language-navigation)
- [Habitat Navigation Challenge](https://github.com/facebookresearch/habitat-challenge)（Habitat 框架中整合了非常多常見的 agent skill，例如語義地圖構建，FBE 和一些 heuristic 方法，非常適合模組化方法的開發）

<section id="embodied-ai-4-x"></section>

## 3.10 Embodied AI for X - 具身智能+X

<section id="medical"></section>

### 3.10.1 EAI for Healthcare - 具身醫療

> 具身智能技術的迅猛發展正在引領醫療服務模式邁向革命性的新紀元。作為人工智慧演算法、先進機器人技術與生物醫學深度融合的前沿交叉學科，具身智能+醫療這一研究領域不僅突破了傳統醫療的邊界，更開創了智能化醫療的新範式。其多學科協同創新的特質，正在重塑醫療服務的全流程，為精準醫療、遠程診療和個性化健康管理帶來前所未有的發展機遇，推動醫療行業向更智能、更人性化的方向轉型升級。這一領域的突破性進展，標誌著醫療科技正邁向一個全新的智能化時代。
> 
* 醫療具身智能綜述: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/abs/2501.07468)<br>

#### 3.10.1.1 MLLM for Medical - 多模態大語言模型在醫學中的應用
* 用於醫學影像分析的通用人工智慧綜述: [website](https://arxiv.org/pdf/2306.05480)<br>
* 醫學影像的通用分割模型-MedSAM： [website](https://www.nature.com/articles/s41467-024-44824-z.pdf)<br>
* 2024 盤點：醫學 AI 大模型，從通用視覺到醫療影像: [NEJM 醫學前沿](https://mp.weixin.qq.com/s?__biz=MzIxNTc4NzU0MQ==&mid=2247550230&idx=1&sn=6baa8dcba12f3f70f4c8205a0f23b6a0&chksm=966df4ca45c8cbcaa0a5d2e42fbb4de92e6881f92981071ce7fda3bd1e13e4715f92415a9258&scene=27)<br>
* 醫療領域基礎模型的發展機遇與挑戰: [website](https://arxiv.org/pdf/2404.03264)<br>
* SkinGPT-4 for dermatological diagnosis: [website](https://www.nature.com/articles/s41467-024-50043-3)<br>
* PneumoLLM for pneumoconiosis diagnosis: [website](https://www.sciencedirect.com/science/article/abs/pii/S1361841524001737)<br>
* BiomedGPT: [website](https://github.com/taokz/BiomedGPT)<br>
* LLaVA-Med: [website](https://github.com/microsoft/LLaVA-Med?tab=readme-ov-file)<br>
* RoboNurse-VLA: [website](https://robonurse-vla.github.io)<br>
* PathChat 哈佛醫學院 Faisal Mahmood 教授團隊的病理大模型。臨床上，病理被稱為診斷的金標準: [website](https://www.nature.com/articles/s41586-024-07618-3)<br>
* DeepDR-LLM 糖尿病視網膜病變 (DR) 的專科垂域多模態大模型: [website](https://www.nature.com/articles/s41591-024-03139-8)<br>
* VisionFM 通用眼科人工智慧的多模式多任務視覺基礎模型: [website](https://ai.nejm.org/doi/full/10.1056/AIoa2300221)<br>
* Medical-CXR-VQA 用於醫學視覺問答任務的大規模胸部 X 光資料集: [website](https://github.com/Holipori/Medical-CXR-VQA)<br>

#### 3.10.1.2 Medical Robotics - 醫療機器人
* 醫療機器人的五級自動化（醫療機器人領域行業共識），杨广中教授於 2017 年在 Science Robotics 上的論著: [Medical robotics—Regulatory, ethical, and legal considerations for increasing levels of autonomy](https://www.science.org/doi/pdf/10.1126/scirobotics.aam8638)<br>
* 醫療機器人的十年回顧（含醫療機器人的不同分類），杨广中教授在 Science Robotics 上的綜述文章：[A decade retrospective of medical robotics research from 2010 to 2020](https://www.science.org/doi/epdf/10.1126/scirobotics.abi8017)<br>
* 醫療具身智能的分級: [A Survey of Embodied AI in Healthcare: Techniques, Applications, and Opportunities](https://arxiv.org/pdf/2501.07468?)<br>
* Artificial intelligence meets medical robotics, 2023 年發表在 Science 正刊上的論著: [website](https://www.science.org/doi/abs/10.1126/science.adj3312)<br>
* 機器人手術：從理論到實踐的突破 (Nature Reviews Bioengineering): [Robotic surgery](https://www.nature.com/articles/s44222-025-00294-6)

* 醫療機器人的機器視覺
  * 3DGS 在腔鏡手術中的應用綜述: [website](https://arxiv.org/pdf/2408.04426)<br>
  * 香港中文大學任洪亮教授團隊在 Nature Reviews Electrical Engineering 上關於大型視覺模型 (LVM) 在手術機器人上的綜述 [website](https://www.nature.com/articles/s44287-025-00166-6)

* 達文西手術機器人是最為常用的外科手術機器人，對於這類機器人自主技能操作的研究最為廣泛
  * 達文西手術機器人研究套件 dVRK 介紹: [website](https://ieeexplore.ieee.org/abstract/document/9531355)<br>
  * 透過模仿學習在達文西機器人上學習外科手術操作任務 Surgical Robot Transformer (SRT): [website](https://surgical-robot-transformer.github.io/)<br>
  * Domain-specific Simulators - 手術機器人技能學習領域的模擬器
    * SurRoL: RL-Centered and dVRK Compatible Platform for Surgical Robot Learning [website](https://med-air.github.io/SurRoL/)<br>
    * Surgical Gym: A high-performance GPU-based platform for surgical robot learning (ICRA 2024, work in progress, based on NVIDIA Omniverse): [website](https://github.com/SamuelSchmidgall/SurgicalGym)<br>
    * ORBIT-Surgical: An Open-Simulation Framework for Learning Surgical Augmented Dexterity  (ICRA 2024, based on NVIDIA Omniverse): [website](https://orbit-surgical.github.io/)<br>
    * 縫合是手術機器人操作中的一個關鍵子任務，實現其自主化已有多項研究。關於自主縫合技能操作的綜述可參考: [website](https://link.springer.com/article/10.1007/s00464-024-10788-w)<br>

* 連續體和軟體手術機器人作為柔性醫療機器人的重要分支，憑藉其獨特的結構設計和材料特性，在微創介入診療領域展現出顯著優勢。它們能夠靈活進入人體狹窄腔體，實現精準操作，同時最大限度地減小手術創口，降低患者術後恢復時間及感染風險，為現代微創手術提供了創新性的技術解決方案。
  * 連續體機器人在醫療領域的應用 (Nabil Simaan; Howie Choset 等): [Continuum Robots for Medical Interventions](https://ieeexplore.ieee.org/abstract/document/9707607)<br>
  * 軟體手術機器人在微創介入手術中的應用 (Ka-wai Kwok; Kaspar Althoefer 等)： [Soft Robot-Assisted Minimally Invasive Surgery and Interventions: Advances and Outlook](https://ieeexplore.ieee.org/abstract/document/9765966/authors#authors)<br>
  * 血管介入手術機器人的具身智能（面向血管介入特定場景與任務的感知、決策、技能學習）：[Advancing Embodied Intelligence in Robotic-Assisted Endovascular Procedures: A Systematic Review of AI Solutions](https://arxiv.org/abs/2504.15327)
* 連續體和軟體機器人因其超冗餘自由度和高度非線性的結構特性，採用傳統的控制與感測方法構建正逆運動學方程時面臨顯著的計算複雜性和建模局限性。傳統方法難以精確描述其多自由度耦合運動及環境互動中的動態響應。為此，基於數據驅動的智能控制方法（如深度學習、強化學習及自適應控制演算法）成為解決這一問題的前沿方向。這些方法能夠透過大量資料訓練，高效學習系統的非線性映射關係，顯著提升運動控制的精度、自適應性和魯棒性，為複雜醫療場景下的機器人操作提供了更為可靠的技術支撐。
    * 什麼是軟體機器人？軟體機器人的具身智能定義: [知乎, by Ke WU from MBUZAI](https://www.zhihu.com/question/61637360/answer/92834447300?utm_psn=1870238291607040000)<br>
    * IROS 2024 大會 Program Chair 新加坡國立大學 Cecilia Laschi 教授的論著: [Learning-Based Control Strategies for Soft Robots: Theory, Achievements, and Future Challenges](https://ieeexplore.ieee.org/abstract/document/10136428)<br>
    * 軟體機器人中具身智能物理建模簡明指南（也是出自 NUS Cecilia 教授團隊）: [A concise guide to modelling the physics of embodied intelligence in soft robotics](https://inria.hal.science/hal-03921606/document)<br>
    * 數據驅動方法在軟體機器人建模與控制中的應用: [Data-driven methods applied to soft robot modeling and control: A review](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10477253)<br>

* 微納機器人技術是一類集成了微納米製造、生物工程和智能控制等多學科前沿技術的微型機器人系統。憑藉其微納米級的獨特尺寸、優異的生物相容性和精準的操控性能，這一前沿技術為現代醫學診療範式帶來了突破性創新。在精準診斷方面，微納機器人能夠深入人體微觀環境，實現細胞乃至分子水平的即時監測；在靶向治療領域，其可作為智能藥物載體，實現病灶部位的精準定位與可控釋放；在微創手術應用中，微納機器人系統為複雜外科手術提供了前所未有的精確操作平台。這些創新性應用不僅顯著提升了診療效率，更為攻克重大疾病提供了全新的技術途徑，推動著現代醫學向更精準、更微創、更智能的方向發展。
    * 微納機器人的機器學習 (CUHK 张立教授團隊在 Nature Machine Intelligence 上的論著): [Machine learning for micro- and nanorobots](https://www.nature.com/articles/s42256-024-00859-x)<br>

<section id="uav"></section>

### 3.10.2 UAV - 無人機
無人機的發展來源於：
1. 從外部感測設備保護發展至機載感測與計算；
2. 從遙控/預先編程發展至自主。

不同於 legged locomotion 和 manipulation，在無人機領域，data-driven 的方法與 model-based/modular 的方法在不同任務中的優勢不同，仍處於分庭抗禮的階段。這主要是因為無人機的模型與驅動模式較為簡單（如四旋翼的驅動機構只有四個電機），且傳統的無人機（即不具有操作設備）不會與環境產生互動，因此基於模型、優化和分層的方法，透過良好的狀態機/規則設計和高效的局部優化技術，仍能夠被賦予很強的性能。然而，無人機的難點在於其狀態估計（通常需要）、感知和底層驅動充滿噪聲，這是因為小型化無人機的負載能力十分有限以及其成本被盡可能壓低，因此在一些任務中 data-driven/端到端的方法展現出了遠超於傳統方法的性能。因此，以下對無人機 data-driven 資料介紹的同時會穿插其與傳統方法的對比，以便大家了解整個領域發展的動機。

總體而言，無人機的研究分為三個部分：
1. 技能實現/學習，例如避障、競速、大機動飛行/特技等；
2. 任務實現/學習，例如探索、重建、追蹤等；
3. 飛行機器人本體設計。

無人機工作的開原始碼並不多且良莠不齊，大部分需要透過論文學習。

### 3.10.2.1 技能實現/學習
- **支持 RL 的模擬器**
  
  無人機的模擬器普遍並不強大，並且幾乎沒有開源的 RL sim2real 項目。基於開原始碼需要較大的內容改動才能實現理想的 sim2real performance。
  - **AirSim** (https://microsoft.github.io/AirSim/)：基於 UE4 引擎，具有較為逼真動力學 transition 模擬。缺點是 UE4 底層功能較難修改並且運行速度較慢。
  - **Flightmare** (https://github.com/uzh-rpg/flightmare)：基於 Unity 渲染，CPU 並行動力學。
  - **AerialGym** (https://github.com/ntnu-arl/aerial_gym_simulator)：基於 IsaacSim，GPU 並行動力學。

- **經典技能代表性工作**

  我們主要介紹一些 data-driven 方法在經典任務上的應用。值得一提的是，以下的工作中，出現了一些擺脫了對 SLAM 系統和里程計依賴的方法（而無人機最初的興起正是依靠 SLAM/里程計系統的日益成熟），將成為無人機技能學習中有趣的進展方向。
  - **未知場景障礙物躲避**
    - Learning Monocular Reactive UAV Control in Cluttered Natural Environments. ICRA 2013, 卡內基梅隆大學 (CMU). 受自動駕駛發展啟發，第一個使用監督學習將圖像映射為離散上游控制指令的系統。
    - CAD2RL: Real Single-Image Flight without a Single Real Image. RSS 2017，柏克萊大學 (UCB). 第一個使用 sim2real RL，對單目 RGB 圖像進行大量 domain randomization，在長廊中輸出速度指令的系統。
    - DroNet: Learning to Fly by Driving. RAL 2018, 蘇黎世大學 (UZH). 利用自動假設資料集讓飛機輸出速度指令，程式碼開源 ( https://github.com/uzh-rpg/rpg_public_dronet )。
    - Learning High-Speed Flight in the Wild. SciRob 2021, 蘇黎世大學 (UZH). 使用 dagger 利用傳統軌跡規劃進行監督學習。文章 claim 網路推理的低延遲可以使未知環境中飛行速度更快。程式碼開源 ( https://github.com/uzh-rpg/agile_autonomy )。
    - Back to Newton's Laws: Learning Vision-based Agile Flight via Differentiable Physics, Arxiv 2024, 上海交通大學 (SJTU). 用 differentiable physics 提供的一階梯度做策略優化，不需要顯式的位置和速度估計。文章用低解析度深度圖，訓練避障比 RL 更高效，實現高速飛行。
    - [Flying on Point Clouds using Reinforcement Learning](https://arxiv.org/abs/2503.00496) [[Video](https://www.bilibili.com/video/BV1xeRpYnEYT)]. Arxiv 2025, 浙江大學 (ZJU). 使用機載雷達和 sim2real RL 實現自主避障。
    - 值得一提的是，作為無人機最常用的任務，避障現在最常用的還是傳統方法的系統如開源的 ego-planner ( https://github.com/ZJU-FAST-Lab/ego-planner )，由於這樣的方案已經足以勝任大部分場景（而不像四足的 MPC），因此在實際應用中比較少使用 data-driven 的方案。

  - **無人機競速**
    - Champion-level drone racing using deep reinforcement learning. Nature 23, 蘇黎世大學 (UZH). 用強化學習戰勝人類冠軍飛手，近幾年無人機領域影響力最高的文章，是 UZH RPG 實驗室多年來深厚工程積累的結果，其中的 RL 方案較為簡單直接。
    - Reaching the Limit in Autonomous Racing: Optimal Control versus Reinforcement Learning. SciRob 23, 蘇黎世大學 (UZH). 強化學習與最優控制方法競速飛行對比。
    - Demonstrating Agile Flight from Pixels without State Estimation. RSS 2024, 蘇黎世大學 (UZH). 使用視覺，不需要顯式狀態估計的現實世界競速 demo。
    - UZH 的 Perception and Robotics Group (RPG) 使用最優控制和 RL 的方法在競速上有諸多嘗試，使得無人機在固定軌道上達到最快飛行速度。

  - **大機動/特技飛行**
    - Deep Drone Acrobatics. RSS 2020, 蘇黎世大學 (UZH). 使用模仿學習，從視覺特徵點中學習 MPC 的軌跡追蹤，實現姿態劇烈變化的特技飛行。
    - [Whole-Body Control Through Narrow Gaps From Pixels to Action](https://arxiv.org/abs/2409.00895). ICRA 2025, 浙江大學 (ZJU). 使用強化學習實現視覺端到端窄縫穿越，不需要顯式的位置和速度估計，超越傳統方法性能。

- **經典任務實現代表性工作**
  - **追捕**
    - HOLA-Drone: Hypergraphic Open-ended Learning for Zero-Shot Multi-Drone Cooperative Pursuit. Arxiv 2024, University of Manchester.
    - Multi-UAV Pursuit-Evasion with Online Planning in Unknown Environments by Deep Reinforcement Learning. Arxiv 2024, 清華大學 (THU).
  - **探索**
    - Deep Reinforcement Learning-based Large-scale Robot Exploration, RAL 2024, 新加坡國立大學 (NUS). 利用注意力機制學習不同空間尺度的依賴關係，對未知區域進行隱式預測，優化已知空間探索策略，提高探索效率。
    - ARiADNE: A Reinforcement learning approach using Attention-based Deep Networks for Exploration, ICRA 2023, 新加坡國立大學 (NUS). 學習已知不同區域在多個空間尺度上的相互依賴關係，並隱式預測探索這些區域可能獲得的潛在收益。這使得代理能夠安排行動順序，以平衡在已知區域對地圖進行開發/細化與探索新區域之間的自然權衡。
    - DARE: Diffusion Policy for Autonomous Robot Exploration. ICRA 2025, 新加坡國立大學 (NUS). DARE 方法利用 self-attention 學習地圖空間資訊，並透過 diffusion 生成通往未知區域的軌跡，以提高自主機器人的探索效率。

### 3.10.2.2 無人機硬體平台搭建
手搓一個遙控器操控的穿越機不是一個很難的事情，網上有很多愛好者分享教程。但想搭建一個具有自主導航功能的無人機並非易事，是一個系統工程，這裡推薦浙大 FAST-lab 開源的教程：

- [從 0 製作自主空中機器人](https://www.bilibili.com/video/BV1WZ4y167me)

### 3.10.2.3 新構型無人機設計
除了常規用於航拍，環境探索的四旋翼無人機，想讓無人機具備更多能力，應用於更廣泛的具身智能場景，除了演算法上的創新外，也需要在硬體層面對無人機的構型進行創新設計。

- **空中機械臂 (Aerial Manipulator)** 

    空中機械臂，也叫空中操作無人機，兼具無人機的快速空間移動能力和機械臂的精確操縱能力，是具身智能的一種理想載體。西湖大學赵世钰老師組在知乎上有一系列文章介紹：

    - [空中作業機器人，下一代無人機技術？](https://zhuanlan.zhihu.com/p/442331197)
    - [空中作業機器人—沒那麼簡單！](https://zhuanlan.zhihu.com/p/487203757)
    - [空中操作機器人：如何設計機械臂？](https://zhuanlan.zhihu.com/p/509669272)
    - [空中作業機器人都有哪些應用？](https://zhuanlan.zhihu.com/p/517471760)

    * 代表性工作
        * [Past, Present, and Future of Aerial Robotic Manipulators](https://ieeexplore.ieee.org/document/9462539). TRO 2022. 空中機械臂領域目前最全的綜述文章，入門了解必備。
        * [Millimeter-Level Pick and Peg-in-Hole Task Achieved by Aerial Manipulator](https://ieeexplore.ieee.org/abstract/document/10339889). TRO 2023, 北京航空航天大學 (BHU). 使用四旋翼加串聯機械臂實現毫米精度 peg-in-pole 任務。
        * [NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122) [[Video](https://www.bilibili.com/video/BV16Zt5eBEPW)]. ICRA 2025, 中山大學 (SYU). 使用四旋翼加並聯機械臂實現毫米精度抓取。
        * [A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7) [[Video](https://www.bilibili.com/video/BV1CC4y1Z7xS)]. JIRS 2024, 北京航空航天大學 (BHU). 用空中機械臂做一些有趣的應用，比如抓雞蛋、開門等等。

- **全驅動無人機 (Fully-Actuated UAV)**

    常見的四旋翼無人機具有欠驅動特性，即位置與姿態耦合。而具有位置姿態解耦控制的全驅動無人機，理論上更適合作為空中操作的飛行平台。

    * 代表性工作
        * [Fully Actuated Multirotor UAVs: A Literature Review](https://ieeexplore.ieee.org/document/8978486/?arnumber=8978486). RAM 2020. 全驅動無人機領域目前最全的綜述文章，入門了解必備。
        * [Design, modeling and control of an omni-directional aerial vehicle](https://ieeexplore.ieee.org/document/7487497). ICRA 2016, 蘇黎世聯邦理工學院 (ETH). 第一個實現全向飛行的固定傾角全驅動無人機。
        * [The Voliro omniorientational hexacopter: An agile and maneuverable tiltable-rotor aerial vehicle](https://ieeexplore.ieee.org/document/8485627). RAM 2018, 蘇黎世聯邦理工學院 (ETH). 第一個實現全向飛行的可變傾角全驅動無人機 
        * [FLOAT Drone: A Fully-actuated Coaxial Aerial Robot for Close-Proximity Operations](https://arxiv.org/abs/2503.00785) [[Website](https://zju-jxlin.github.io/float-drone.github.io/)]. Arxiv 2025, 浙江大學 (ZJU). 適合近端作業的小尺寸全驅動無人機。

- **可變形無人機 (Deformable UAV)**

    除了透過往飛行平台上安裝機械臂，讓無人機本體可以變形，也是使其實現更多功能的一種方法。

    * 代表性工作
        * [Design, Modeling, and Control of an Aerial Robot DRAGON: A Dual-Rotor-Embedded Multilink Robot With the Ability of Multi-Degree-of-Freedom Aerial Transformation](https://ieeexplore.ieee.org/document/8258850). RAL 2018，東京大學. Best paper award on UAV in ICRA 2018，多關節可變形無人機。
        * [The Foldable Drone: A Morphing Quadrotor That Can Squeeze and Fly](https://ieeexplore.ieee.org/document/8567932?arnumber=8567932). RAL 2019, 蘇黎世大學 (UZH). 四旋翼每個機臂上安裝一個舵機，實現機體變形飛行。
        * [Ring-Rotor: A Novel Retractable Ring-Shaped Quadrotor With Aerial Grasping and Transportation Capability](https://ieeexplore.ieee.org/document/10044964) [[Video](https://www.bilibili.com/video/BV1gY4y1K723)]. RAL 2023, 浙江大學 (ZJU). 一種可變形的環形四旋翼，可用於抓取、運輸等任務。
        * [Design and Control of a Passively Morphing Quadcopter](https://ieeexplore.ieee.org/document/8794373) [[Video](https://www.youtube.com/watch?v=MSvoQT__c9U)]. ICRA 2019, 柏克萊大學 (UCB). 一種被動變形的四旋翼無人機。

- **多模態無人機 (Multi-Modal UAV)**

    無人機與地面機器人相比，其優勢在於三維空間運動能力，劣勢則是續航差。因此一些研究關注多模態無人機的構型設計、運動控制以及自主導航。多模態無人機具備空中、地面、水下等多域運動能力。這不僅能解決無人機的續航問題，也能讓無人機具有更多應用潛力。

    * 代表性工作
        * [A bipedal walking robot that can fly, slackline, and skateboard](https://www.science.org/doi/10.1126/scirobotics.abf8136). SR 2021, Caltech. 多模態空地足式機器人。
        * [Multi-Modal Mobility Morphobot (M4) with appendage repurposing for locomotion plasticity enhancement](https://www.nature.com/articles/s41467-023-39018-y). NC 2023, Northeastern University. 具有很多種運動模式的多模態無人機。
        * [Skater: A Novel Bi-Modal Bi-Copter Robot for Adaptive Locomotion in Air and Diverse Terrain](https://ieeexplore.ieee.org/document/10538378) [[Video](https://www.bilibili.com/video/BV1y2421M7HM)]. RAL 2024, 浙江大學 (ZJU). 適應多樣地形的多模態空地雙旋翼無人機。
        * [Autonomous and Adaptive Navigation for Terrestrial-Aerial Bimodal Vehicles](https://ieeexplore.ieee.org/document/9691888). RAL 2022, 浙江大學 (ZJU). 實現空地多模態無人機的自主導航。


<section id="ad"></section>

### 3.10.3 Autonomous Driving - 自動駕駛

[自動駕駛之心](https://www.zdjszx.com/)（也有個微信公眾號）

自動駕駛被稱為「最小的具身智能驗證場景」，這是因為它在具身智能的框架中，具備完整的感知、決策和行動閉環，但任務目標明確、物理互動簡單、場景複雜性相對較低。作為一個技術驗證場景，自動駕駛既能體現具身智能的核心特性，又為更複雜的具身智能任務提供了技術積累和理論支持。

#### Model：自動駕駛模擬

[生成式模擬為具身智能釋放無限靈感](https://bydrug.pharmcube.com/news/detail/80b67b2227879864af934e5f81835776)

自動駕駛模擬是自動駕駛技術開發中不可或缺的一部分。它透過提供安全、高效、可控的測試環境，不僅降低了研發成本和風險，還加速了技術的迭代和規模化部署。同時，模擬能夠覆蓋大量現實中難以復現的場景，為自動駕駛系統的安全性、可靠性和泛化能力提供了重要保障。

1. 3D/4D 場景重建

* 經典工作：NSG, MARS, StreetGaussians, OmniRe
  * **NSG**: CVPR 2021, [github](https://github.com/princeton-computational-imaging/neural-scene-graphs), [arxiv](https://arxiv.org/abs/2011.10379), [paper](https://openaccess.thecvf.com/content/CVPR2021/html/Ost_Neural_Scene_Graphs_for_Dynamic_Scenes_CVPR_2021_paper.html)
  * **MARS**: [github](https://open-air-sun.github.io/mars/), [arxiv](https://arxiv.org/abs/2307.15058)
  * **StreetGaussians**: [github](https://github.com/zju3dv/street_gaussians), [arxiv](https://arxiv.org/abs/2401.01339)
  * **OmniRe**: ICLR 2025 Spotlight, [demo page](https://ziyc.github.io/omnire), [github](https://github.com/ziyc/drivestudio), [arxiv](https://arxiv.org/abs/2408.16760)

2. 場景可控生成（世界模型）

* 經典工作：GAIA-1, GenAD（OpenDV 資料集）, Vista, SCP-Diff, MagicDrive -> MagicDriveDiT, UniScene, VaVAM
  * **GAIA-1**: [demo page](https://wayve.ai/thinking/introducing-gaia1/), [arxiv](https://arxiv.org/abs/2309.17080)
  * **GenAD**: CVPR 2024 Highlight, OpenDV 資料集, [github](https://github.com/OpenDriveLab/DriveAGI?tab=readme-ov-file#opendv), [arxiv](https://arxiv.org/abs/2403.09630)
  * **Vista**: NeurIPS 2025, [demo page](https://opendrivelab.com/Vista), [github](https://github.com/OpenDriveLab/Vista), [arxiv](https://arxiv.org/abs/2405.17398)
  * **SCP-Diff**: [demo page](https://air-discover.github.io/SCP-Diff/), [github](https://github.com/AIR-DISCOVER/SCP-Diff-Toolkit), [arxiv](https://arxiv.org/abs/2403.09638)
  * **MagicDrive** -> MagicDriveDiT: [demo page](https://gaoruiyuan.com/magicdrive-v2/), [arxiv](https://arxiv.org/abs/2411.13807)
  * **UniScene**: CVPR 2025, [demo page](https://arlo0o.github.io/uniscene/),  [arxiv](https://arxiv.org/abs/2412.05435)
  * **VaVAM**: [github](https://github.com/valeoai/VideoActionModel)


#### Policy：自動駕駛策略

1. 從模組化到端到端

* 經典的模組化管線中，每個模型作為一個獨立的組件，負責對應的特定任務（3D 目標檢測與追蹤 & BEV 建圖 -> 目標運動預測 -> 軌跡規劃），這種設計已逐漸被端到端模型所取代。

[End-to-end Autonomous Driving: Challenges and Frontiers](https://arxiv.org/pdf/2306.16927)

2. 快系統與慢系統並行

[理想端到端-VLM 雙系統](https://www.sohu.com/a/801987742_258768)

* 快系統經典論文：UniAD (CVPR 2023 Best Paper), VAD, SparseDrive, DiffusionDrive
  * **UniAD**: CVPR 2023 Best Paper, [github](https://github.com/OpenDriveLab/UniAD), [arxiv](https://arxiv.org/abs/2212.10156)
  * **VAD**: ICCV 2023, [github](https://github.com/hustvl/VAD), [arxiv](https://arxiv.org/abs/2303.12077)
  * **SparseDrive**: [github](https://github.com/swc-17/SparseDrive), [arxiv](https://arxiv.org/abs/2405.19620)
  * **DiffusionDrive**: CVPR 2025, [github](https://github.com/hustvl/DiffusionDrive), [arxiv](https://arxiv.org/abs/2411.15139)
  * 快系統的 Scale up 特性探究：https://arxiv.org/pdf/2412.02689
* 慢系統經典論文：DriveVLM, EMMA
  * **DriveVLM**: CoRL 2024, [arxiv](https://arxiv.org/abs/2402.12289)
  * **EMMA**: [arxiv](https://arxiv.org/abs/2410.23262)
    - **[Open-EMMA](https://github.com/taco-group/OpenEMMA)** 是 EMMA 的一個開源實現，提供了一個用於自動駕駛車輛運動規劃的端到端框架。


#### 未來發展方向

[AIR ApolloFM 技術全解讀](https://air.tsinghua.edu.cn/info/1007/2258.htm)

<section id="control"></section>

## 4. Control and Robotics - 控制論與機器人學基礎
**經典課程**
  - [video](https://www.bilibili.com/video/BV1GJ411k7fE) 美國西北大學 現代機器人 Modern Robotics：這門課側重於基礎的機器人理論，涉及的概念有**笛卡爾座標系**，**關節座標系**，**自由度**，**齊次旋轉矩陣**，**正運動學 (FK)**，**逆運動學 (IK)** 等等，適合零基礎入門。
  - [video](https://www.bilibili.com/video/BV1h7411A7B9) 加州柏克萊大學 高級機器人技術 by Pieter Abbeel：這門課是機器人的進階課程，適合在學習完「現代機器人 Modern Robotics」或者有相應基礎後進一步學習。涉及的部分有**馬可夫決策過程**，**LQR 控制**，**在約束條件下的最優化問題**，**基於最優化的控制**，**運動規劃**，**卡爾曼濾波**，**模仿學習**，**強化學習**，**Sim2Real** 等等。課程中還涉及了很多實操演示，有助於進一步了解理論在真實世界中的應用。
## 4.1. 控制理論基礎

### 4.1.1 經典控制原理
* 理解系統、回饋
* 時域與頻域分析
* 傳遞函數
* 理解前饋控制、回饋控制
* **PID 控制**：[CSDN](https://blog.csdn.net/name_longming/article/details/115093338) [BiliBili](https://www.bilibili.com/video/BV1B54y1V7hp)

### 4.1.2 現代控制理論 (線性系統控制)
* Modern Control Systems (14th edition), Robert. H. Bishop, Richard. C, Dorf. z: [Book](http://103.203.175.90:81/fdScript/RootOfEBooks/E%20Book%20collection%20-%202024/EEE/Modern_control_systems_Robert_H_Bishop_Richard_C_Dorf_z_lib_org.pdf#page=1.00&gsr=0)
* 狀態方程
* 狀態回饋與最優控制
* **LQR 控制** [BiliBili](https://www.bilibili.com/video/BV1Ng4y1V7JQ)
* **卡內基梅隆大學 (CMU) 16-745 Optimal Control** 涵蓋從數值優化到最優化理論, [Website](https://optimalcontrol.ri.cmu.edu/), [Youtube](https://www.youtube.com/playlist?list=PLZnJoM76RM6IAJfMXd1PgGNXn3dxhkVgI), [Bilibili](https://space.bilibili.com/504273533/lists/6271656?type=season)

### 4.1.3 先進控制技術
* 魯棒控制
* 徹底搞懂阻抗控制、導納控制、力位混合控制: [CSDN](https://blog.csdn.net/a735148617/article/details/108564836)
* **模型預測控制 MPC**
* 智能控制 (包含基於深度學習的控制)

## 4.2. 機器人學導論

### 4.2.1 推薦材料
* 現代機器人學（非常推薦！）[video](https://www.youtube.com/watch?v=29LhXWjn7Pc&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx&index=11)
* 經典教材
  * 《機構學與機器人學的幾何基礎與旋量代數》 戴建生院士 著
  * 《現代機器人學：機構、規劃與控制》凱文·M. 林奇, 朴鐘宇 著
  * 《機器人學的現代數學理論基礎》丁希侖 著

### 4.2.2 機器人運動學 (Kinematics) 與動力學 (Dynamics)
1. 機器人運動學
> 想要快速了解什麼是 IK FK 的同學可以看這個 7 分鐘的短片，可以對此建立一個粗略的認知：[BiliBili](https://www.bilibili.com/video/BV18E411v7F9)<br>
> 較為簡單的過一遍 IK 和 FK 的原理可以看這個：[CSDN](https://blog.csdn.net/Dwzsa/article/details/142386529?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ECtr-3-142386529-blog-109314877.235%5Ev43%5Epc_blog_bottom_relevance_base7&utm_relevant_index=6) 

* IK (Inverse Kinematics) 逆運動學
  * 較為詳細的影片課
    * [BiliBili IK(1)](https://www.bilibili.com/video/BV1PD4y1t7xP)
    * [BiliBili IK(2)](https://www.bilibili.com/video/BV1Tt4y1T79Z)
  * 文字教學
    * [Book](https://motion.cs.illinois.edu/RoboticSystems/InverseKinematics.html)，較為詳細的 IK 理論

* FK (Forward Kinematics) 正運動學
  * 較為詳細的影片課
    * [BiliBili FK(1)](https://www.bilibili.com/video/BV1Ve4y127Uf)
    * [BiliBili FK(2)](https://www.bilibili.com/video/BV1a14y157uL)

2. 機器人動力學（**重要！！！**）
* 理解斜對稱矩陣，Twist 和 Exponential of a twist，旋量代數

### 4.2.3 里程計與同步定位與建圖 (Odometry & SLAM)
里程計 (Odometry) 用於為機器人即時提供定位，里程計常常基於擴展卡爾曼濾波 (EKF) 實現，融合來自慣性測量單元 (IMU)、相機、雷射雷達、碼盤、毫米波雷達、超寬頻 (UWB)、光流感測器等等各種常用於機器人位姿感知的感測器之中的多種觀測，以較高的頻率實現對機器人位姿的估計。

里程計中最常見的是視覺慣性里程計 (VIO) 和雷射慣性里程計 (LIO)，以及最近新興的一些用 4D 毫米波雷達作為主要感測器的方法，其中比較經典的工作包括 VINS 系列 [VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)，[ORB-SLAM](https://github.com/UZ-SLAMLab/ORB_SLAM3)，[VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)，[LOAM](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf)，[FAST-LIO](https://github.com/hku-mars/FAST_LIO) 等等。此外還有融合了 IMU、相機和雷射感測器的里程計 [FAST-LIVO](https://github.com/hku-mars/FAST-LIVO2) 系列等。

SLAM (Simultaneous Localization And Mapping) 在定位的同時完成地圖的構建，使得回環 (Loop Closure) 檢測成為可能，回環檢測的存在使得當機器人重新訪問到某個位置時可以修正一部分的累計誤差，提高在長時間作業時的定位精度。SLAM 的實現主要有 filter-based 和 optimization-based 兩種，實現中一般又分前端和後端，基於不同感測器的 SLAM 又各有其特點，在這裡提供一些學習資源，主要是書籍：

* [SLAM Handbook](https://github.com/SLAM-Handbook-contributors/slam-handbook-public-release)
* [Past, Present, and Future of Simultaneous Localization And Mapping: Towards the Robust-Perception Age](https://arxiv.org/abs/1606.05830)：SLAM 領域的經典綜述
* 高翔老師的[《視覺 SLAM 十四講》](https://github.com/gaoxiang12/slambook2)
* 高翔老師的[《自動駕駛與機器人的 SLAM 技術》](https://github.com/gaoxiang12/slam_in_autonomous_driving)

此外，SLAM 也有端到端的實現 [DROID-SLAM](https://arxiv.org/abs/2108.10869)。

其他關於 SLAM 的思考可以參考 [awesome-and-novel-works-in-slam](https://github.com/runjtu/awesome-and-novel-works-in-slam)

### 4.2.4 雜項 Misc

* ROS 基礎：
  * 具身智能 ROS1 基礎：[website](http://www.autolabor.com.cn/book/ROSTutorials/)
  * 具身智能 ROS2 基礎：[website](https://zhangzhiwei-zzw.github.io/ROS2%E5%AD%A6%E4%B9%A0/ROS2/)
  * ROS2 Humble 3 小時入門教程：[ROS2 Humble Crash Course from Open Robotics Discourse](https://discourse.openrobotics.org/t/ros2-humble-3h-tutorial-for-beginners/28500/)
  * Open Robotics 官網：[Open Robotics](https://openrobotics.org/) 是 ROS、Gazebo 和 Open-RMF 等開源機器人軟體平台背後的組織，官網提供 ROS / Gazebo / Open-RMF 的官方入口、文件與社群動態，適合作為 ROS 生態的總入口。

* 常用的庫 
  * cuRobo：[cuRobo](https://curobo.org/)，cuRobo 是 Nvidia 的一個利用 CUDA 加速的機器人庫，提供了一套高效的機器人演算法，主要透過並行計算顯著提升性能，包括但不限於 IK、碰撞檢測、路徑規劃等。
  * IKFast：[IKFast](https://moveit.github.io/moveit_tutorials/doc/ikfast/ikfast_tutorial.html)，經典 IK 庫。
  * mplib：[mplib](https://github.com/haosulab/mplib)，Maniskill Benchmark 以及 Sapien 模擬平台的 IK 庫。
* ROS 多感測器時間戳同步：[website](https://blog.csdn.net/qq_43495930/article/details/125649446)
* 動手實踐 LeRobot SO-100：[website](https://huggingface.co/lerobot)


<section id="hardware"></section>

# 5. Hardware - 硬體

> 具身智能硬體方面涵蓋多個技術棧，如嵌入式軟硬體設計、機械設計、機器人系統設計，這部分知識比較繁雜，適合想要專注此方向的人。
> 關於硬體部分的學習，最好從實踐出發！

<section id="embedded"></section>

## 5.1 Embedded - 嵌入式
* 嵌入式學習路線：[CSDN](https://blog.csdn.net/wangshuaiwsws95/article/details/107830452)
* 51 單晶片：[BiliBili](https://www.bilibili.com/video/BV1Mb411e7re)，經典江科大自動協出品
* Stm32 單晶片：[BiliBili](https://www.bilibili.com/video/BV1th411z7sn)，經典江科大自動協出品
* Stm32 電機驅動：[BiliBili](https://www.bilibili.com/video/BV1AZ4y1V7wt)，野火
* 野火 Stm32 標準庫：[BiliBili](https://www.bilibili.com/video/BV1yW411Y7Gw)，野火
* 正點原子 Stm32：[BiliBili](https://www.bilibili.com/video/BV1Lx411Z7Qa)，正點原子
* 韋東山嵌入式 Linux：[BiliBili](https://www.bilibili.com/video/BV1w4411B7a4)，韋東山

<section id="mechanical"></section>

## 5.2 Mechanical Design - 機械設計

* SolidWorks 教學：[BiliBili](https://www.bilibili.com/video/BV1iw411Z7HZ)
* URDF 生成：[CSDN](https://blog.csdn.net/weixin_45168199/article/details/105755388)，指導如何透過 SolidWorks 裝配體出發生成機器人 URDF 檔案。
  
<section id="robosystem"></section>

## 5.3 Robot System Design - 機器人系統設計

* 《機器人學簡介》，來自 [2] 做的高品質教材：[PDF](./files/%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%AD%A6%E7%AE%80%E4%BB%8B.pdf)
* 《機器人系統教材》：[website](https://motion.cs.illinois.edu/RoboticSystems/)


<section id="sensors"></section>

## 5.4 Sensors - 感測器
### 5.4.1 深度相機

RealSense，[RealSense Ros 開發套件](https://github.com/IntelRealSense/realsense-ros/tree/ros1-legacy)

<section id="tactile"></section>

## 5.5 Tactile Sensing - 觸覺感知

### 1. 視觸覺感測器 (Vision-Based Tactile Sensors)


視觸覺感測器透過攝像頭捕捉觸覺資訊，將觸摸表面變形映射為視覺數據，以估計接觸力、形變等資訊。其設計涉及 **感測器形狀** (影響接觸範圍與適應性)、**標記點設置** (追蹤表面形變，提高解析度)、**材料選擇** (如矽膠或彈性體，提高靈敏度) 以及 **光照與攝像系統** (增強視覺訊號品質)。

* **優點**：提供高解析度觸覺資訊、非侵入式感知、不影響物體表面特性，並且可與視覺系統整合，提高多模態感知能力。  
* **缺點**：計算量大，依賴視覺處理和機器學習；易受環境光影響；光學設計複雜，封裝和耐用性受限。

 **參考文獻綜述**：寫得非常詳細，分別是演算法和結構設計
- 演算法：*[When Vision Meets Touch: A Contemporary Review for Visuotactile Sensors From the Signal Processing Perspective
](https://ieeexplore.ieee.org/document/10563188)*
- 結構：*[On the Design and Development of Vision-Based Tactile Sensors](https://link.springer.com/article/10.1007/s10846-021-01431-0)*

### 2. 電子皮膚 (Electronic Skin)

觸覺感知的路徑主要就是這兩類。電子皮膚模擬人類皮膚的觸覺能力，通常採用柔性電子材料 (如壓力感測薄膜、奈米感測器網路等) 來感知外界壓力、溫度和形變，使機器人具備更接近生物的觸覺感知能力。

* **優點**：電子皮膚可 **大面積覆蓋** 機器人表面，實現全身觸覺感知；具有 **高靈敏度**，能夠檢測微小的力變化，實現精準回饋；同時 **可伸縮性** 使其適應複雜表面，提高耐久性。
* **缺點**：電子皮膚的 **製造複雜**，材料和工藝要求高，成本較高；**數據處理挑戰**，大規模觸覺數據需要高效的計算與存儲方案；此外，**穩定性問題** 可能導致長期使用後靈敏度下降，影響可靠性。


 **參考文獻綜述**：*[Toward an AI Era: Advances in Electronic Skins](https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00049)*

### 3. 觸覺感知的應用和演算法 (視觸覺)

* 3.1 姿態估計 (Pose Estimation)
  * 估計 in hand 物體姿態
    * *[3D Shape Perception from Monocular Vision, Touch, and Shape Priors](https://arxiv.org/abs/1808.03247)*
  * in scene
    * *[Fast Model-Based Contact Patch and Pose Estimation for Highly Deformable Dense-Geometry Tactile Sensors](https://ieeexplore.ieee.org/document/8936859)*

* 3.2 物體分類 (Classification)
  * 區分不同液體、材料或透明物體。
    * *[Understanding Dynamic Tactile Sensing for Liquid Property Estimation](https://arxiv.org/abs/2205.08771)*
    * *[Multimode Fusion Perception for Transparent Glass Recognition](https://www.semanticscholar.org/paper/Multimode-fusion-perception-for-transparent-glass-Zhang-Shan/90109f2eabba717d152a599fc8d8d5a3677c85e5)*

* 3.3 觸覺操控 (Manipulation)
  * 物體裝配
    * *[Active Extrinsic Contact Sensing: Application to General Peg-in-Hole Insertion](https://ieeexplore.ieee.org/abstract/document/9812017)*
    * *[Building a Library of Tactile Skills Based on Fingervision](https://ieeexplore.ieee.org/abstract/document/9035000)*
  * 線纜整理
    * *[Cable Manipulation with a Tactile-Reactive Gripper](https://arxiv.org/abs/1910.02860)*
  * 精細手部操作
    * *[Manipulation by Feel: Touch-Based Control with Deep Predictive Models](https://arxiv.org/abs/1903.04128)*
    * *[NeuralFeels with Neural Fields: Visuotactile Perception for In-Hand Manipulation](https://www.science.org/doi/10.1126/scirobotics.adl0628)*

* 3.4 觸覺大模型 (Large Tactile Models)
  * 以統一多模態觸覺表示，提高通用性。
    * *[Binding Touch to Everything: Learning Unified Multimodal Tactile Representations](https://openaccess.thecvf.com/content/CVPR2024/papers/Yang_Binding_Touch_to_Everything_Learning_Unified_Multimodal_Tactile_Representations_CVPR_2024_paper.pdf)*

### 4. 感測器購買

市面上有一些成熟的視觸覺感測器可供選擇 🔗 **[GelSight 官網](https://gelsight.com/)**

<section id="companies"></section>

## 5.6 Companies - 公司

| 公司 | 主營產品 | Others |
|-------|------|------|
| [松灵AgileX](https://www.agilex.ai/) | [pipper 六軸機械臂](https://www.agilex.ai/chassis/16)<br> [PIKA 數採方案](https://www.agilex.ai/chassis/22)<br>[Cobot Magic 雙臂遙操作平台](https://www.agilex.ai/chassis/27)<br>移動底盤| 面向教育科研
| [宇树Unitree](https://www.unitree.com/cn) | [四足機器人開發指南](https://www.yuque.com/ironfatty/nly1un/luo9gb)<br>[Go2 機器狗](https://www.unitree.com/cn/go2)<br>[AlienGo 機器狗](https://www.yuque.com/ironfatty/nly1un/dqcz3u)<br>[通用人形 H1](https://www.unitree.com/cn/h1)<br>[通用人形 G1](https://www.unitree.com/cn/g1)<br> | 許多產出使用宇樹的機器人作為硬體基礎
| [方舟无限ARX](https://www.arx-x.com/?product/) | [X5 機械臂](https://www.arx-x.com/?product/21.html)<br>[X7 雙臂平台](https://www.arx-x.com/?product/23.html)<br>[R5 機械臂](https://www.arx-x.com/?product/22.html)  | 適合複現很多經典的工作，例如 [aloha](https://mobile-aloha.github.io/cn.html)<br>[RoboTwin 松靈底盤 + 方舟臂](https://github.com/TianxingChen/RoboTwi)
| [波士顿动力](https://bostondynamics.com/)  | [spot 機器狗](https://bostondynamics.com/products/spot/)<br>[Atlas 通用人形](https://bostondynamics.com/atlas/)  | 具身智能本體製造商，從液壓驅動轉向電機驅動 |
| [灵心巧手](https://www.linkerbot.cn/index) | [Linker Hand L30（健繩驅動）](https://www.linkerbot.cn/product?page=L30)<br>[Linker Hand L20（連桿驅動）](https://www.linkerbot.cn/product?page=L20) | 主攻各類靈巧手 |
| [灵巧智能DexRobot](https://www.dex-robot.com/)| [Dexhand 021 靈巧手](https://www.dex-robot.com/productionDexhand) | 19 自由度量產靈巧手 |
| [银河通用](https://www.galbot.com/about) | [GALBOT G1](https://www.galbot.com/g1) | 專注於具身智能多模態大模型通用機器人研發 |
| [星海图Galaxea](https://galaxea.ai/) | [A1 六軸機械臂](https://galaxea.ai/A1)<br>[R1-Pro 仿人形機器人](https://galaxea.ai/R1-Pro) | 軟硬體產品均自主研發，專注於打造「一腦多型」 |
| [World Labs](https://www.worldlabs.ai/) | | 專注於空間智能，致力於打造大型世界模型 (LWM)，以感知、生成並與 3D 世界進行交互。[相關介紹](https://mp.weixin.qq.com/mp/wappoc_appmsgcaptcha?poc_token=HEH5X2ejkAoWy1ZXj8DlZO_Y2Q7PsYX-3ID-rfr5&target_url=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fi58_yTFtt904haKezJgr1Q) |
| [星动纪元](https://www.robotera.com) | [Star1 人形](https://www.robotera.com/goods/1.html)<br> [XHAND1 靈巧手](https://www.robotera.com/goods/2.html) | |
| [加速进化](https://boosterobotics.com/zh/) | [Booster T1 人形](https://boosterobotics.com/zh/store/)|  |
| [人形机器人（上海）有限公司](https://www.openloong.net/) | [青龍機器人](https://www.openloong.org.cn/cn) | 全尺寸通用人形機器人，提供開源硬體設計圖紙、軟體框架代碼、演算法包和全鏈模擬工具。 |
| [云深处科技](https://www.deeprobotics.cn/) |  [絕影 X30 四足機器人](https://www.deeprobotics.cn/robot/index/product3.html)<br> [Dr.01 人形機器人](https://www.deeprobotics.cn/robot/index/humanoid.html) |  |
| [松应科技](http://www.orca3d.cn/) |  | 具身智能模擬平台供應商 |
| [光轮智能](https://lightwheel.net/) |  | 具身智能數據平台 |
| [智元机器人](https://www.zhiyuan-robot.com/about/167.html) | [遠征 A2 人形機器人](https://www.zhiyuan-robot.com/products/A2)<br>[遠征 A2-W 輪式人形](https://www.zhiyuan-robot.com/products/A2_W)<br>[靈犀 X1 人形機器人](https://www.zhiyuan-robot.com/products/X1)<br>[精靈 G1 輪式人形](https://www.zhiyuan-robot.com/products/A2_D)|  |
| [Nvidia](https://www.nvidia.cn/industries/robotics/) |  | 具身智能基建公司 |
| [求之科技](https://airbots.online/)  | [TOK2 移動主從臂平台](https://airbots.online/zh/tok)<br>[MMK2 移動升降雙臂平台](https://airbots.online/zh/mmk2)<br> Play 六軸機械臂|  |
| [穹彻智能](https://www.noematrix.ai/) | | |
| [优必选](https://www.ubtrobot.com/cn/about/companyProfile) | | |
| [具身风暴](https://www.robotstorm.tech) | | 落地具身智能通用按摩機器人 |
| [众擎机器人](https://engineai.com.cn/) |[SE 01](https://engineai.com.cn/product_one)<br>[PM 01](https://engineai.com.cn/product_fore)| |
| [魔法原子](https://www.magiclab.top/) |[MagicBot](https://www.magiclab.top/human)<br>[MagicDog](https://www.magiclab.top/dog)| |
| [帕西尼](https://www.paxini.com/) |[PX-6AX GEN2 觸覺感測器](https://www.paxini.com/ax/gen2)<br>[DexH13 GEN2 靈巧手](https://www.paxini.com/dex/gen2)<br>[TORA-ONE 人形機器人](https://www.paxini.com/robot) | |
<section id="software"></section>

# 6. Software - 軟體

<section id="simulators"></section>

## 6.1 Simulators 模擬器
常見模擬器 wiki：[wiki](https://simulately.wiki/)
| 模擬器 | 對應基準集 |
|-------|------|
| [IsaacGym](https://developer.nvidia.com/isaac-gym) | [legged gym](https://github.com/leggedrobotics/legged_gym)<br>[parkour（包括蒸餾以及真機部署）](https://github.com/ZiwenZhuang/parkour)<br>[extreme-parkour](https://github.com/chengxuxin/extreme-parkour) |
| [IsaacSim](https://developer.nvidia.com/isaac/sim) | [BEHAVIOR-1K（可跨平台）](https://behavior.stanford.edu/behavior-1k) + [omniGibson（工具鏈）](https://behavior.stanford.edu/omnigibson/)<br>[ARNOLD](https://arnold-benchmark.github.io/) <br> [GarmentLab](https://garmentlab.github.io/) and [DexGarmentLab](https://wayrise.github.io/DexGarmentLab/) |
| [MuJoCo](https://mujoco.org/) | [robosuite](https://robosuite.ai/docs/overview.html) + [robomimic（工具鏈）](https://robomimic.github.io/)<br>[LIBERO](https://libero-project.github.io/main.html)<br>[MetaWorld](https://meta-world.github.io/)<br>[Gymnasium-Robotics (Fetch; Shadow Dexterous Hand; Maze; Adroit Hand; Franka Kitchen; MaMuJoCo)](https://robotics.farama.org/)<br>[RoboCasa](https://github.com/robocasa/robocasa?tab=readme-ov-file)<br>[RoboHive](https://github.com/vikashplus/robohive) |
| [Sapien](https://sapien.ucsd.edu/) | [ManiSkill](https://maniskill.readthedocs.io/en/latest/index.html)<br>[RoboTwin](https://github.com/TianxingChen/RoboTwin) |
| [CoppeliaSim](https://www.coppeliarobotics.com/) | [RLBench](https://github.com/stepjam/RLBench)<br>[PerAct2](https://bimanual.github.io/)<br>[COLOSSEUM](https://robot-colosseum.github.io/) |
| [PyBullet](https://pybullet.org/wordpress/) | [Calvin](https://github.com/mees/calvin?tab=readme-ov-file)<br>[Ravens](https://github.com/google-research/ravens)<br>[VimaBench](https://github.com/vimalabs/VimaBench) |
| [Genesis](https://genesis-embodied-ai.github.io/) ||
| [SOFA](https://github.com/sofa-framework/sofa/)| 常用於軟體機器人的模擬 |
| [GenieSim](https://github.com/AgibotTech/genie_sim)| [A simulation and benchmark framework from AgiBot.](http://agibot-world.com/sim-evaluation/docs) |
| [Gazebo](https://gazebosim.org) | 通用機器人模擬平台，由 [Open Robotics](https://openrobotics.org/) 維護，和 ROS / ROS 2 深度整合，適合移動機器人、倉儲物流等場景的模擬 |

**教程**：
- **Isaac 101：** [Blog](https://axi404.top/tags/isaac%20101) by Axi404.

<section id="benchmarks"></section>

## 6.2 Benchmarks 基準集
具身智能常用 benchmark 總結 [1]：[zhihu](https://zhuanlan.zhihu.com/p/695342864)<br>
* **CALVIN**，[github](https://github.com/mees/calvin)，[website](http://calvin.cs.uni-freiburg.de/) 2022 年，第一個公開的結合了自然語言控制、高維多模態輸入、7 自由度的機械臂控制以及長視野的機器人操縱 benchmark。支援不同的語言指令、不同的攝像頭輸入、不同的控制方式，主要用來評估具身智能模型的多模態輸入的能力和長程規劃能力。
* **Meta-World**，[webpage](https://meta-world.github.io/)：評估機器人在多任務和元強化學習場景下的表現。50 個機器人操作任務（如抓取、推動物體、開門等），組織成不同的基準測試集（如 ML1、ML10、ML45、MT10、MT50 等），每個集合都有明確的訓練任務和測試任務。周邊和文件比較全面，基於 MuJoCo，有完整的 API 和工具，Python import 即可執行。
* **Embodied Agent Interface: Benchmarking LLMs for Embodied Decision Making**，[website](https://embodied-agent-interface.github.io/)：主要評估大型語言模型 (LLMs) 在具身決策中的表現，重點在於決策過程，包括目標解釋、子目標分解、動作序列化和狀態轉換建模，不涉及到具體的執行。
* **RoboGen**，[repo](https://github.com/Genesis-Embodied-AI/RoboGen)，[website](https://robogen-ai.github.io/)：不是生成 policy，而是生成任務、場景和帶標記的數據，能直接用來監督學習。
* **LIBERO**，[repo](https://github.com/Lifelong-Robot-Learning/LIBERO)，[website](https://libero-project.github.io/intro.html)：用一個程序化生成管道來生成任務，這個管道理論上可以生成無限數量的操作任務，還提供了：三種視覺運動策略網路架構 (RNN、Transformer 和 ViLT) 和三種終身學習演算法，以及順序微調和多任務學習的基準。
* **RoboTwin**，[repo](https://github.com/TianxingChen/RoboTwin)：使用程序生成雙臂機器人無限操作任務數據，並提供了所有任務的評測基準。

<section id="datasets"></section>

## 6.3 Datasets 數據集
* **Open X-Embodiment: Robotic Learning Datasets and RT-X Models**，[website](https://robotics-transformer-x.github.io/)：22 種不同機器人平台的超過 100 萬條真實機器人軌跡數據，覆蓋了 527 種不同的技能和 160,266 項任務，主要集中在抓取和放置。
* **AgiBot World Datasets (智元机器人)**，[website](https://agibot-world.com/)：八十餘種日常生活中的多樣化技能，超過 100 萬條軌跡數據，採集自**同構型機器人**，多級品質把控和全程人工在環的策略，從採集員的專業培訓，到採集過程中的嚴格管理，再到數據的篩選、審核和標註，每一個環節都經過了精心設計和嚴格把控。
* **RoboMIND**，[website](https://x-humanoid-robomind.github.io/)：包含了在 479 種不同任務中涉及 96 類獨特物體的 10.7 萬條真實世界演示軌跡，來自四種不同協作臂，任務被分為基礎技能、精準操作、場景理解、櫃體操作和協作任務五大類。
* **All Robots in One**，[website](https://imaei.github.io/project_pages/ario/)：ARIO 數據集，包含了 **2D、3D、文本、觸覺、聲音 5 種模態的感知數據**，涵蓋**操作**和**導航**兩大類任務，既有**模擬數據**，也有**真實場景數據**，並且包含多種機器人硬體，有很高的豐富度。在數據規模達到三百萬的同時，還保證了數據的統一格式，是目前具身智能領域同時達到高品質、多樣化和大規模 of the 開源數據集。
* **MimicGen** [26 Oct 2023, CoRL 2023]，[repo](https://github.com/NVlabs/mimicgen)，[website](https://mimicgen.github.io/)：基於 Robosuite 與 MuJoCo 開發的高效數據生成框架，主要聚焦於單臂機器人桌面操作任務，支援多種主流機器人型號。MimicGen 提出了一種自動化的數據擴增方法，能夠從少量真實人類演示中自動生成大量模擬數據，例如僅使用 200 段真人演示即可生成超過 5 萬條模擬演示數據，涵蓋 18 類常見機器人任務。
* **RoboCasa** [4 Jun 2024]，[repo](https://github.com/robocasa/robocasa)，[website](https://robocasa.ai/)：基於 RoboSuite 與 MimicGen 在 MuJoCo 中構建的高模擬廚房任務模擬平台。RoboCasa 提供了 120 個多樣化廚房環境，包含超過 2500 個 3D 物體模型。平台支援單臂、雙臂、人形機器人以及移動底座搭載機械臂的機器人系統。此外，RoboCasa 內置了 25 種基礎原子任務和 75 種組合任務，能夠真實模擬機器人在複雜廚房場景中的多樣化操作行為。
* **DexMimicGen** [6 Mar 2025, ICRA 2025]，[repo](https://github.com/NVlabs/dexmimicgen/)，[website](https://dexmimicgen.github.io/)：以 RoboSuite 和 MimicGen 為基礎，在 MuJoCo 平台上構建的高保真雙臂桌面操作任務模擬環境。DexMimicGen 涵蓋 9 類典型雙臂任務，提出了增強版 real2sim2real 數據自動生成技術，只需 60 段真實人類演示便可生成 2.1 萬條高品質模擬數據。相比原版 MimicGen，該框架顯著提升了數據生成效率和真實感，使機器人雙臂協作任務的模擬訓練更具實用性。
* **FUSE Dataset** [ICRA 2025] [website](https://fuse-model.github.io/) 包含 26,866 條遠端操控軌跡，涵蓋桌面抓取、購物袋內抓取和按鈕按壓三類任務。機器人透過 Meta Oculus Quest 2 VR 頭顯操作，任務結合語言指令和複雜視覺遮擋，支援多感測器與語言融合的機器人策略研究。
* **BiPlay Dataset** [website](https://dit-policy.github.io/)：為了解決現有雙臂數據集任務單一、環境固定的問題，BiPlay 數據集採用隨機物體和背景，採集多樣化雙臂操作軌跡。數據由多段 3.5 分鐘的機器人操作影片拆分成 7023 個帶語言任務描述的剪輯，總計 10 小時數據，支援雙臂操作泛化研究。
* **DROID (Distributed Robot Interaction Dataset)** [website](https://droid-dataset.github.io/)：包含 76,000 條示範軌跡，約 350 小時交互數據，覆蓋 564 個場景和 86 個任務。數據由 50 名採集員在北美、亞洲和歐洲 12 個月內收集，場景和任務多樣性顯著提升。基於 DROID 訓練的策略表現更優、魯棒性和泛化能力更強。數據集、訓練代碼及硬體搭建指南均已開源。
* **BridgeData V2** [website](https://rail-berkeley.github.io/bridgedata/)：包含 60,096 條軌跡數據，涵蓋 24 個環境和 13 類技能，支援基於目標圖像或自然語言指令的多任務開放詞彙學習。數據主要採集自 7 個玩具廚房環境及多樣桌面、洗衣機等場景，軌跡包括 50,365 條遠端操控示範和 9,731 條腳本策略執行。每條軌跡均標註對應自然語言任務描述，促進跨環境和跨機構的技能泛化研究。
* **Ego4DSounds** [website](https://ego4dsounds.github.io/)：作為 Ego4D 大規模第一人稱視角數據集的多模態子集，包含超過 120 萬條影片剪輯，覆蓋 3000 多個不同日常場景 and 行為，如烹飪、清潔、購物和社交等。數據強調動作與環境聲音的高度對應，配備帶時間戳的動作敘述，支援具身智能中動作感知、多模態融合及聲音生成等任務的研究。
* **RH20T** [website](https://rh20t.github.io/)：人機交互數據集，包含豐富的人臉和語音資訊，使用時需注意隱私保護，僅限模型訓練。數據原始規模約 40TB，提供尺寸縮減版（約 5TB RGB，10TB RGB-D）。包含 7 組 RGB 影片及對應深度數據，附帶相機標定和機器人關節角度資訊。數據透過 Google Drive 和百度雲公開下載。
* **白虎數據集** [website](https://www.openloong.org.cn/cn/dataset)：大規模**異構機器人**數據集，首批開源數據聚焦四款主流機器人本體（青龍機器人、智元A2D、傅利葉GR2、樂聚誇父）與兩類典型末端執行器，覆蓋工業製造、家居家政、餐飲服務、商超藥店和通用抓取放置五大場景，任務類型超過 30 類，共開放 10 萬餘條高品質任務數據，面向具身智能演算法訓練、模型驗證和跨平台評估提供堅實基礎。


<section id="paper_list"></section>

# 7. Paper Lists - 論文列表

* Awesome Humanoid Robot Learning - Yanjie Ze：[repo](https://github.com/YanjieZe/awesome-humanoid-robot-learning)
* Paper Reading List - DeepTimber 社群：[repo](https://github.com/DeepTimber-Robot-Lab/Paper-Reading-List)
* Paper List - Yanjie Ze：[repo](https://github.com/YanjieZe/Paper-List)
* Paper List For EmbodiedAI - Tianxing Chen：[repo](https://github.com/TianxingChen/Paper-List-For-EmbodiedAI)
* SOTA Paper Rating - Weiyang Jin：[website](https://waynejin0918.github.io/SOTA-paper-rating.io/)
* Awesome-LLM-Robotics：一個包含使用大型語言/多模態模型進行機器人/強化學習的論文精選列表：[website](https://github.com/GT-RIPL/Awesome-LLM-Robotics)
* Awesome-Video-Robotic-Papers - Yaoyao(Freax) Qian：[repo](https://github.com/H-Freax/Awesome-Video-Robotic-Papers)
* Awesome Embodied Robotics and Agent - Haonan Zhang：[repo](https://github.com/zchoi/Awesome-Embodied-Robotics-and-Agent)
* awesome-embodied-vla/va/vln - Qiang (Jony) ZHANG：[repo](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln)
* Awesome-Affordance-Learning - Hanqing Wang：[repo](https://github.com/hq-King/Awesome-Affordance-Learning)
* Embodied-AI-Paper-TopConf - Wenxuan Song, Jiayi Chen, Xiaoquan Sun：[repo](https://github.com/Songwxuan/Embodied-AI-Paper-TopConf)
<section id="acknowledgement"></section>

# 8. Acknowledgement - 致謝
本文轉載/引用了一些博主的文章，我們對他們的知識分享表示感謝，引用列表如下：
[1] 知乎 [穆尧](https://www.zhihu.com/people/mu-yao-12-34)，[2] 知乎 [东林钟声](https://www.zhihu.com/people/dong-lin-zhong-sheng-76)，Github [Yunlong Dong](https://github.com/yunlongdong)，[3] 知乎 [强化学徒](https://www.zhihu.com/people/heda-he-28)，[4] 知乎 [Biang哥](https://www.zhihu.com/people/qi-da-guang)，[5] OpenAI [Lilian Weng](https://lilianweng.github.io/)，[6] B 站 [木木具身](https://space.bilibili.com/350563565)，[7] Github [Zhuoheng Li](https://github.com/StarCycle/EmbodiedAI-Reading-List-For-Lists?tab=readme-ov-file)，[8] 知乎 [Flood Sung](https://www.zhihu.com/people/flood-sung)，[9] Github [Sida Peng](https://github.com/pengsida/learning_research)

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

# 🏷️ License - 許可證
This repository is released under the MIT license. See [LICENSE](./LICENSE) for additional details.


<section id="star-history"></section>

# ⭐️ Star History - Star 歷史

[![Star History Chart](https://api.star-history.com/svg?repos=TianxingChen/Embodied-AI-Guide&type=Date)](https://star-history.com/#TianxingChen/Embodied-AI-Guide&Date)
