# Datium Insights Sales Price Regression
This Jupyter Notebook report has been created to explore developing a Regression model for Car Sales prediction.

## Get Started
To get started with the project, follow the steps below:

### 1. Clone the Repository
Open your terminal to clone the project repository from GitHub:
```bash
git clone https://github.com/nlpguy2022/datium_assessment.git
```
and then navigate to the project root directory:
```bash
cd datium_assessment
```

### 2. Set Up the Environment
Make sure you have **Python 3.10+** installed.    
- Create a Python virtual environment:
    ```
    python -m venv venv
    ```
- Activate the environment:
    ```
    source venv/bin/activate
    ```
    For Windows:
    ```
    venv\Scripts\activate
    ```
- Install the necessary packages
    ```
    pip install -r requirements.txt
    ```

### 3. Data & Reports
Original data tab separated in .rpt format:
1. 01_DatiumTrain.rpt
2. 02_DatiumTest.rpt

There is an engineered feature dataframe for Colour, as it uses expensive processing. It can loaded in using pd.merge().
1. ColorGroups.csv

The processed datasets with feature engineering are in the following files:
1. FeatureDF.csv: for the training data
2. TestDF.csv: for the test data

- You can refine the existing model (RFRegressor with current R2 of 0.85 by adding to the existing featuresets.)

### 4. Evaluation & Conclusion
1. Carefully selecting the data is crucial, evident with the fact that we had relatively good performance only using 4 input features (NewPrice, KM per Year, Aging and RelativePower) to model car depreciation to predict sales price.
2. Feature engineering was important to deal with multicollinearity and to have better representations of the data for the model to learn from. 3/4 of the features in the model's featureset were feature engineered.
3. I did not have time to look at the categorical features to train the model, and perhaps I could build a pipeline in order to evaluate these features and the extent to which they can improve the model performance, while also balancing complexity.
4. I did not fine tune the RFRegressor model, which can be an extension to further improve model performance (n_estimators, max_depth, max_features).

Ultimately, I believe that carefully curating features to define my car depreciation model was key to ensuring that the model had good performance with minimal complexity, pointing out that even relative understanding of the business domain can lead to valuable insights into predicting car price.