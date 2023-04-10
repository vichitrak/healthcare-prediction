# healthcare-prediction

This project aims to reduce the MAE of a real life healthcare dataset using various data processing, feature selection and regression methods.  

Training Dataset: 432600 rows, 18 columns  
Test Dataset: 103500 rows, 16 columns

Baseline Model: Lasso Regressor(alpha=0.1)  
Baseline MAE: 5.4 (validation dataset)

Final Model: SVR Regressor  
Final MAE: reduced the MAE to 4.0 on validation dataset and 3.7 on full test dataset

Interesting Fact and Data Transformation: It was observed that for one observation, only four columns were changing, values in other columns were fixed.
Hence, data was transformed to create a wide dataframe on observation level, converting every value in continuous variables a columns.  

For example:  
`col1, col2, col3, col4`  
`1, a, 2, b, 5.5`  
`1, a, 2, b, 6.5`  
`1, a, 2, b, 7.5`  
`1, a, 2, b, 8.5`  

Modified Dataset: `1, a, 2, b, 5.5, 6.5, 7.5, 8.5`
