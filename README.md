# MBAPPÉ Project
1. [v2 (current)](https://github.com/isi-mube/mbappe-project/blob/main/notebook/project-mbapp%C3%A9.ipynb)
2. [v1](https://github.com/isi-mube/iron-labs/tree/main/project-mbappe)
3. [Original code](https://github.com/isi-mube/data_mid_bootcamp_project_FIFA_MoneyBall)

## About the Project
The objective of this **project** is to identify young soccer players who posses the potential to become **the next Kylian Mbappé**. The [original](https://github.com/isi-mube/data_mid_bootcamp_project_FIFA_MoneyBall) project was completed in 5 days in collaboration with my fellow Ironhack classmates, [Nati](https://github.com/natnaelfe) & [Hugo](https://github.com/HugoIronhack).

This repository is designed to improve my knowledge, redifining the Linear Regression Model, data cleaning processes and functions.

## About the Dataset
After reading the [documentation](https://www.kaggle.com/datasets/ekrembayar/fifa-21-complete-player-dataset?select=fifa21_male2.csv) we decided to proceed with the following **strategy**:

1. The majority of the data types are **numericals**, so we will work with that to make a Linear Regression model.
2. The **target** for our dataset it will be the `OVA` (overall score) of a player.
3. Through **Exploratory Data Analysis** we will identify the features that contribute to this prediction.

## Changes
`v1` (16/20/2023)
* **Libraries:** This time, we use `os` to be proficent with other ways of opening the data. Also, they were re-organized for readibility.
* **Functions:** The following functions were added `data_info`, `clean_columns`, `check_null_cols`, `check_nan_cols` & `is_significant` to improve our workflow.
* All the work has been documented, explaining everystep and avoiding redudancy
* The project's **size** has been reduced, making it more readble and efficent. From 1.45 MB (7.265 lines) to 904 KB (8.184 lines)
* **Cleaning the Data:** step had been improved and simplified. We added some extra code for visualization of the changes.
* **Plots:** Still not my strongest point. Normalization plots had been improved, also the Linear Regression results.
* **Rounding after normalization** in this case, we did not round our numericals.

`v2` (20/03/2023)
* We decide to not `import math`; our matematical operations come from `numpy` and we don't want unnecesary code.
* For this final version, we will only import `ElasticNet` for our Linear Regression model. Go to [v1](https://github.com/isi-mube/iron-labs/tree/main/project-mbappe) code to see all results (`Linear Regression`, `Lasso`, `Ridge` and `ElasticNet`).
* We will drop `hits` even if it's a numerical, since it represents the popularity of a player used or watched in FIFA21 community. With that, we also deal with `v1` `hits` outliers issue.

## Results and Discussion
R2 =  0.9927
RMSE =  0.5191
The value of the metric MSE is  0.2695
MAE =  0.4056

The **choice** of using **ElasticNet** over Linear Regression was not strictly required and initially happened by **mistake**. As a result, our updated model produced slightly more realistic outcomes compared to the previous Linear Regression model, which returned perfect predictions (R2 of 1.0).

v1/v2 comparision:
* R2 increased from 0.9908 to 0.9927, a 0.0019 improvement. The updated model now explains 99.27% of the variance in the target variable, up from 99.08%.
* RMSE decreased by 0.0273, from 0.5464 to 0.5191, indicating better performance in the updated model.
* MSE decreased by 0.0290, from 0.2985 to 0.2695, suggesting improved model performance.
* MAE decreased by 0.0235, from 0.4291 to 0.4056, meaning the updated model has fewer errors in its predictions.

<p align="center">
  <img src="https://i.ibb.co/4MWRKCs/226477449-8d283183-59e7-4352-b190-18b88a88d889.png"/>
</p>

## Future development...
* Incorporate additional datasets to improve the model.
* Enhance the README file to provide more comprehensive and visual documentation.
