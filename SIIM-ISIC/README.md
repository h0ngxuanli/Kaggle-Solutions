## Final Rank:  118/3308 🥈SILVER MEDAL

Competition description: [https://www.kaggle.com/competitions/siim-isic-melanoma-classification](https://www.kaggle.com/competitions/siim-isic-melanoma-classification)

Special thanks to [Chris](https://www.kaggle.com/cdeotte). I learned a lot from his notebooks and discussion topics.

We adopted [Chris's Triple Stratified Leak-Free KFold Cross Validation(CV) strategy](https://www.kaggle.com/competitions/siim-isic-melanoma-classification/discussion/165526) to avoid leakage:

- _Isolate Patients_: all images from one patient are fully contained inside a single TFRecord.

- _Balance Malignant Images_: the entire dataset has 1.8% malignant images. Each TFRecord contains 1.8% malignant images. 

- _Balance Patient Count Distribution_: each TFRecord has the same patient count distribution.   

Besides, we upsampled malignant patients in the train set of each fold to circumvent highly imbalance and utilized TTA (Test Time Augmentation) to yield a higher validation score.

The training environment is Colab Pro. Final submission kernel used an ensemble of EfficientNets with highest CV scores for each training image size 256/384/512. _Private Score: 0.9410; Public Score: 0.9639_    









