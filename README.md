# Robust Deep Object Tracking against Adversarial Attacks

:herb: Robust Deep Object Tracking against Adversarial Attacks（Under Review）

Shuai Jia, Chao Ma, Yibing Song and Xiaokang Yang

This work is based on [Robust Tracking against Adversarial Attacks](https://arxiv.org/pdf/2007.09919.pdf) in ECCV2020.

## Introduction
<img src="https://github.com/joshuajss/RTAA/blob/master/demo/visualization.png" width='700'/><br/>

Deep convolutional neural networks (CNNs) are vulnerable to adversarial attacks. 
- We study the robustness of the state-of-the-art deep trackers against adversarial attacks under both white-box and black-box settings. 
- We propose a defense method to subtract perturbations from the input frame, which eliminates performance drops caused by adversarial attacks. 
- We craft universal adversarial perturbations to directly inject them into every frame of video sequences, leading to a higher attack speed.
- We choose four representative trackers, [SiamRPN++](https://github.com/STVIR/pysot), [SiamCAR](https://github.com/ohhhyeahhh/SiamCAR), [RT-MDNet](https://github.com/IlchaeJung/RT-MDNet) and [TransT](https://github.com/chenxin-dlut/TransT).

## Prerequisites 

 The environment follows the tracker you intend to attack：
 
 - The specific setting and pretrained model for **SiamPRN++** can refer to [[Code_SiamRPN++]](https://github.com/STVIR/pysot).
 .
 - The specific setting and pretrained model for **SiamCAR** can refer to [[Code_SiamCAR]](https://github.com/ohhhyeahhh/SiamCAR).
 
 - The specific setting and pretrained model for **RT-MDNet** can refer to [[Code_RT-MDNet]](https://github.com/IlchaeJung/RT-MDNet).
 
 - The specific setting and pretrained model for **TransT** can refer to [[Code_TransT]](https://github.com/chenxin-dlut/TransT).
 
## Results (Not updated)
 #### Result for SiamRPN++ on multiple datasets
|                    | OTB2015<br>OP / DP|  VOT2019<br>A / R / EAO |VOT2018<br>A / R / EAO  | VOT2016<br>A / R / EAO | UAV123 <br>OP / DP| LaSOT <br>OP / DP|
| -------------------| :--------------:  | :----:  |:----: |:----: |:----: |:----: |
| SiamRPN++(Original)|  0.658 / 0.886    |   0.585 / 0.272 / 0.380  |0.622 / 0.214 / 0.418|  0.592 / 0.791    | ||
| SiamRPN++(Random)  |  0.586 / 0.799    |  0.571 / 0.529 / 0.223   |0.606 / 0.303 / 0.336|  0.572 / 0.769    |||
| SiamRPN++(Att)     |  0.050 / 0.050    |  0.536 / 1.447 / 0.097   |0.521 / 1.631 / 0.078|  0.026 / 0.045    |||
| SiamRPN++(Att+Def) |  0.473 / 0.639    |  0.579 / 0.674 / 0.195   |0.581 / 0.722 / 0.211|  0.465 / 0.639    |||
| SiamRPN++(Def)     |  0.658 / 0.886    |  0.584 / 0.253 / 0.384   |0.625 / 0.224 / 0.439|  0.592 / 0.792    |||

 #### Result for SiamCAR on multiple datasets
|                    | OTB2015<br>OP / DP|  VOT2019<br>A / R / EAO |VOT2018<br>A / R / EAO  | VOT2016<br>A / R / EAO | UAV123 <br>OP / DP| LaSOT <br>OP / DP|
| -------------------| :--------------:  | :----:  |:----: |:----: |:----: |:----: |
| SiamCAR(Original)|  0.658 / 0.886    |   0.585 / 0.272 / 0.380  |0.622 / 0.214 / 0.418|  0.592 / 0.791    | ||
| SiamCAR(Random)  |  0.586 / 0.799    |  0.571 / 0.529 / 0.223   |0.606 / 0.303 / 0.336|  0.572 / 0.769    |||
| SiamCAR(Att)     |  0.050 / 0.050    |  0.536 / 1.447 / 0.097   |0.521 / 1.631 / 0.078|  0.026 / 0.045    |||
| SiamCAR(Att+Def) |  0.473 / 0.639    |  0.579 / 0.674 / 0.195   |0.581 / 0.722 / 0.211|  0.465 / 0.639    |||
| SiamCAR(Def)     |  0.658 / 0.886    |  0.584 / 0.253 / 0.384   |0.625 / 0.224 / 0.439|  0.592 / 0.792    |||

 
 
 #### Result for RT-MDNet on multiple datasets
|                    | OTB2015<br>OP / DP|  VOT2019<br>A / R / EAO |VOT2018<br>A / R / EAO  | VOT2016<br>A / R / EAO | UAV123 <br>OP / DP| LaSOT <br>OP / DP|
| -------------------| :--------------:  | :----:  |:----: |:----: |:----: |:----: |
| RT-MDNet(Original)|  0.643 / 0.876    |   0.533 / 0.567 / 0.176  |0.567 / 0.196 / 0.370|  0.512 / 0.754    |||
| RT-MDNet(Random)  |  0.559 / 0.753    |  0.503 / 0.871 / 0.137   |0.550 / 0.452 / 0.235|  0.491 / 0.728    |||
| RT-MDNet(Att)     |  0.131 / 0.140    |  0.475 / 1.611 / 0.076   |0.469 / 0.928 / 0.128|  0.079 / 0.128    |||
| RT-MDNet(Att+Def) |  0.420 / 0.589    |  0.515 / 1.021 / 0.110   |0.531 / 0.494 / 0.225|  0.419 / 0.620    |||
| RT-MDNet(Def)     |  0.644 / 0.883    |  0.529 / 0.538 / 0.179   |0.540 / 0.168 / 0.364|  0.513 / 0.757    |||

 #### Result for TransT on multiple datasets
|                    | OTB2015<br>OP / DP|  VOT2019<br>A / R / EAO |VOT2018<br>A / R / EAO  | VOT2016<br>A / R / EAO | UAV123 <br>OP / DP| LaSOT <br>OP / DP|
| -------------------| :--------------:  | :----:  |:----: |:----: |:----: |:----: |
| TransT(Original)|  0.658 / 0.886    |   0.585 / 0.272 / 0.380  |0.622 / 0.214 / 0.418|  0.592 / 0.791    | ||
| TransT(Random)  |  0.586 / 0.799    |  0.571 / 0.529 / 0.223   |0.606 / 0.303 / 0.336|  0.572 / 0.769    |||
| TransT(Att)     |  0.050 / 0.050    |  0.536 / 1.447 / 0.097   |0.521 / 1.631 / 0.078|  0.026 / 0.045    |||
| TransT(Att+Def) |  0.473 / 0.639    |  0.579 / 0.674 / 0.195   |0.581 / 0.722 / 0.211|  0.465 / 0.639    |||
| TransT(Def)     |  0.658 / 0.886    |  0.584 / 0.253 / 0.384   |0.625 / 0.224 / 0.439|  0.592 / 0.792    |||
 
:herb: ~~**All raw results are available.**  [[Google_drive]](https://drive.google.com/drive/folders/1E1XrLghxyZRMQSPzO6oxKXd_htErX6WY?usp=sharing)  [[Baidu_Disk]](https://pan.baidu.com/s/1Iqdn34ZXufyxrpvujQykCg) Code: 5ex9~~

## Quick Start (Not updated)
:herb: **The code of adversarial attack and defense will be released soon. **
- ~~You should download the OTB2015 dataset in ```data``` folder.~~
- ~~Please download the pretrained model in [Code_DaSiamRPN](https://github.com/foolwood/DaSiamRPN).~~

~~Test the original performance on OTB2015 dataset, please using the follwing command.~~
```
cd DaSiamRPN/code
python test_otb.py
```
~~Test the adversarial attack performance on OTB2015 dataset, please using the follwing command.~~
```
cd DaSiamRPN/code
python test_otb_attack.py
```
~~Test the adversarial defense performance on OTB2015 dataset, please using the follwing command.~~
```
cd DaSiamRPN/code
python test_otb_defense.py
```

~~```-v``` can be used to visualize the tracking results.~~

## Demo (Not updated)
<img src="https://github.com/joshuajss/RTAA/blob/master/demo/attack_otb100.gif" width='300'/>   <img src="https://github.com/joshuajss/RTAA/blob/master/demo/defense_otb100.gif" width='300'/><br/>
&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; <img src="https://github.com/joshuajss/RTAA/blob/master/demo/legend.png" width='400'/><br/>

## Acknowledgement 
We sincerely thanks the authors of [SiamRPN++](https://github.com/STVIR/pysot), [SiamCAR](https://github.com/ohhhyeahhh/SiamCAR), [RT-MDNet](https://github.com/IlchaeJung/RT-MDNet) and [TransT](https://github.com/chenxin-dlut/TransT), who provide the baseline trackers for our attack and defense.
## License
Licensed under an MIT license.

