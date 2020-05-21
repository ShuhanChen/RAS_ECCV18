# RAS
This code is for the paper "Reverse Attention for Salient Object Detection".[pdf](https://arxiv.org/pdf/1807.09940.pdf)

---
Pytorch Version
---
A PyTorch version is available at [here](https://github.com/ShuhanChen/RAS-pytorch).

Citation
---
```
@inproceedings{chen2018eccv, 
  author={Chen, Shuhan and Tan, Xiuli and Wang, Ben and Hu, Xuelong}, 
  booktitle={European Conference on Computer Vision}, 
  title={Reverse Attention for Salient Object Detection}, 
  year={2018}
} 
```
```
@article{chen2020tip, 
  author={Chen, Shuhan and Tan, Xiuli and Wang, Ben and Lu, Huchuan and Hu, Xuelong and Fu, Yun}, 
  journal={IEEE Transactions on Image Processing}, 
  title={Reverse Attention Based Residual Network for Salient Object Detection},
  volume={29},  
  pages={3763-3776},
  year={2020}
} 
```

Installing
---
1. Install prerequisites for Caffe (http://caffe.berkeleyvision.org/installation.html#prequequisites).<br>
2. Build [DSS](https://github.com/Andrew-Qibin/caffe_dss) [1] with cuDNN v5.1 for acceleration. Supposing the root directory of DSS is ``$DSS``.<br>
```
USE_CUDNN := 1
```
3. Copy the folder RAS to ``$DSS/example/``.<br>

Training
---
1. Prepare training dataset and its corresponding data list.<br>
2. Download the Pre-trained VGG model ([VGG-16](http://vcl.ucsd.edu/hed/5stage-vgg.caffemodel)) and copy it to ``$DSS/example/ras``.<br>
3. Change the dataset path in ``$DSS/example/RAS/train.prototxt``.<br>
4. Run ``solve.py`` in shell (or you could use IDE like Eclipse).<br>

```
cd $DSS/example/RAS/
python solve.py
```

Testing
---
1. Change the dataset path in ``$DSS/example/RAS-tutorial_save.py``.<br>
2. Run ``jupyter notebook RAS-tutorial_save.ipynb``.<br>

Evaluation
---
We use the [code](https://github.com/MingMingCheng/CmCode/tree/master/CmLib/Illustration) of [1] for evaluation.

Pre-trained RAS model 
---
Pre-trained RAS model on [MSRA-B](https://people.cs.umass.edu/~hzjiang/drfi/index.html): [Baidu drive](https://pan.baidu.com/s/1aM2VYUioCpsReOQ-42POoA)(h7qj) and [Google drive](https://drive.google.com/open?id=1vDHzr0O7qcQcx0qkzz0iSe5qTPn8h6J0).<br>
Note that this released model is newly trained and is slightly different from the one reported in our paper.

Saliency Map
---
ECCV 2018: The saliency maps on 7 datasets are available at [Baidu drive](https://pan.baidu.com/s/1fG-LO48CwZOeFIqH2Xvc2Q)(zin5) and [Google drive](https://drive.google.com/open?id=1OTgOYlZoTOFOIHwxEDBYkZbAS7L3UKcP).<br>
TIP 2020: The saliency maps on 6 datasets are available at [Google drive](https://drive.google.com/open?id=16FRhqXEhtWQ8dJh8TzaY-C182TdsAfFQ).<br>

Reference
---
[1] Hou, Q., Cheng, M.M., Hu, X., Borji, A., Tu, Z., Torr, P.: Deeply supervised
salient object detection with short connections. In: CVPR. (2017) 5300–5309.
