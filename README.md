# Mask R-CNN for Table detection training

Steps to prepare jupyter notebook on colab

* Clone the repo, 
``` !git clone https://github.com/Gerald2077/mask-rcnn-training ``` 

* Install mask rcnn using pip 
``` !pip install mrcnn ```

* ``` import sys 
  sys.path.insert(0, '/mask-rcnn-training') ```

* Navigate to the main directory
``` %cd mask-rcnn-training/ ```

* Add the following into the code cell and execute.
``` !git clone https://github.com/Gerald2077/mask-rcnn-training
      !pip install mrcnn
      import sys
      sys.path.insert(0, '/mask-rcnn-training')
      %cd mask-rcnn-training/ 
      ```

* In custom.py updated class name to table(If not already edited).

# Also replace images and annotation json in customeimages/ train and val folders!

# Steps to view dataset

* Open inspect_custom_data.ipynb in google colab by providing github repo link.

# Steps to train model

* 