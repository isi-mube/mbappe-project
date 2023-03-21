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
* **Libraries** We decide to not `import math`; our matematical operations come from `numpy` and we don't want unnecesary code.
* **Functions** Erased some of the extra-functions to keep it nice and simple.
* **Features:** We will drop `hits` even if it's a numerical, since it represents the popularity of a player used or watched in FIFA21 community. With that, we also deal with `v1` `hits` outliers issue. Total features in v2; `22`.
* **Plots:** Have been improved.
* **Linear Regression:** For this final version, we will only import `ElasticNet` for our Linear Regression model. Go to [v1](https://github.com/isi-mube/iron-labs/tree/main/project-mbappe) code to see all previous results with `Linear Regression`, `Lasso`, `Ridge` and `ElasticNet`.
* **Size:** Compared to v1, we reduced the amount of lines (from 8.186 to 4808). The final python script size is `1.54 MB`

## Results & Discussion
* R2 =  0.9933
* RMSE =  0.5205
* The value of the metric MSE is  0.2709
* MAE =  0.4092

The **choice** of using **ElasticNet** over Linear Regression was not strictly required and initially happened by **mistake**. As a result, our updated model produced slightly more realistic outcomes compared to the previous [v1](https://github.com/isi-mube/iron-labs/tree/main/project-mbappe) Linear Regression model, which returned perfect predictions (R2 of 1.0).

`v1/v2` ** detailed comparision**:
* R2 increased from 0.9908 to 0.9933, a 0.0025 improvement.
* RMSE decreased by 0.0259, from 0.5464 to 0.5205.
* MSE decreased by 0.0276, from 0.2985 to 0.2709.
* MAE decreased by 0.0199, from 0.4291 to 0.4092.

Throughout this final version, we expanded our knowledge on regression methods, focused on basics (libraries, functions...) and improved our code documentation and visualization.

<p align="center">
  <img src="https://user-images.githubusercontent.com/90038586/226585162-6dd8e0dc-aa72-4867-a348-76316aca3553.png"/>
</p>

## Tools
**Enviornment**
* VSCode and Jupyter Notebook

**Libraries**
* **File management:** os
* **Data manipulation:** pandas
* **Numerical operations:** numpy
* **Visualization:** matplotlib, seaborn
* **Settings:** warnings
* **Machine Learning:** scikit-learn
* **Preprocessing:** LabelEncoder, MinMaxScaler
* **Model election:** train test split
* **Regression model:** ElasticNet
* **Metrics evaluation:** r2 score, mean squared error, mean absolute error

## Future development...
* Incorporate additional datasets to improve the model.
* Enhance the README file to provide more comprehensive and visual documentation. Also, to justify all text.

## BONUS
Entropy happens. We have a glitch in our code if you're visualizing it on GitHub.

![image](https://user-images.githubusercontent.com/90038586/226587768-239a6605-ac15-4ae0-93e2-3d8bf2d7d82b.png)

For readability, please download the notebook and open the code in Jupyter/VSCode.

