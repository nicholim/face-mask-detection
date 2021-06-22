---
title: Face Mask Detection
author: Nicholas Limarsha
date: 21-06-2021
---

# Overview

COVID-19 pandemic has rapidly affected our day-to-day life, disrupting the world. Wearing a protective face mask plays a pivotal role in protecting the health of individuals against respiratory diseases, as infection is transmitted predominately by respiratory droplets generated when people breathe, cough, talk, or sneeze. In the near future, many public service providers will ask the customers to wear masks correctly to avail of their services. Wearing a mask is a primary, convenient, and effective method of blocking 80% of all respiratory infections. Therefore, face mask detection has become a crucial task to help global society.

This project is an image based machine learning process where the objective of the project is to identify and annotate whether faces inside a given picture are wearing a mask. It is inspired by the unfortunate pandemic which forced people to always wear masks in order to help to prevent the spreading of the virus.

# Dataset and Preprocessing

In this project, images dataset and annotations of the images dataset available publicly on Kaggle website in the following link: 

https://www.kaggle.com/andrewmvd/face-mask-detection

This dataset contains 853 images belonging to the three classes (with mask, without mask, and mask worn incorrectly), as well as annotations of their bounding boxes in the PASCAL VOC format provided via .xml files.

This .ipynb is made using Google Colab's environment with the help of PyTorch library which features Faster R-CNN, Mask R-CNN, and RetinaFace model. It is also included with non-max suppression such that the bounding boxes are not overlap with each other and shaped nicely. In general, all these architectures will perform bounding box prediction as well as classification of the object interests inside the bounding boxes as in object detection.

# Folder structure

```
Colab (Face Mask Detection.ipynb)
    | checkpoints -> save best model
    | data -> datasets
    | loss_list -> .txt of lists of training loss, mAP@.5, and mAP@.5:.95 for each model
    | pyhelper -> for COCO purposes
```

Complete version of the repository which include checkpoints is in https://gitlab.com/nicholim/face-mask-detection
