---
title: "Predicting crystal structure from X-ray diffraction"
excerpt: "NANO 281 Fall 2020 Lab3 InClass Competition: Predicting bravais lattice from XRD"
collection: portfolio
---

- This is the solo- and in-class Kaggle competition that I took the class in the [NANO 281 Fall 2020 Lab3](https://www.kaggle.com/c/nano281fa2020/leaderboard).
- This Kaggle competition winner code was written in TensorFlow 2.x. All EDA and preliminary ML approach were implemented in advance. 
- The dataset comes from [Crystallography Open Dataset](http://www.crystallography.net/cod/) (open to the public, but simply downloadable from the Kaggle).
- Through several testing with hyperparameter optimized ML models including Boosting (LightGBM, CatBoost, XGBoost, and others) Bagging(RandomForest, and ExtraTrees) and others, the best accuracy was achieved from 1D-CNN structure. Based on the 1D-CNN models with 3-step fine tuning and CV-stacking(n-folds: 40), I hitted the 2nd-place in the public leader board, and finally ranked 1st-place in the private leader board!
- The result was built on the 'no augmented dataset' and 'no ensemble with other ML models.' I believe there are spaces to enhance the accuracy if we can add more dataset (augmentation) or ensemble with CNN, LightGBM, and RandomForest. LightGBM is very powerful model with this structured dataset, and I confirmed its promising performance in the ML model testing. 
- [The repository](https://github.com/haenara-shin/NANO281_Labs/tree/main/3) is under the private. Please contact me if you want to see in detail.
