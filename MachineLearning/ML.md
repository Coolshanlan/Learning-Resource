## Pre-Process
### 文字轉數字
``` python
from sklearn.preprocessing import LabelEncoder
labelencoder = LabelEncoder()
data_le=pd.DataFrame(dic)
data_le['Country'] = labelencoder.fit_transform(data_le['Country'])
```
### One hot encoding
by sklearn
```python
from sklearn.preprocessing import OneHotEncoder
onehotencoder = OneHotEncoder(categorical_features = [0])
data_str_ohe=onehotencoder.fit_transform(data_le).toarray()
```
by pytorch
``` python
a=torch.LongTensor(np.reshape([1,3,3],(3,1)))
print(a)
one_hot = torch.zeros((3, 4)).scatter_(1, a, 1)
print(one_hot)
```
```
from sklearn.feature_extraction import DictVectorizer
vec = DictVectorizer(sparse=False, dtype=int)
vec.fit_transform(data)
```
## Pytorch
- tensor.detach() 取出不被追蹤變數
- tensor.item() 取出變數值