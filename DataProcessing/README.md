# Data Pre-Processing
## Exploratory Data Analysis(EDA)
[Automatic EDA Libraries Comparisson](https://www.kaggle.com/andreshg/automatic-eda-libraries-comparisson)
## 文字資料轉換
### 斷詞 Lib

#### 中研院CKIP
#### jiba

### 轉vec

``` python
from sklearn.preprocessing import LabelEncoder
labelencoder = LabelEncoder()
data_le=pd.DataFrame(dic)
data_le['Country'] = labelencoder.fit_transform(data_le['Country'])
```
``` python
from sklearn.feature_extraction import DictVectorizer
vec = DictVectorizer(sparse=False, dtype=int)
vec.fit_transform(data)
```
## One hot encoding
Scikit-Learn
```python
from sklearn.preprocessing import OneHotEncoder
onehotencoder = OneHotEncoder(categorical_features = [0])
data_str_ohe=onehotencoder.fit_transform(data_le).toarray()
```
Pytorch
``` python
onehot_labels = nn.functional.one_hot(labels,num_classes=5)
```
``` python
a=torch.LongTensor(np.reshape([1,3,3],(3,1)))
print(a)
one_hot = torch.zeros((3, 4)).scatter_(1, a, 1)
print(one_hot)
```

## Normalization
[深度學習中的標準化——Normalization Methods in Deep Learning](https://zhuanlan.zhihu.com/p/142866736)
### Zero-mean normalization
[Z-Score 標準化(zero-mean normalization)](https://zhuanlan.zhihu.com/p/32482328)

### Instance Normalization
大多應用在GAN、Style Transform上

[從Style的角度理解Instance Normalization](https://zhuanlan.zhihu.com/p/57875010)

## Image Convert
### Gray Level Co-occurrence Matrix(GLCM) 灰度共生矩陣
[還沒看的一篇，對紋理講得蠻詳細的](https://www.itread01.com/content/1545348267.html)

[應用Haralick texture於蔬菜辨識](https://chtseng.wordpress.com/2017/03/17/%E6%87%89%E7%94%A8haralick-texture%E6%96%BC%E8%94%AC%E8%8F%9C%E8%BE%A8%E8%AD%98/)

[灰度共生矩陣（GLCM）With Python Code](https://blog.csdn.net/kmsj0x00/article/details/79463376)

### Image Decompose
- [Decomposing Images into Layers via RGB-space Geometry](https://cragl.cs.gmu.edu/singleimage/)
  - [Paper](https://cragl.cs.gmu.edu/singleimage/Decomposing%20Images%20into%20Layers%20via%20RGB-space%20Geometry%20(Tan%20et%20al%202016%20TOG).pdf)
  - [Website Demo](http://yig.github.io/image-rgb-in-3D/)
## Image Augmentation
### Albumentations Library
[Python庫- Albumentations 圖片數據增強庫](https://www.aiuai.cn/aifarm422.html)

[Overview of popular Image Augmentation packages](https://www.kaggle.com/parulpandey/overview-of-popular-image-augmentation-packages)

### Image Contrast Enhancement
[Image-Contrast-Enhancement](https://github.com/AndyHuang1995/Image-Contrast-Enhancement)

### Mixup/Cutout/CutMix Training Data
## Dataset Format
[制作自己的pascal voc数据集](https://zhuanlan.zhihu.com/p/42980766)

### VOC to COCO
[【筆記】制作自己的MSCOCO数据集（VOC2COCO）](https://blog.csdn.net/csdn_zhishui/article/details/95074395)

### COCO DataLoader
[How to train an Object Detector with your own COCO dataset in PyTorch (Common Objects in Context format)   ](https://medium.com/fullstackai/how-to-train-an-object-detector-with-your-own-coco-dataset-in-pytorch-319e7090da5)

## Data Vision
### T-SNE
[資料降維與視覺化：t-SNE 理論與應用](https://mropengate.blogspot.com/2019/06/t-sne.html)

做資料視覺化通常會需要用到降為技術，TSNE是常見技術之一效果不錯

[Kaggle example for efficionnet-b3 without classifier](https://www.kaggle.com/c/cassava-leaf-disease-classification/discussion/202017)