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
- **How**: TensorFlow 2.x (Conv-1D). CV-Stacking. Ensemble. Scikit-learn. LightGradientBoost. CatBoost. XGBoost. AdaBoost. RandomForest. Data transformation (n-root transformation). 3-step fine-tuning(Adam_custom, Adamax, Adadelta) of self-building models. Learning rate control(Reduced learing rate on the plateau).
- **Learn**: Handling structured-type dataset (table data). Building Conv-1D structure from the scratch. Statistically data analysis. Data augmentation method for XRD dataset.

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

- Featured slides
![xrd_1](https://user-images.githubusercontent.com/58493928/117560118-d81adf00-b03f-11eb-9bb6-83bd29766062.png)
![xrd_2](https://user-images.githubusercontent.com/58493928/117560124-e49f3780-b03f-11eb-9263-673a38602853.png)
![xrd_3](https://user-images.githubusercontent.com/58493928/117560129-ef59cc80-b03f-11eb-98da-b299bab5c135.png)
![xrd_4](https://user-images.githubusercontent.com/58493928/117560132-f8e33480-b03f-11eb-89ff-cc25947ff483.png)
![xrd_5](https://user-images.githubusercontent.com/58493928/117560136-013b6f80-b040-11eb-8ce5-332ff62491cb.png)
![xrd_6](https://user-images.githubusercontent.com/58493928/117560140-08627d80-b040-11eb-85f0-c0dcdd3e2ed7.png)
![xrd_7](https://user-images.githubusercontent.com/58493928/117560193-7018c880-b040-11eb-9cbe-f9391a15dd54.png)
![xrd_8](https://user-images.githubusercontent.com/58493928/117560199-7c9d2100-b040-11eb-910e-fef21585f301.png)

- Models' backbone structures with FC-layers
![p16](https://user-images.githubusercontent.com/58493928/117560204-845cc580-b040-11eb-9268-c55e110f973f.png)
![p19](https://user-images.githubusercontent.com/58493928/117560209-8cb50080-b040-11eb-8c06-f9d44f64a143.png)

- Models' backbone structures with GAP layer
![p16_GAP](https://user-images.githubusercontent.com/58493928/117560214-93437800-b040-11eb-91f0-8d98f51badf6.png)
![p19_GAP](https://user-images.githubusercontent.com/58493928/117560223-9b9bb300-b040-11eb-9275-9e74cebb6444.png)
