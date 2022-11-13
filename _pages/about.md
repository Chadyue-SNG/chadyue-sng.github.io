window.onload = function() {

  MAX_SEQ = 80
  var canvas = document.getElementById('canvas');
  var context = canvas.getContext('2d');
  context.canvas.width = window.innerWidth;
  context.canvas.height = (850 * window.innerWidth) / 1300;
  var width = canvas.width;
  var height = canvas.height;
  var imagedata = context.createImageData(width, height);

  function colorMapping() {
    var mapping = [];

    var color = {};
    color["red"] = 247;
    color["green"] = 252;
    color["blue"] = 253;
    mapping.push(color);

    var color = {};
    color["red"] = 233;
    color["green"] = 242;
    color["blue"] = 247;
    mapping.push(color);

    var color = {};
    color["red"] = 217;
    color["green"] = 231;
    color["blue"] = 241;
    mapping.push(color);

    var color = {};
    color["red"] = 197;
    color["green"] = 216;
    color["blue"] = 232;
    mapping.push(color);

    var color = {};
    color["red"] = 177;
    color["green"] = 201;
    color["blue"] = 225;
    mapping.push(color);

    var color = {};
    color["red"] = 158;
    color["green"] = 188;
    color["blue"] = 218;
    mapping.push(color);

    var color = {};
    color["red"] = 147;
    color["green"] = 165;
    color["blue"] = 206;
    mapping.push(color);

    var color = {};
    color["red"] = 146;
    color["green"] = 139;
    color["blue"] = 187;
    mapping.push(color);

    var color = {};
    color["red"] = 164;
    color["green"] = 109;
    color["blue"] = 157;
    mapping.push(color);

    var color = {};
    color["red"] = 165;
    color["green"] = 114;
    color["blue"] = 177;
    mapping.push(color);

    var color = {};
    color["red"] = 156;
    color["green"] = 138;
    color["blue"] = 222;
    mapping.push(color);

    var color = {};
    color["red"] = 200;
    color["green"] = 142;
    color["blue"] = 170;
    mapping.push(color);

    var color = {};
    color["red"] = 234;
    color["green"] = 153;
    color["blue"] = 137;
    mapping.push(color);

    var color = {};
    color["red"] = 249;
    color["green"] = 174;
    color["blue"] = 140;
    mapping.push(color);

    var color = {};
    color["red"] = 245;
    color["green"] = 190;
    color["blue"] = 162;
    mapping.push(color);

    var color = {};
    color["red"] = 232;
    color["green"] = 204;
    color["blue"] = 192;
    mapping.push(color);

    return mapping;
}

  function complex_abs(z) {
    var x = z[0];
    var y = z[1];
    return Math.sqrt(Math.pow(x, 2) + Math.pow(y, 2));
  }

  function complex_add(z, z_prime) {
    var z_add = [];
    z_add.push(z[0] + z_prime[0]);
    z_add.push(z[1] + z_prime[1]);
    return z_add;
  }

  function complex_square(z) {
    var x = z[0];
    var y = z[1];
    var z_sq = [Math.pow(x, 2) - Math.pow(y, 2), 2*x*y]
    return z_sq;
  }

  function mandelbrot(c) {
    var zn = [0, 0];
    var n = 0;
    while (n <= MAX_SEQ) {
      var zn_sq = complex_square(zn);
      zn = complex_add(zn_sq, c);

      if (complex_abs(zn) > 2) {
        return n;
      }
      n++;
    }
    return -1;
  }

  function draw_mandelbrot(colorMap) {

    for (var x = 0; x < width; x++) {
        for (var y = 0; y < height; y++) {
            var pixelindex = (y * width + x) * 4;

            cx = -2 + (3 / (width - 1)) * x;
            cy = -1 + (2 / (height - 1)) * y;

            m = mandelbrot([cx, cy]);

            if (m == -1) {
              var red = 0;
              var green = 0;
              var blue = 0;
            } else {
              var color_index = m % 16;
              var red = colorMap[color_index]["red"];
              var green = colorMap[color_index]["green"];
              var blue = colorMap[color_index]["blue"];
            }

            // Set the pixel data
            imagedata.data[pixelindex] = red;     // Red
            imagedata.data[pixelindex+1] = green; // Green
            imagedata.data[pixelindex+2] = blue;  // Blue
            imagedata.data[pixelindex+3] = 0;   // Alpha
        }
    }
  }

  function change_alpha(color_mod, duration){
      //if browser doesn't support requestAnimationFrame, generate our own timestamp using Date:
      var timestamp = new Date().getTime();
      var runtime = timestamp - starttime;
      var progress = runtime / duration;
      progress = Math.min(progress, 1);

      for (var x = 0; x < width; x++) {
          for (var y = 0; y < height; y++) {
              var pixelindex = (y * width + x) * 4;
              switch(color_mod) {
                case 0:
                	if (imagedata.data[pixelindex] == 247) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 1:
                	if (imagedata.data[pixelindex] == 233) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 2:
                	if (imagedata.data[pixelindex] == 217) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 3:
                	if (imagedata.data[pixelindex] == 197) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 4:
                	if (imagedata.data[pixelindex] == 177) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 5:
                	if (imagedata.data[pixelindex] == 158) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 6:
                	if (imagedata.data[pixelindex] == 147) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 7:
                	if (imagedata.data[pixelindex] == 146) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 8:
                	if (imagedata.data[pixelindex] == 164) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 9:
                	if (imagedata.data[pixelindex] == 165) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 10:
                	if (imagedata.data[pixelindex] == 156) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 11:
                	if (imagedata.data[pixelindex] == 200) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 12:
                	if (imagedata.data[pixelindex] == 234) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 13:
                	if (imagedata.data[pixelindex] == 249) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 14:
                	if (imagedata.data[pixelindex] == 245) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
                case 15:
                	if (imagedata.data[pixelindex] == 232) {
                		imagedata.data[pixelindex+3] = 255;   // Alpha
                	}
                break;
              default:
                break;
            }
          }
      }
      context.putImageData(imagedata, 0, 0);
      if (runtime < duration) { // if duration not met yet
          requestAnimationFrame(function(){ // call requestAnimationFrame again with parameters
            setTimeout(function() {
              change_alpha(color_mod + 1, duration) }, 30);
          })
      }
  }

  // Main loop
  function main(tframe) {

        var colorMap = colorMapping();
        draw_mandelbrot(colorMap);

        //window.requestAnimationFrame(draw_mandelbrot);
        requestAnimationFrame(function(){
            starttime = new Date().getTime() //if browser doesn't support requestAnimationFrame, generate our own timestamp using Date
            change_alpha(0, 1000000000000);
        })
  }

  // Call the main loop
  main(0)
};
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

I am **YUE Wenchao**, a passionate about solving technically challenging problems that have a direct impact on medical robotics community and society. In order to acquire the required skills and technical knowledge required for it, I worked as a Full-time Research Engineer Fellow affiliated with <a href='https://arc.nus.edu.sg/'>Advanced Robotics Centre (ARC)</a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a>, supervised by <a href='https://cde.nus.edu.sg/me/staff/cecilia-laschi/'>**Prof. Laschi Cecilia**</a>, and I earned M.S. degree with distinction in <a href='https://cde.nus.edu.sg/me/'>Mechanical Engineering</a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a> in 2021, supervised by <a href='https://cde.nus.edu.sg/me/staff/tay-eng-hock-francis/'>**Prof. TAY Eng Hock, Francis**</a>. During this period, I joined Medical Mechatronics Lab as a Part-time Research Assistant affiliated with <a href='https://cde.nus.edu.sg/bme/'>Department of Biomedical Engineering </a> from <a href='https://www.nus.edu.sg/'>National University of Singapore</a>, supervised by <a href='https://cde.nus.edu.sg/bme/staff/dr-ren-hongliang/'>**Prof. Hongliang Ren**</a>. While pursuing my Master degree, I quickly became aware of the enormous potential that Advanced Robotics techinique and Artificial Intelligence compution hold to improve our medical conditions and then better people's daily lives. In order to further specialize in these fields, I decided to pursue doctoral studies in <a href='http://www.ee.cuhk.edu.hk/en-gb/'>Department of Electronic Engineering</a> at <a href='https://www.cuhk.edu.hk/english/index.html'> The Chinese University of Hong Kong</a> in 2021, where I am currently a second-year Ph.D. Candidate, co-supervised by <a href='https://www.ee.cuhk.edu.hk/en-gb/people/academic-staff/professors/prof-ren-hongliang'>**Prof. Hongliang Ren**</a> and <a href='https://cde.nus.edu.sg/me/staff/cecilia-laschi/'>**Prof. Laschi Cecilia**</a>.

My main research vision is to build autonomous dynamic tactile generation module based on multimodal fusion (vision+tactile), which enables the surgical robot to autonomously and efficiently acquire biological properties (such as tissue's elastic modulus) during operation through only millimeter-scale contact depth. In this way, I firmly believe that it safely provides the surgeon with more information through physical interaction beyond the single visual information input, creating a more immersive and comprehensive view of the surgery. Also, I am also interested and dedicated to developing inspiring and new generation of medical devices based on deployable mechanisms, origami structure, soft machines, and etc.

# 🔥 News
- *07/2022*: One paper about magnetic origami spring robots is accepted by IEEE Robotics and Automation Letters (RAL) with the option of IEEE International Conference on Intelligent Robots and Systems (IROS) 2022. (IF=4.325, 2022)
- *07/2022*: One paper about origami-inspired structure for multi-DOF force-sensing is accepted by Sensors. (IF=3.847, 2022)
- *04/2022*: One paper about deployable tubular mechanisms is accepted by Actuators. (IF=2.523, 2022)
- *08/2021*: Moving from SG to HK for my doctoral study.
- *07/2021*: One paper about dual-mode tactile hardness sensor is accepted by Smart Materials and Structures. (IF=4.131, 2022)
- *06/2021*: One paper about dynamic piezoelectric tactile sensor is accepted by IEEE Sensors Journal. (IF=4.325, 2022)

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">RA-L with IROS 2022</div><img src='images/RA_L_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Versatile Motion Generation of Magnetic Origami Spring Robots in the Uniform Magnetic Field](https://ieeexplore.ieee.org/document/9842307)

Yuan Sishen, Cao Sifan, Xue Junnan, Su Shijian, Yan Junyan, Wang Min, **Yue Wenchao**, Cheng Shing Shin, Liu Jun, Wang Jiaole, Song Shuang, Meng, Max Q.-H, and Ren Hongliang*

IEEE Robotics and Automation Letters (RAL) with IEEE International Conference on Intelligent Robots and Systems (IROS) 2022
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Sensors</div><img src='images/Sensors_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Origami-Inspired Structure with Pneumatic-Induced Variable Stiffness for Multi-DOF Force-Sensing](https://www.mdpi.com/1424-8220/22/14/5370)

**Yue Wenchao**, Qi Jiaming, Song Xiao, Fan Shicheng, Giancarlo Fortino, Chen Chia-Hung, Xu Chenjie, and Ren Hongliang*.

Sensors-[Special Issue Advances in Tactile Sensing and Robotic Grasping](https://www.mdpi.com/journal/sensors/special_issues/TSRG)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Actuators</div><img src='images/Actuators_cover.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Deployable Tubular Mechanisms Integrated with Magnetic Anchoring and Guidance System](https://www.mdpi.com/2076-0825/11/5/124)

**Yue Wenchao**, Tang Ruijie, Wong Joei Simin, and Ren Hongliang*.

Actuators-[Special Issue Advancements in Actuation, Sensing, and Control Schemes for Intelligent Medical Robotics](https://www.mdpi.com/journal/actuators/special_issues/actuation_sensing_robotics)
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


# 💬 Invited Talks
- *14.11.2020*, Invited Speaker, Dynamic Piezoelectric Tactile Sensing using Symmetrical Structure of Flexure Hinges and Anisotropic Vibration Modes, International Conference on Intelligent Equipment and Robots, 2020. 

# 💻 Teaching
- *2022.09 - 2022.12*, Teaching Assistant - ENGG 2760B Probability for Engineers
- *2022.01 - 2022.04*, Teaching Assistant - ELEG 3103 Robotic Perception and Intelligence
- *2021.09 - 2021.12*, Teaching Assistant - ENGG 2760B Probability for Engineers


© 2021-2022 Wenchao Yue. All Rights Reserved.
<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=a8c5b6&w=400&t=n&d=yGVNxYGr4WSIHZMPrtf3v0TMFruP0zBzGowqufUxQq4&co=ffffff&ct=d2a690&cmo=9fa08e&cmn=83a296'></script>
