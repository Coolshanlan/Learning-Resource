# Deep Learning Resources
## 待讀
[SSL4MIS：半監督醫學圖像分割論文合集+benchmark](https://bangqu.com/9tbJy7.html?fbclid=IwAR1Qh7lEgklCnuwbgWrzO7qff9Tt7-kUq7J9U94LrErqdCIFMnIOuB5FVjI)

[提升Pytorch training 的17種方法](https://bangqu.com/q844ga.html)

[數據集樣本有10萬，結果80%都是貓？如何解決「數據類別不均衡」丨NeurIPS 2020](https://bangqu.com/e6439v.html)

[CV技術在醫療領域中有哪些應用？Salesforce、谷歌、斯坦福綜述文章登上Nature子刊](https://bangqu.com/NC2F11.html)

[介紹一篇深度學習圖像分類中處理noisy labels方法的綜述](https://bangqu.com/qCA4nI.html)

[從零開始，用Python徒手寫線性迴歸](https://bangqu.com/d96f49.html)

[內置降維、聚類等算法，時間序列數據分析Python庫Deeptime](https://bangqu.com/UeE6oB.html)

[如何防止我的模型過擬合？這篇文章給出了6大必備方法](https://bangqu.com/IF9r31.html)

[交叉驗證(Cross-validation, CV)](https://medium.com/@chih.sheng.huang821/%E4%BA%A4%E5%8F%89%E9%A9%97%E8%AD%89-cross-validation-cv-3b2c714b18db)

[Three mysteries in deep learning ensemble knowledge distillation and self distillation](https://www.microsoft.com/en-us/research/blog/three-mysteries-in-deep-learning-ensemble-knowledge-distillation-and-self-distillation/)

[3萬字輕鬆入門Transform Vision](https://bangqu.com/31z8yM.html)

[真正的即插即用！盤點11種CNN網絡設計中精巧通用的「小」插件](https://bangqu.com/YH99o3.html)

[Vision Transformer](https://zhuanlan.zhihu.com/p/273652295)
## 找不到資料或是lib來這裡
[Best-of Machine Learning with Python](https://github.com/ml-tooling/best-of-ml-python)
## Relation Website
[Deepfake Tutorial Website](https://www.deepfakescn.com/)

[CNN 技巧統整《Bag of Tricks for Image Classification with Convolution Neural Networks》](https://arxiv.org/pdf/1812.01187v2.pdf)
## Pytorch
### Seed setting
[Source Code](https://www.kaggle.com/piantic/cnn-or-transformer-pytorch-xla-tpu-for-cassava?scriptVersionId=51538992)
```python
def seed_torch(seed=2021):
    random.seed(seed)
    os.environ['PYTHONHASHSEED'] = str(seed)
    np.random.seed(seed)
    torch.manual_seed(seed)
    torch.cuda.manual_seed(seed)
    torch.backends.cudnn.deterministic = True

seed_torch(seed=CFG.seed)
```
### 提升Pytorch training 速度
- [EN- Faster Deep Learning Training with PyTorch – a 2021 Guide](https://efficientdl.com/faster-deep-learning-in-pytorch-a-guide/#1-consider-using-another-learning-rate-schedule)
- [CN- Faster Deep Learning Training with PyTorch – a 2021 Guide](https://bangqu.com/q844ga.html)
- [其他建議 推！](https://hackmd.io/@Hong-Jia/H1hmbNr1d)
### 分散式訓練(單機多卡)
[【分佈式訓練】單機多卡的正確打開方式（三）](https://fyubang.com/2019/07/23/distributed-training3/)
### Learning Rate Scheduler
[pytorch中六種學習率調整方法](https://zhuanlan.zhihu.com/p/69411064)
### Activation
[優秀的超詳細教學](https://www.chainnews.com/zh-hant/articles/741795991763.htm)
### Pytorch model modify Pre-Trained
- [教學 1 各式修改](https://zhuanlan.zhihu.com/p/75563856)
- [教學 2 修改模組](https://blog.csdn.net/weixin_42118374/article/details/103761795)
### Fine-tune
- [教學 1 凍結參數](https://zhuanlan.zhihu.com/p/79106053)
- [PyTorch 學習筆記（五）：Finetune和各層定制學習率](https://zhuanlan.zhihu.com/p/59780798)
> 推薦  with torch.no_grad():
## ResNet Family
- [ResNet 全解析+improve](https://zhuanlan.zhihu.com/p/54289848)
- [ResNet Xt St 進化教學](https://medium.com/%E8%BB%9F%E9%AB%94%E4%B9%8B%E5%BF%83/deep-learning-residual-leaning-%E8%AA%8D%E8%AD%98resnet%E8%88%87%E4%BB%96%E7%9A%84%E5%86%A0%E5%90%8D%E5%BE%8C%E7%B9%BC%E8%80%85resnext-resnest-6bedf9389ce)
- [ResNeXt](https://medium.com/@hupinwei/resnext%E7%B6%B2%E8%B7%AF-31c76e4d3409)
  - [Group Convolution](https://blog.csdn.net/zhangjunhit/article/details/90763234?utm_medium=distribute.pc_aggpage_search_result.none-task-blog-2~all~first_rank_v2~rank_v25-1-90763234.nonecase&utm_term=%E5%88%86%E7%BB%84%E5%8D%B7%E7%A7%AF)
- ResNeSt
  - [Tutorial 1](https://zhuanlan.zhihu.com/p/132655457)
  - [Tutorial 2](https://www.codenong.com/cs106434314)
  - [Tutorial 3 疑惑教學探討](https://aijishu.com/a/1060000000110446)
## Enhence Model
### Attention in CNN
- [CBAM](https://zhuanlan.zhihu.com/p/96975064)
- [CBAM in Resnet](https://zhuanlan.zhihu.com/p/99261200)
- [BAM](https://blog.csdn.net/qq_32768091/article/details/86612132)
- [SEnet](https://medium.com/@hupinwei/%E6%B7%B1%E5%BA%A6%E5%AD%B8%E7%BF%92-senet-squeeze-and-excitation-networks-52ad0a7fd307)
- [SKNet](https://github.com/developer0hye/SKNet-PyTorchs)
- [SCSENet(cSE、sSE、scSE)](https://blog.csdn.net/XX_123_1_RJ/article/details/87928935)
- [GENet](https://blog.csdn.net/dgyuanshaofeng/article/details/84179196)
- [Regularization L2](https://blog.csdn.net/guyuealian/article/details/88426648)
### Spatial Pyramid Pooling (SPP Layer)
- [Spatial Pyramid Pooling講解](https://zhuanlan.zhihu.com/p/34788333)
### Training Trick
[深度神经网络模型训练中的最新tricks总结【原理与代码汇总】](https://zhuanlan.zhihu.com/p/66080948)
### Noise Label
[Robustness of Accuracy Metric and its Inspirations in Learning with Noisy Label](https://arxiv.org/pdf/2012.04193.pdf)

### Add Attention Block

### Label Smoothing
## Grad-CAM
[打開黑盒子 Open Black Boxes 2: Grad-CAM](https://medium.com/jarvis-toward-intelligence/%E6%89%93%E9%96%8B%E9%BB%91%E7%9B%92%E5%AD%90-open-black-boxes-2-1ec6a313f5e9)
## GAN
[PyTorch GAN example](https://github.com/eriklindernoren/PyTorch-GAN)

## Feature fusion / Module fusion
- Multimodal Compact Bilinear Pooling for Visual Question Answering and Visual Grounding
  - [Tutorial 1](https://medium.com/paper-club/multimodal-compact-bilinear-pooling-for-visual-question-answering-and-visual-grounding-6f71bc7d0566)
  - [Tutorial 2 CN](https://blog.csdn.net/bea_tree/article/details/72903566)
- [Bilinear CNN](https://blog.csdn.net/u013841196/article/details/102730183)
## Image Augmentation
### Albumentations Library
[Python庫- Albumentations 圖片數據增強庫](https://www.aiuai.cn/aifarm422.html)
### Overview of popular Image Augmentation packages
[Overview of popular Image Augmentation packages](https://www.kaggle.com/parulpandey/overview-of-popular-image-augmentation-packages)
### Mixup/Cutout/CutMix Training Data

### Image Decompose
- [Decomposing Images into Layers via RGB-space Geometry](https://cragl.cs.gmu.edu/singleimage/)
  - [Paper](https://cragl.cs.gmu.edu/singleimage/Decomposing%20Images%20into%20Layers%20via%20RGB-space%20Geometry%20(Tan%20et%20al%202016%20TOG).pdf)
  - [Website Demo](http://yig.github.io/image-rgb-in-3D/)
## VOC Dataset format conversion
[制作自己的pascal voc数据集](https://zhuanlan.zhihu.com/p/42980766)

## VOC to COCO
[【筆記】制作自己的MSCOCO数据集（VOC2COCO）](https://blog.csdn.net/csdn_zhishui/article/details/95074395)

## COCO DataLoader
[How to train an Object Detector with your own COCO dataset in PyTorch (Common Objects in Context format)   ](https://medium.com/fullstackai/how-to-train-an-object-detector-with-your-own-coco-dataset-in-pytorch-319e7090da5)

## Normalization
[深度學習中的標準化——Normalization Methods in Deep Learning](https://zhuanlan.zhihu.com/p/142866736)
#### Zero-mean normalization
[Z-Score 標準化(zero-mean normalization)](https://zhuanlan.zhihu.com/p/32482328)

#### Instance Normalization
[從Style的角度理解Instance Normalization](https://zhuanlan.zhihu.com/p/57875010)

## Kaggle trick
Install albumentations for image augmentations

Installing Gradual Warmup Scheduler
```
pip install git+https://github.com/ildoonet/pytorch-gradual-warmup-lr.git
```

## Pandas

#### Shuffle
``` python
df = df.smaple(frac=1,random_state=seed)
```
#### Split Data
```python

```