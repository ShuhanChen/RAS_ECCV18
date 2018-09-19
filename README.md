# RAS
This code is for the paper "Reverse Attention for Salient Object Detection".[pdf](http://openaccess.thecvf.com/content_ECCV_2018/papers/Shuhan_Chen_Reverse_Attention_for_ECCV_2018_paper.pdf)

---

Citation
---
@inproceedings{chen2018eccv, <br>
author={Chen, Shuhan and Tan, Xiuli and Wang, Ben and Hu, Xuelong}, <br>
booktitle={European Conference on Computer Vision}, <br>
title={Reverse Attention for Salient Object Detection}, <br>
year={2018}<br>
} 

Saliency Map
---
The saliency maps on 7 datasets are available at [Baidu drive](https://pan.baidu.com/s/1fG-LO48CwZOeFIqH2Xvc2Q)(zin5) and [Google drive](https://drive.google.com/open?id=1OTgOYlZoTOFOIHwxEDBYkZbAS7L3UKcP).

Installing
---
1. Install prerequisites for Caffe (http://caffe.berkeleyvision.org/installation.html#prequequisites).<br>
2. Build [DSS](https://github.com/Andrew-Qibin/caffe_dss) [1]. Supposing the root directory of DSS is ``$DSS``.<br>
3. Copy the folder RAS to ``$DSS/example/``.<br>

Training
---
1. Download training dataset and put it to ``$DSS/data/``.<br>
2. Download the Pre-trained VGG model ([VGG-16](http://vcl.ucsd.edu/hed/5stage-vgg.caffemodel)) and copy it to ``$DSS/example/ras``.<br>
3. Change the dataset path in ``$DSS/example/RAS/train.prototxt``.<br>
4. Run ``solve.py`` in shell (or you could use IDE like Eclipse).<br>

```
cd $DSS/example/RAS/
python solver.py
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
Pre-trained RAS model on [MSRA-B](https://people.cs.umass.edu/~hzjiang/drfi/index.html): [Baidu drive] and [Google drive](https://drive.google.com/open?id=1vDHzr0O7qcQcx0qkzz0iSe5qTPn8h6J0).

Reference
---
[1] Hou, Q., Cheng, M.M., Hu, X., Borji, A., Tu, Z., Torr, P.: Deeply supervised
salient object detection with short connections. In: CVPR. (2017) 5300–5309.
