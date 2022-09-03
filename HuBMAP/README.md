## Final Rank:  40/1200 🥈SILVER MEDAL

Competition description: [https://www.kaggle.com/c/hubmap-kidney-segmentation](https://www.kaggle.com/c/hubmap-kidney-segmentation)

Notebooks' frameworks were heavily insp from [Matthias](https://www.kaggle.com/matjes). We put the two model with highest Public Score  ensembling predictions to the global feature extraction.

Randomly sampled tiles with a high probability of containing glomeruli from TIFF tissue image to enable a
robust model and fast training convergence. Random tile centers were selected based on probability density
function(PDF) which was created by assigning weights for cortex(0.46), medulla(0.17), and background(0.02)
regions according to anatomical structure.



Final submission kernel used efficientdet d5 with TTA (Test Time Augmentation) such as Flip, Rotate. Private Score: 0.6491; Public Score: 0.7352

