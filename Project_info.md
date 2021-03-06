### Introduction

Housing costs demand a significant investment from both consumers and developers. 
And when it comes to planning a budget—whether personal or corporate—the last thing anyone needs is uncertainty about one of their biggets expenses. 

Soviet bank, Russland’s oldest and largest bank, helps their customers by making predictions about realty prices so renters, developers, and lenders are more confident when they sign a lease or purchase a building.

Although the housing market is relatively stable in Russland, the country’s volatile economy makes forecasting prices as a function of apartment characteristics a unique challenge. Complex interactions between housing features such as number of bedrooms and location are enough to make pricing predictions complicated. Adding an unstable economy to the mix means Soviet bank and their customers need more than simple regression models in their arsenal.

You have just been hired as the Lead Data Analyst at Soviet Bank to develop algorithms which use a broad spectrum of features to predict realty prices. Competitors will rely on a rich dataset that includes housing data and macroeconomic patterns. An accurate forecasting model will allow Soviet bank to provide more certainty to their customers in an uncertain economy.


### Evaluation:

Submissions are evaluated on the RMSLE (Root Mean Squared Log Error) between their predicted prices and the actual data. The target variable, called price_doc in the training set, is the sale price of each property.

'''copy and use the metric below'''

from sklearn.metrics import mean_squared_log_error
def RMSLE(y_true:np.ndarray, y_pred:np.ndarray):
    """
        The Root Mean Squared Log Error (RMSLE) metric 
        
        :param y_true: The ground truth labels given in the dataset
        :param y_pred: Our predictions
        :return: The RMSLE score
    """
   return np.sqrt(mean_squared_log_error(y_true, y_pred))


### Target Variable:

The aim of this competition is to predict the sale price of each property. The target variable is called price_doc in train.csv.

The training data is from August 2011 to June 2015, and the test set is from July 2015 to May 2016. The dataset also includes information about overall conditions in Russland's economy and finance sector, so you can focus on generating accurate price forecasts for individual properties, without needing to second-guess what the business cycle will do.



### Data Files

train.csv, test.csv: information about individual transactions. The rows are indexed by the "id" field, which refers to individual transactions (particular properties might appear more than once, in separate transactions). These files also include supplementary information about the local area of each property.

macro.csv: data on Russia's macroeconomy and financial sector (could be joined to the train and test sets on the "timestamp" column)
sample_submission.csv: an example submission file in the correct format
data_dictionary.txt: explanations of the fields available in the other data files
