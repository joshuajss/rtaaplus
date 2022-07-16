# Robust Deep Object Tracking against Adversarial Attacks

:herb: Robust Deep Object Tracking against Adversarial Attacks（Under Review）

Shuai Jia, Chao Ma, Yibing Song and Xiaokang Yang

This work is based on [Robust Tracking against Adversarial Attacks](https://arxiv.org/pdf/2007.09919.pdf) in ECCV2020. [[Project]](https://github.com/VISION-SJTU/RTAA)

## Introduction
<img src="https://github.com/joshuajss/rtaaplus/blob/main/img/pipeline.png" width='700'/><br/>

Deep convolutional neural networks (CNNs) are vulnerable to adversarial attacks. 
- We study the robustness of the state-of-the-art deep trackers against adversarial attacks under both white-box and black-box settings. 
- We propose a defense method to subtract perturbations from the input frame, which eliminates performance drops caused by adversarial attacks. 
- We craft universal adversarial perturbations to directly inject them into every frame of video sequences, leading to a higher attack speed.
- We choose four representative trackers, [SiamRPN++](https://github.com/STVIR/pysot), [SiamCAR](https://github.com/ohhhyeahhh/SiamCAR), [RT-MDNet](https://github.com/IlchaeJung/RT-MDNet) and [TransT](https://github.com/chenxin-dlut/TransT).

## Prerequisites 

 The environment follows the tracker you intend to attack：
 
 - The specific setting and pretrained model for **SiamPRN++** can refer to [[Code_SiamRPN++]](https://github.com/STVIR/pysot).
 - The specific setting and pretrained model for **SiamCAR** can refer to [[Code_SiamCAR]](https://github.com/ohhhyeahhh/SiamCAR).
 - The specific setting and pretrained model for **RT-MDNet** can refer to [[Code_RT-MDNet]](https://github.com/IlchaeJung/RT-MDNet).
 - The specific setting and pretrained model for **TransT** can refer to [[Code_TransT]](https://github.com/chenxin-dlut/TransT).
 
## Experiments
 - #### Results on the OTB2015 dataset
 <img src="https://github.com/joshuajss/rtaaplus/blob/main/img/results_otb.png" width='800'/><br/>
  - #### Results on the UAV123 dataset
 <img src="https://github.com/joshuajss/rtaaplus/blob/main/img/results_uav.png" width='800'/><br/>
  - #### Results on the LaSOT dataset
 <img src="https://github.com/joshuajss/rtaaplus/blob/main/img/results_lasot.png" width='800'/><br/>

 
:herb: **All raw results are available.**  [[Google_drive]](https://drive.google.com/file/d/1KlL8qj36srqC8lvX7J2NlI-Ff-XDQzj3/view?usp=sharing)

## Quick Start

:herb: **The code of adversarial attack and defense will be released soon.**


## Demo
<img src="https://github.com/joshuajss/rtaaplus/blob/main/img/human9_attack.gif" width='300'/>   <img src="https://github.com/joshuajss/rtaaplus/blob/main/img/human9_defense.gif" width='300'/><br/>
<img src="https://github.com/joshuajss/rtaaplus/blob/main/img/legend.png" width='600'/><br/>

:herb: **All demos are available at [[video]](https://drive.google.com/file/d/1KlL8qj36srqC8lvX7J2NlI-Ff-XDQzj3/view?usp=sharing)
 .**

## Acknowledgement 
We sincerely thanks the authors of [SiamRPN++](https://github.com/STVIR/pysot), [SiamCAR](https://github.com/ohhhyeahhh/SiamCAR), [RT-MDNet](https://github.com/IlchaeJung/RT-MDNet) and [TransT](https://github.com/chenxin-dlut/TransT), who provide the baseline trackers for our attack and defense.
## License
Licensed under an MIT license.

