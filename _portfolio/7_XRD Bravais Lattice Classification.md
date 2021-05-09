---
title: "Predicting crystal structure from X-ray diffraction"
excerpt: "NANO 281 Fall 2020 Lab3 InClass Competition: Predicting bravais lattice from XRD"
collection: portfolio
---
![nano281_2](https://user-images.githubusercontent.com/58493928/116186958-766e8280-a6d9-11eb-82d4-f58fdd3f2db8.png)
- **Who**: the solo- and in-class Kaggle competition project
- **When**: Sept. 2020 - Mar. 2021
- **Where**: [NANO 281 Fall 2020 Lab3](https://www.kaggle.com/c/nano281fa2020/overview)
- **What**: Prediction the crystal structures (14 bravais lattice) from table-type XRD data
  - **Dataset**: [Crystallography Open Dataset](http://www.crystallography.net/cod/) (open to the public, but simply downloadable from the Kaggle)
- **How**: TensorFlow 2.x (Conv-1D). CV-Stacking. Ensemble. Scikit-learn. LightGradientBoost. CatBoost. XGBoost. AdaBoost. RandomForest. Data transformation (n-root transformation).
- **Learn**: Handling structured-type dataset (table data). Building Conv-1D structure from the scratch. Statistically data analysis. Data augmentation method for XRD dataset. 3-step fine-tuning(Adam_custom, Adamax, Adadelta) of self-building models. 

![nano281](https://user-images.githubusercontent.com/58493928/116184306-5e483480-a6d4-11eb-9ed9-b540345599d6.png)
- Through several testing with hyperparameter optimized ML models including Boosting (LightGBM, CatBoost, XGBoost, and others) Bagging(RandomForest, and ExtraTrees) and others, the best accuracy was achieved from 1D-CNN structure. Based on the 1D-CNN models with 3-step fine tuning and CV-stacking(n-folds: 40), I reached at the 2nd-place in the public LB, and finally ranked 1st-place in the private LB! Yeah!
- The result was built on the 'no augmented dataset' and 'no ensemble with other ML models.' I believe there are spaces to enhance the accuracy if we can add more dataset (augmentation). LightGBM was very powerful model with this structured dataset, but my self-built pseudo VGG16 model showed the better performance.
- [The repository](https://github.com/haenara-shin/NANO281_Labs/tree/main/3) is opened to the public, but not including the [entire materials and information](https://github.com/haenara-shin/XRD_ML.git). This is because the project is still going on, and its proprietary is under Prof. Ong, even though I am one of the contributor to this repository and project. Please contact me if you want to see in detail.

- After the Kaggle competition, following techniques were added, merged, and enhanced the original codes. All makes the siginificant performace enhancement to show the 92.5% classification accruacy. 
  - (1) Data augmentation - from class-mate
  - (2) ICSD dataset - dataset quality improved (from class-mate)
  - (3) Deeper model built with shorter FC layers - from pseudo VGG16 to pseudo VGG19
  - (4) Global Average Pooling layers for bottom layers - replaced FC layers
  - (5) Data transformation (n-root transformation)

![nano281_3](https://user-images.githubusercontent.com/58493928/116186985-85553500-a6d9-11eb-976b-fa1a05c8688c.png)
