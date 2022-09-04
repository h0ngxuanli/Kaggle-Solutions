## Final Rank:  40/1200 🥈SILVER MEDAL 

Competition description: [https://www.kaggle.com/c/hubmap-kidney-segmentation](https://www.kaggle.com/c/hubmap-kidney-segmentation)

Notebooks' frameworks were heavily insp from [Matthias](https://www.kaggle.com/matjes). 

<div align = "justify"> 
  
- [hubmap-anatomy-zarr](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-anatomy-zarr.ipynb) / [hubmap-labels-pdf](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-labels-pdf-0-5-0.16-0-01.ipynb) / [hubmap-zarr](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/hubmap-zarr.ipynb) created probability density function(PDF) by assigning weights for cortex, medulla, and background regions according to anatomical structure.  
  
</div>

<div align = "justify"> 
  
- We integrated test set with pseudo-labels into train set. The pseudo-labels [submission_TF_1_034_10.csv](HuBMAP/model3/submission_TF_1_034_10.csv) / [submission.csv](HuBMAP/0.936gpu1-b3_lr_find_me20_bs12/submission.csv) were generated from [V2- HuBMAP: TF with Multi model ensumble[sub] [Version 10]](https://www.kaggle.com/code/durbin164/v2-hubmap-tf-with-multi-model-ensumble-sub) and [Kidney Unet model (keras) inference [Version 284] ](https://www.kaggle.com/code/vgarshin/kidney-unet-model-keras-inference) separately. 
  
</div>


<div align = "justify">  
  
- We augmented image with RandomBrightnessContrast, HueSaturationValue and ContrastLimitedAHE to suppress the effect of blur, over-bright and over-dark regions in the image.
 
 </div>

<div align = "justify">  
  
- During training, we randomly sampled tiles with a high probability of containing glomeruli based on PDF from TIFF tissue image to enable a robust model and fast training convergence. We adopted the U-net with EfficientNet as backbone to train on those tiles and the model was trained With Mixed Precision to double the batch size.

 </div>
  


<div align = "justify">  
  
- Final submission kernel used an ensemble of two models with highest Public Score (0.936/0.935).  _Private Score: 0.9467; Public Score: 0.9394_
  
 </div>



