# Sales Predictions
## How different variables affect sales

**Joshua Nickell**: 

### Business problem:

We need to find out which variables affect the sales the most.

### Data:
The data can be found here: https://docs.google.com/spreadsheets/d/e/2PACX-1vR0TKEXKL-l0SVSGCehXIONnm0wttSHcPqgVceF7dUXcrrk1ClRQXGNCDFm0qWIfNrbCV6uuXWxh9P5/pub?gid=1274198617&single=true&output=csv


## Methods
I decided to drop Item_Identifier, Outlet_Identifier, and Outlet_Establishment_year, as they did not contribute to the sales predictions. 

## Results

#### Sales Based on MRP
![image](https://user-images.githubusercontent.com/85464771/202827982-aeb764b3-5fe1-4c43-bd66-9818b288355c.png)

As MRP rises, so do the sales.

#### Sales of Different Item Types
![image](https://user-images.githubusercontent.com/85464771/202827990-e871e618-76db-4439-888e-7d2a26c34ce4.png)

There is a very slight negative trend in this graph. Item visibilty does not affect sales much, but it appears that sales drop slightly as visibility rises.

#### Coefficients
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/LinearRegression.png)
The three most impactful features are the three types of supermarkets.

#### Feature Importances
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/DecisionTree.png)
The five most important features include the three types of supermarkets, with item MRP at the top.

#### SHAP Barplot
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/SHAPBar.png)
Higher MRP is still at the top, but SHAP shows that visibility, weight, and outlet size may hold some importance.

#### SHAP Dotplot
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/SHAPBar.png)
A high MRP and the outlet type of one of the three supermarkets increased prediction of higher sales.

#### LIME
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/LIMEhigh.png)
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/LIMElow.png)
The lime graphs show the items with high MRP, which increases sales, are mostly in supermarket-1 and low MRP items are mostly in supermarket-3.

#### Force Plot
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/force_high.png)
Items with max MRP push the sales higher, but outlet type supermarket-1 helps as well.
![image](https://github.com/Josh-XS/Sales-predictions/blob/main/images/force_low.png)
Items with minimum MRP lower the sales, but supermarket-3 pushes them significantly higher.

## Model

I decided to use the decision tree regressor because it was the most accurate model
The R2 was around 0.6 meaning that the model could predict 60% of variation in the target.
The RMSE was around 1000, which was lower than the other model, but still not good.
The model would perform OK, but there is some tuning that could be done, or another model that may perform better.

## Recommendations:

I would recommend a random tree model for this data, as the current model is not as accurate as it could be.

### For further information


For any additional questions, please contact **nickelljoshua@gmail.com**
