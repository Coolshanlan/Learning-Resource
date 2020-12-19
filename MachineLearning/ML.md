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
## Pandas
Dataframe shuffle
``` Python
dataframe.sample(frac=1).reset_index(drop =True)
```
DataFrame to list of dictionary
``` Python
DataFrame.to_dict("records")
```
DataFrame filter to select data
``` Python
DataFrame[DataFrame["label"] == filtervalue]
DataFrame[DataFrame["label"] == filtervalue].tolist()
```
## Matpoltlib
subplots
``` Python
def plot_smapleimage():
    fig,axis = plt.subplots(2,4,figsize=(15,15))
    plot_images = traincsv.sample(8).to_dict("records")
    for i in range(8):
        imgpath  =os.path.join(basepath,"train_images/"+plot_images[i]["image_id"])
        img = cv2.imread(imgpath)
        img = img[:,:,::-1]
        axis[i//4,i%4].set_title("")
        axis[i//4,i%4].axis('off')
        axis[i//4,i%4].imshow(img)
    fig.subplots_adjust(wspace =0.3, hspace =-0.7)
    fig.show()
plot_smapleimage()
```
pie plot
``` Python
fig,axis =plt.subplots()
_,_,autotexts=axis.pie(labeltotalvalues,labels=list(d_label.values()),autopct = '%1.1f%%',shadow=True)
# for i, a in enumerate(autotexts):
#     a.set_text("{}({})".format(a.get_text(),labeltotalvalues[i]))
axis.axis('equal')
fig.show()
```