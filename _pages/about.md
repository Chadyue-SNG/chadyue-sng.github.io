---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

Welcome to my page! I am **YUE Wenchao**, a passionate about solving technically challenging problems that have a direct impact on the medical robotics community and society. In order to acquire the required skills and technical knowledge required for it, I worked as a Full-time Research Engineer Fellow affiliated with <a href='https://arc.nus.edu.sg/'>Advanced Robotics Centre (ARC)</a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a>, supervised by <a href='https://cde.nus.edu.sg/me/staff/cecilia-laschi/'>**Prof. Laschi Cecilia**</a>, and I earned M.S. degree with distinction in <a href='https://cde.nus.edu.sg/me/'>Mechanical Engineering</a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a> in 2021, supervised by <a href='https://cde.nus.edu.sg/me/staff/tay-eng-hock-francis/'>**Prof. TAY Eng Hock, Francis**</a>. During this period, I joined Medical Mechatronics Lab as a Part-time Research Assistant affiliated with <a href='https://cde.nus.edu.sg/bme/'>Department of Biomedical Engineering </a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a>, supervised by <a href='https://cde.nus.edu.sg/bme/staff/dr-ren-hongliang/'>**Prof. Hongliang Ren**</a>. While pursuing my Master degree, I quickly became aware of the enormous potential that Advanced Robotics techniques and Artificial Intelligence computation hold to improve our medical conditions and then better people's daily lives. In order to further specialize in these fields, I decided to pursue doctoral studies in <a href='http://www.ee.cuhk.edu.hk/en-gb/'>Department of Electronic Engineering</a> at <a href='https://www.cuhk.edu.hk/english/index.html'> The Chinese University of Hong Kong</a> in 2021, where I am currently a third-year Ph.D. Candidate, co-supervised by <a href='https://www.ee.cuhk.edu.hk/en-gb/people/academic-staff/professors/prof-ren-hongliang'>**Prof. Hongliang Ren**</a> and <a href='https://cde.nus.edu.sg/me/staff/cecilia-laschi/'>**Prof. Laschi Cecilia**</a>.

My main research vision is to build an autonomous dynamic tactile generation module based on multimodal fusion (vision+tactile), which enables the surgical robot to autonomously, safely, and efficiently acquire biological properties (such as tissue's elastic modulus) during operation through only millimeter-scale contact depth. 

Recently, I am working on developing a multimodal surgical robotic tactile interface based on a Collaborative Research Fund (CRF) project funded by the Hong Kong Research Grants Council (RGC). 

# 🔥 News
- *12/2023*: One poster about the soft pouch motor has won a second-place award at the 8th Chinese Annual Seminar on Soft Robotic Theory and Technology. (Shenzhen, China, 2023)
- *11/2023*: One journal paper about soft pouch motors based on liquid-to-gas phase transition is accepted and selected as the front cover.
- *12/2022*: One paper about deep reinforcement learning-based robotic palpation strategy is accepted by the 2022 IEEE International Conference on Robotics and Biomimetics (ROBIO). (Xishuangbanna, China, 2022)
- *11/2022*: One paper about a laminated continuum robot with gripping force-sensing forceps is accepted by IEEE Sensors Journal. 
- *11/2022*: Our proposed project on "AI-based Pulmonary Tree-branch Reconstruction for Precise Motion Planning in Personalized Robotic-assisted Bronchoscope Intervention" has been finalisted and won the fourth-place award in AI x HK OpenCup 2022.
- *07/2022*: One paper about magnetic origami spring robots is accepted by IEEE Robotics and Automation Letters (RAL) with the option of IEEE International Conference on Intelligent Robots and Systems (IROS) 2022. 
- *07/2022*: One paper about the origami-inspired structure for multi-DOF force-sensing is accepted by Sensors. 
- *05/2022*: Our Projects "Magnetic Capsule Robots" and "Modular Parallel Robot" won the Third-place Award and Merit Award in The 8th Hong Kong University Student Innovation and Entrepreneurship Competition. Many thanks for the generous and continuing help from Prof. Ren and Sishen!
- *04/2022*: One paper about deployable tubular mechanisms is accepted by Actuators. 
- *11/2021*: Our Project "Magnetically-Connected Modular-Reconfigurable Mini-Robot Towards Minimally Invasive Procedures" wins Merit Award in Emedic Global 2021.
- *08/2021*: Moving from SG to HK for my doctoral study.
- *07/2021*: One paper about dual-mode tactile hardness sensors is accepted by Smart Materials and Structures.
- *06/2021*: One paper about dynamic piezoelectric tactile sensors is accepted by IEEE Sensors Journal.

# 📝 Publications 
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Front Cover Invited</div><img src='images/AEM_Front_Cover.PNG' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Dual-Stroke Soft Peltier Pouch Motor Based on Pipeless Thermo-Pneumatic Actuation](https://onlinelibrary.wiley.com/doi/epdf/10.1002/adem.202301408)

**W. Yue**, C. Bai, J. Lai, H. Ren*
- Proposed the novel soft pouch motor based on the pipeless thermo-pneumatic actuation;
- Realized the bidirectional control of liquid-to-gas phase transition;
- Validated the several application potential in both aquatic and terrestrial media environments.

<!-- <div class='paper-box'> -->
<div class='paper-box' style="display: flex; justify-content: center;">
  <div class='paper-box-image'><div><div class="badge">Principle Behind</div><img src='images/PPM_cover.png' alt="sym" width="250%"></div></div>
</div>


</div>
</div>

<!-- <div class='paper-box'> -->
<div class='paper-box' style="display: flex; justify-content: space-between;">
  <div class='paper-box-image'><div><div class="badge">Hovering In Liquid</div><img src='images/Floating_Cover.gif' alt="sym" width="100%"></div></div>
  <div class='paper-box-image'><div><div class="badge">Untether Rolling On Land</div><img src='images/Rolling_Process.gif' alt="sym" width="100%"></div></div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Advanced Engineering Materials - under review</div><img src='images/TattooBalloon_Cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Soft Balloon Actuators Embodied Flexible Ink-Transfer-Printing Sensing for Self-Awareness Inflation and Microneedle Punch**

-Embodying sensing capabilities for soft balloon actuators allow for better control and understanding of their deformation behavior.

-Sensing capabilities in soft balloon actuators improve safety in human-machine interactions reducing the risk of over-inflation.


<!-- <div class='paper-box'> -->
<div class='paper-box' style="display: flex; justify-content: space-evenly;">
<div class='paper-box-image'><div><div class="badge">Pop Up from 2D Plane</div><img src='images/Beating_Balloon.gif' alt="sym" width="100%"></div></div>
  <div class='paper-box-image'><div><div class="badge">Touch Balloon!</div><img src='images/Touch_Process_Cover.gif' alt="sym" width="100%"></div></div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">To Appear Soon</div><img src='images/RoboticMN_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Multimodal Mechanical Stimuli Enables Depth Self-Awareness and Transdermal Drug Diffusion Acceleration based on Robotic Microneedles Patches and Optical Coherence Tomography**

Brief: the objective of our project is to pioneer a groundbreaking robot-assisted transdermal immunization approach. Integrating medical robotics, optical imaging, microneedle technology, and artificial intelligence algorithms, we aim to revolutionize the field of minimally invasive immunization by enabling comprehensive monitoring of the entire process and achieving a highly advanced approach to immunization.

**Interdisciplinary Collaborative Project with CUHK BME and CityU BME**

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IEEE T-ASE (under 2nd Review)</div><img src='images/TASE_Cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**RASEC: Rescaling Acquisition Strategy with Energy Constraints under Fusion Kernel for Active Incision Recommendation in Tracheotomy**

- Visualize hands-on information & Localize the trachea regions more efficiently;
- Enable visual-tactile guidance for robotic tracheotomy;
- Promote surgical sub-task autonomy.

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Sensors</div><img src='images/Sensors_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Origami-Inspired Structure with Pneumatic-Induced Variable Stiffness for Multi-DOF Force-Sensing](https://www.mdpi.com/1424-8220/22/14/5370)

**Yue Wenchao**, Qi Jiaming, Song Xiao, Fan Shicheng, Giancarlo Fortino, Chen Chia-Hung, Xu Chenjie, and Ren Hongliang*.

Sensors - Multidisciplinary Digital Publishing Institute (MDPI)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Actuators</div><img src='images/Actuators_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Deployable Tubular Mechanisms Integrated with Magnetic Anchoring and Guidance System](https://www.mdpi.com/2076-0825/11/5/124)

**Yue Wenchao**, Tang Ruijie, Wong Joei Simin, and Ren Hongliang*.

Actuators - Multidisciplinary Digital Publishing Institute (MDPI)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Smart Materials and Structures</div><img src='images/SMS_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[A dual-mode tactile hardness sensor for intraoperative tumor detection and tactile imaging in robot-assisted minimally invasive surgery](https://iopscience.iop.org/article/10.1088/1361-665X/ac112b/meta)

Zhang Yingxuan, Wei Xiaoyong, **Yue Wenchao**, Zhu Chengjun and Ju Feng*.

Smart Materials and Structures
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IEEE Sensors Journal</div><img src='images/IEEESensors_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Dynamic piezoelectric tactile sensor for tissue hardness measurement using symmetrical flexure hinges and anisotropic vibration modes](https://ieeexplore.ieee.org/abstract/document/9446118)

**Yue Wenchao**, Ju Feng, Zhang Yingxuan, Yun Yahui, Li Tianliang, Tse Zion Tsz Ho and Ren Hongliang*

IEEE Sensors Journal
</div>
</div>


# 💬 Community Contribution
- *28.07.2023*, Invited Speaker on behalf of Medical Mechatronics Lab, "Magnetically-connected Modular Reconfigurable Robots", Roadshow of the CUHK Robotics Open Day hosted by T Stone Robotics Institute, 2023. [Link](https://www.cpr.cuhk.edu.hk/en/press/cuhk-robotics-open-day-and-collaboration-agreement-signing-ceremony-with-hkstp-lenovo-and-hkclr/)
- *07.01.2023*, Invited Speaker on behalf of Medical Mechatronics Lab, Hong Kong Science Popularization Program Series IV - 
Academician Talks Activities hosted by Centre for Artificial Intelligence and Robotics (CAIR) Hong Kong and The Greater Bay Area Association of Academicians(GBAAA), 2023. [Link](https://www.cair-cas.org.hk/article/157)
- *14.11.2020*, Invited Speaker, "Dynamic Piezoelectric Tactile Sensing using Symmetrical Structure of Flexure Hinges and Anisotropic Vibration Modes", International Conference on Intelligent Equipment and Robots. 

# 👨‍🔧 Mentoring Experience
- *2023.09 - 2023.12*, Teaching Assistant - ENGG 2760C Probability for Engineers
- *2023.01 - 2023.04*, Teaching Assistant - ELEG 3103 Robotic Perception and Intelligence
- *2022.09 - 2022.12*, Teaching Assistant - ENGG 2760B Probability for Engineers
- *2022.01 - 2022.04*, Teaching Assistant - ELEG 3103 Robotic Perception and Intelligence
- *2021.09 - 2021.12*, Teaching Assistant - ENGG 2760B Probability for Engineers


© 2021-2022 Wenchao Yue. All Rights Reserved.
<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=a8c5b6&w=400&t=n&d=yGVNxYGr4WSIHZMPrtf3v0TMFruP0zBzGowqufUxQq4&co=ffffff&ct=d2a690&cmo=9fa08e&cmn=83a296'></script>

