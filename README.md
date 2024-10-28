
# Competition in Machine learning for socio-technical systems (TPM034a)

Welcome to the technical guidelines for the competition in Machine Learning for Socio-technical Systems (TMP034a). Assignment 01 finalizes with an internal competition in pedicting `Life expectancy`. For doing so, you have to train and predicts country's Life Expectancy given the data set you have been working in this assigment.

In this competition, you have access to two data files in CSV: 
- (1) **train.csv**: This data file includes everything, the dependent variable `Life expectancy`, many explanatory variables, and a `ROW_ID` column. The latter is just a unique identification for the row.
- (2) **predict.csv**: This data file has the exact same format as *train.csv*, but the `Life expectancy` values where removed (i.e., the column is filled with NaN values).

You have to use the data provided in **train.csv** to train a model that can predict the `Life expectancy`. Then, you have to use this model to predict the `Life expectancy` in the **predict.csv** file and fill-in the `Life expectancy` column with your predictions. The evaluation metric will be the mean squared error ([RMSE](https://scikit-learn.org/1.5/modules/generated/sklearn.metrics.mean_squared_error.html)) between the your prediction and the true Life Expectancy.

This competition can give you up to 0.5 grading points in the final grade of the assignment 01. The grading will be based on the ranking of the RMSE of your predictions. The ranking position will be based on the RMSE of the predictions in the **predict.csv** file. The RMSE will be calculated by the Competiton team using the true values of the `Life expectancy` of the **predict.csv** file. The top 10 participants will receive grading points according to the following table:

| Rank | Points |
|------|--------|
| 1    | 0.5    |
| 2    | 0.45   |
| 3    | 0.4    |
| 4    | 0.35   |
| 5    | 0.3    |
| 6    | 0.25   |
| 7    | 0.2    |
| 8    | 0.15   |
| 9    | 0.1    |
| 10   | 0.05   |

The competiton have a web interface where you can submit your predictions and check the ranking. The web interface is available at: [http://class-competitor.tpm.tudelft.nl](http://class-competitor.tpm.tudelft.nl). Please read carefully the technical guidelines below to understand how to submit your predictions.

## Technical Guidelines

1. **Data Files**: You have access to two data files in CSV:
    - **train.csv**: This data file includes everything, the dependent variable `Life expectancy`, many explanatory variables, and a `ROW_ID` column. The latter is just a unique identification for the row.
    - **predict.csv**: This data file has the exact same format as *train.csv*, but the `Life expectancy` values where removed (i.e., the column is filled with NaN values).

2. **Training**: You have to use the data provided in **train.csv** to train a model that can predict the `Life expectancy`. You can use any model you want, and any transformation you think is necessary. You can use any library you want, such as `scikit-learn`, `pandas`, `numpy`, etc.

3. **Submission File**: You have to submit a CSV file with the same format as the **predict.csv** file, but with the `Life expectancy` column filled with your predictions. Use comma as the delimiter. Your file should look like this:

    ```csv
    ROW_ID,Country,Year,Status,Adult Mortality,...,Life expectancy
    0,Argentina,2015,Developing,116.0,...,90
    1,Argentina,2014,Developing,118.0,...,101
    ...
    ````

4. **Submission platform**: You have to submit your predictions in the web interface available at: [http://class-competitor.tpm.tudelft.nl](http://class-competitor.tpm.tudelft.nl). **You can submit up to 10 different predictions**. Please, go to the web platform and follow the instructions for registering and submitting your predictions.

5. **Ranking**: You can check the ranking of the competition in the web interface. The ranking will be based on the RMSE of the predictions in the **predict.csv** file. The RMSE will be calculated by the Competiton team using the true values of the `Life expectancy` of the **predict.csv** file.

6. **Grading**: The top 10 participants will receive grading points according to the table mentioned above. The grading will be based on the ranking of the RMSE of your predictions.
