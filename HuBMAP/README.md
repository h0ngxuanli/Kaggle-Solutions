## Final Rank:  40/1200 🥈SILVER MEDAL

Competition description: [https://www.kaggle.com/c/hubmap-kidney-segmentation](https://www.kaggle.com/c/hubmap-kidney-segmentation)

Notebooks' frameworks were heavily insp from [Matthias](https://www.kaggle.com/matjes). 

<div align = "justify"> 
  
[hubmap-anatomy-zarr](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-anatomy-zarr.ipynb) / [hubmap-labels-pdf](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-labels-pdf-0-5-0.16-0-01.ipynb) / [hubmap-zarr](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-zarr.ipynb) created probability density function(PDF) by assigning weights for cortex, medulla, and background regions according to anatomical structure.  
  
</div>

<div align = "justify">  
  
 During training, randomly sampled tiles with a high probability of containing glomeruli based on PDF from TIFF tissue image to enable a robust model and fast training convergence. Augmented image with RandomBrightnessContrast, HueSaturationValue and ContrastLimitedAHE to suppress the effect of blur, over-bright and over-dark regions in the image.
  
 </div>


We put the two model with highest CV Score  ensembling predictions to the global feature extraction.




Final submission kernel used efficientdet d5 with TTA (Test Time Augmentation) such as Flip, Rotate. Private Score: 0.6491; Public Score: 0.7352

