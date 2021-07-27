---
title: "Predict the PV Power Generation"
excerpt: "DACON Time Series competition: Predict PV Power Generation"
collection: portfolio
---

- **Who**: the solo- & side-project
- **When**: July 5th 2021 - July 26th 2021
- **Where**: [DACON Time Series Prediction Competition](https://dacon.io/competitions/official/235680/overview/description) for AI/ML, section in "Predict the PV Power Generation".
  - **Dataset**: [Dacon dataset](https://dacon.io/competitions/official/235680/data)
- **What**: Prediction the pv power generated in next 2 days based on the weather information of 7 days.
- **How**: TensorFlow 2.x. Feature engineering to obtain the reasonable feature based on the given features. Stacking(Ensemble) of MLP, LSTM, CNN(Conv1D), CNN-LSTM, LGBM, RF models. Using the pinball loss. Quantile regression. Rectified Adam + LookAhead optimizer.
- **Learn**: SOTA optimizer(RAdam + Lookahead). Quantile Regression. Pinball loss. Ensemble/Stacking of ML/DL models. Feature engineering to get the meaningful information from the given features in the PV power generation. Combined model of CNN & LSTM in the sequential.
- I got the 18th position in the public LB, and finally ranked at the 3rd of private LB, but it's not officialy counted because I submitted this after the end of competition period. The motivation for joinging this terminated-competition was that I have done the very similar ML task from NREL hiring process, but there was no ranking chart/verification for ML task at the hiring process. I needed to check where I was and how I was doing well. 
- The used models (stacking and ensemble), data preprocessing method, feature engineering method, prediction method/rule, and requested loss function(pinball loss) were very similar between in DACON and NREL.
  * Models: Sequential CNN(two for Conv1D layers with LayerNormalized input), Sequential FC(two for Dense layers with l2 regularizers and LayerNormalized input), LSTM (one for LSTM layer with LayerNormalized input), Sequentially connected CNN-LSTM layer(two for Conv1D layers and one for LSTM layer with LayerNormalized input), LGBM(bagging_fraction and feature_fraction were used), and RF(feature_fraction and bagging were used). Totally, 4 (DL models) * 9 (# of quantile) * 2 (separately targeted days) models from deep learning and 2 (separately targeted days) * 9 (# of quantile) models from LGBM, and 2 RF models were ensembled with the linear meta model, which is the one FC layer with LayerNormalized input. That is to say, 54 models in total, each of 54 models are expected to extract similar but different features from input data, therefore the ensembling will improve accuracy.
  * Score: 1.79292 (Public) / 1.99349 (Private)

- **Note**: I cannot open the dataset I received from NREL and submitted code, but I just uploaded the DACON dataset and code I submitted. 

<!-- ![데이콘](https://user-images.githubusercontent.com/58493928/116183247-67d09d00-a6d2-11eb-93b4-aa0c594e1781.png)
- Through SOTA model evaluations without using pre-trained weights, I ranked the 21st-rank before 14 days to the deadline of submission, and I ranked at 49th of Private LB among 876 participants. This is because I didn't use the Ensemble/stacking models, and stopped submission by updating codes (due to family issues).
- The winner codes used the ensemble/stacking methods.
- [The repository](https://github.com/haenara-shin/DACON_EMNIST.git) is opened to the public. My own codes were written in UCSD-Datahub server, but forgot to download it from there, so it was deleted.
 -->
