# Kaggle-ML-auto-complete-recommeder-challenge-using-KNN.

Building an auto-complete feature for citizen science checklist submissions(Group project)

In this project we try to create a recommender system that can be used to impute the missing values in the ebirds data set.we work with the training data set which has complete and accurate 
values and use that to train our algorithim which then is used to recommend possible bird values in the test data set where we have soft zero values.

## Preprocessing data

first both data sets are scaled to have values between zero and one and we created new scaled data sets scaled_training1 and scaled_test1

**function to scale data so that all values in a column add up to 1**

def scale(df):

    """Normalize all columns in a DataFrame so that their values add up to 1"""
    
    for column in df.columns:
    
        column_sum = df[column].sum()
        
        df[column] = df[column] / column_sum
        
    return df

  more details on prepocessing can be seen in the project file...
    
## functions created for the project

A number of functions were created to help in runing the algorithim to ensure that it does what it is expected to do e.g functions to calculate euclidean distance, cosine distance,
function to get the k nearest neighbors and the recommender function that returns the recommendations based on the training data, test data and k values.
