# Python

## Basic Python
[NCU Programming for Deep Learning EE3054](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054)
- [IPython](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_00_IPython.ipynb)
- [DataTypes](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_01_DataTypes.ipynb)
- [Numbers](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_02_Numbers.ipynb)
- [TextStrings](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_03_TextStrings.ipynb)
- [ChooseWithIF](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_04_ChooseWithIF.ipynb)
- [LoopWithWhileFor](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_05_LoopWithWhileFor.ipynb)
- [TuplesList](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_06_TuplesList.ipynb)
- [DictionariesSets](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_07_DictionariesSets.ipynb)
- [Functions](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_08_Functions.ipynb)
- [ModulesPackages](https://github.com/Coolshanlan/Learning-Resource/tree/master/Python/NCU%20Programming%20for%20Deep%20Learning%20EE3054/1092_PDL_09_ModulesPackages.ipynb)
## Numpy
[Numpy cheatsheet](https://www.kaggle.com/nageshsingh/numpy-cheatsheet)

## Pandas
[Pandas 100 tricks](https://www.kaggle.com/python10pm/pandas-100-tricks)
### Dataframe shuffle
``` Python
dataframe.sample(frac=1).reset_index(drop =True)
```
### DataFrame to list of dictionary
``` Python
DataFrame.to_dict("records")
```
### DataFrame filter to select data
``` Python
DataFrame[DataFrame["label"] == filtervalue]
DataFrame[DataFrame["label"] == filtervalue].tolist()
```

## Matplotlib
[Simple Matplotlib & Visualization Tips](https://www.kaggle.com/subinium/simple-matplotlib-visualization-tips)

[matplotlib cheatsheet](https://github.com/rougier/matplotlib-cheatsheet)

### subplots
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
### pie plot
``` Python
fig,axis =plt.subplots()
_,_,autotexts=axis.pie(labeltotalvalues,labels=list(d_label.values()),autopct = '%1.1f%%',shadow=True)
# for i, a in enumerate(autotexts):
#     a.set_text("{}({})".format(a.get_text(),labeltotalvalues[i]))
axis.axis('equal')
fig.show()
```