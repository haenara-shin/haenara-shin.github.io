---
title: "Predict the PV Power Generation"
excerpt: "DACON Time Series competition: Predict PV Power Generation"
collection: portfolio
---

- **Who**: the solo- & side-project
- **When**: July 2021 - present
- **Where**: [DACON Time Series Prediction Competition](https://dacon.io/competitions/official/235680/overview/description) for AI/ML, section in "Predict the PV Power Generation".
  - **Dataset**: [Dacon dataset](https://dacon.io/competitions/official/235680/data)
- **What**: Prediction the pv power generated in next 2 days based on the weather information of 7 days.
- **How**: TensorFlow 2.x. Feature engineering to obtain the reasonable feature based on the given features. Stacking of MLP, LSTM, CNN(Conv1D), CNN-LSTM, LGBM, RF models. Used the pinball loss. Quantile regression. Rectified Adam + LookAhead optimizer.
- **Learn**: SOTA optimizer(RAdam + Lookahead). Quantile Regression. Pinball loss. Ensemble/Stacking of ML/DL models. Feature engineering(selection) to get the meaningful information from the given features in the PV power generation.

- **Note_1**: It's still going on, and this is very similar to the NREL and other PV companies ML task for hiring process I have applied for. (Tasks cannot be opened to the public, but it's very similar with this competition.)
- **Note_2**: The repos. may be opened to the public in the end of July 2021 (or not). The result and backbone structure will be posted after the task.

<!-- ![데이콘](https://user-images.githubusercontent.com/58493928/116183247-67d09d00-a6d2-11eb-93b4-aa0c594e1781.png)
- Through SOTA model evaluations without using pre-trained weights, I ranked the 21st-rank before 14 days to the deadline of submission, and I ranked at 49th of Private LB among 876 participants. This is because I didn't use the Ensemble/stacking models, and stopped submission by updating codes (due to family issues).
- The winner codes used the ensemble/stacking methods.
- [The repository](https://github.com/haenara-shin/DACON_EMNIST.git) is opened to the public. My own codes were written in UCSD-Datahub server, but forgot to download it from there, so it was deleted.
 -->
