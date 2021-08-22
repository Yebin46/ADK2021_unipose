ADK2021
==========

Cow Keypoint Detection
--------------------

### Base Model
* Unipose: https://github.com/bmartacho/UniPose.git

### Dataset
* Private dataset given by https://github.com/AnimalDatathonKorea/adk2021.git
* train dataset: 9000 Korean Cow images with 17 keypoints

### Preprocessing
    python preprocessing_data.py

### Training
    python unipose.py --epochs EPOCH_NUM --pretrained ./weights/cow_kps_model/UniPose_MPII.tar

### Test
    python unipose.py --is_train 2 --pretrained ./weights/cow_kps_model/0.74_sgd_cow_kps_model_best.pth.tar

### Result (accuracy)
|Public|Private|Final|
|:---:|:---:|:---:|
|0.74018|0.72933|0.73253|

### Result (time)
0.0788 sec per one test image