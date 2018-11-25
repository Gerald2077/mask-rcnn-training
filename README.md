# Mask R-CNN for table detection training on google colab GPU

## Checklist!!
* In custom.py updated class name to table(If not already edited).

* Also replace images and annotation json in customeimages/ train and val folders!

* Add the following into the code cell and execute.
``` 
!rm mask-rcnn-training/
!git clone https://github.com/Gerald2077/mask-rcnn-training
!pip install mrcnn
%cd mask-rcnn-training/ 

```
---

## The above steps do the following to prepare jupyter notebook on colab-

* Clear the previous repo folder
``` !rm mask-rcnn-training/ ```
* Clone the repo, 
``` !git clone https://github.com/Gerald2077/mask-rcnn-training ``` 

* Install mask rcnn using pip 
``` !pip install mrcnn ```

* Navigate to the main directory
``` %cd mask-rcnn-training/ ```

> Don't need this now,

```
import sys 
sys.path.insert(0, '/mask-rcnn-training')
```
---
## Steps to view dataset using notebook

* Open inspect_custom_data.ipynb in google colab by providing github repo link. 

* Select GPU from Edit -> Notebook Settings

* Do copy to drive action. 

---
## Steps to train model

* Run this in a separate code block after making sure GPU is enabled in EDIT->Notebook Settings & you have the initial steps like deleting folder, cloning repo & making sure a couple of images from the dataset are viewable with mask, before proceeding with training(taking 50 mins at the moment on GPU)
```
!python3 custom.py train --dataset=customImages/ --weights=coco
```

* After training we will save the generated h5 file to our local machine & use it for inference using CPU. We can also verify the same with another notebook, where we need to upload the h5 file & update the filename in that notebook as well.
