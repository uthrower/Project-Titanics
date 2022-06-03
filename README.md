# Project-Titanics
Random forest model on classic Titanics dataset, with a C++ twist - inspired by PredictNow.ai (Dr. Ernest Chan)
  
## Overview
* This is a feasibility study towards future development in leveraging machine learning models in developing quantitative trading strategies
* Random forest model was chosen mainly because of its generally lower risk of over-fitting for small datasets, and it is great for performing feature-based analysis
* Classic Titanics dataset is used for simplicity, 89% accuracy was recorded after minimal tuning hyper parameters
* Model is first built in R, output to flat file, parsed with C++, and eventually compiled as `.dll` and imported into MQL4
  
## Modelling in R
* Dataset was downloaded from [Kaggle](https://www.kaggle.com/c/titanic), I have uploaded [here](https://github.com/urinethrower/Project-Titanics/blob/main/titanic.csv)
* Dataset was parted into training and testing sets, to avoid over-fitting
* Hyper perameters like mtry and ntrees are visualised and tuned accordingly:
![ntrees](https://user-images.githubusercontent.com/106392189/171839711-84ca8a9b-58d0-457f-ac22-7ef443f000e5.png)
![mtry](https://user-images.githubusercontent.com/106392189/171839746-6ba82794-5425-471a-842e-9f25d27a1173.png)
  
* Sex (M/F) is the most important feature in prediction, which is in line with other ML models on this dataset. Following are the importance plot and confusion matrix:  
  
<img src="https://user-images.githubusercontent.com/106392189/171841472-1ef4d16e-7a55-4171-a61a-f2797e2e7fa0.png" alt="https://user-images.githubusercontent.com/106392189/171841472-1ef4d16e-7a55-4171-a61a-f2797e2e7fa0.png" width="410" height="397"></img>
<img src="https://user-images.githubusercontent.com/106392189/171841501-3398e479-3406-4085-a0d0-7fc7933f2a8e.png" alt="https://user-images.githubusercontent.com/106392189/171841501-3398e479-3406-4085-a0d0-7fc7933f2a8e.png" width="367" height="397"></img>  
* Following my codes, the final step is the model export in `.csv`, uploaded [here](https://github.com/urinethrower/Project-Titanics/blob/main/titanic_RF.csv)
  
## Parsing with C++
  

## Future directions
* To perform feature-based time-series analysis for trading strategies
* Develop algorithmic trading strategies around random forest model
  
## Resources used
* Using the randomForest package in R: [Dr. Bharatendra Rai](https://www.youtube.com/watch?v=dJclNIN-TPo), [StatQuest](https://www.youtube.com/watch?v=6EXPYzbfLCE)
* Visualising with ggplot2 package: [ramhiser](https://gist.github.com/ramhiser/6dec3067f087627a7a85)
* Visualising with caret package: [Cybernetic](https://stackoverflow.com/questions/23891140/r-how-to-visualize-confusion-matrix-using-the-caret-package)
