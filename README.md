## Loss Severity Analysis on Single Family Residential Mortgage Loans

Course Code: FIM 500
North Carolina State University
Special Thanks to Matthew Lasater, Damon Chengelis, Sean McManus from Arch for their instructions and guidance

### Brief Description

This Repository contains most the of project code that were used to complete the project. For the visualization part, Tableau was utilized so no corresponding code will be recorded here.

In this project, we went through a typical model development and validation cycle with multiple round of redesign and experiment before reaching our final model. Owing to the development process, some of the intermediate code was overwritten and cannot be recovered simply via my memory.

The main programming language we utilize is Python with some common packages like Scikit-Learn being utilized. Some small-scaled dataset operation and validation were carried using Excel. Comments could be found throughout the python file which I believe are self explanatory.   

### File Hierarchy

The file hierarchy in this repository mimics the real one we used for the project implementation but the actual data file and some processed results are excluded owing to the file size restrictions.

The project repository will be divided into raw data directory, processed data directory, visualization directory and code directory.

### Workflow 

The basic workflow of our project could be found as below. Actually during the development stage we kind of jumped back and forth between some steps as we needed to observe the result before making any change.

1. Retrieving Data
2. Eyeballing Data
3. Cleaning Data
   - Handling Missing Value 
   - Filtering Unrelated Field
   - Univariate Analyzing and Outlier Handling
   - Business Knowledge Based Filtering   
4. Processing Data
5. Model Fitting 
6. Revision and Transformation
7. Performance Examination and Result Visualization
8. Presentation and Report

### Data Source

For the mortgage performance data, Fannie Mae single family mortgage data from 2000 to 2020 were used. The dataset has more than 100 fields and provides the time series for each mortgage recorded by Fannie Mae until each individual mortgage was closed. For this project, most of the time we only cared about the very last entry of each mortgage since we are trying to use a linear model to predict the loss severity base on most recent observable data before the mortgage was actually closed.

To integrate some macroeconomic indicator, the house price index from FHFA were utilized which contains house price index on a national, state, MSA or zip code level.  The timestamp contained in both dataset were used to merge them into one final dataset which was used to fit the model.

### Model Specification

Given that this project's main target is to get ourselves familiar with group-work setting and model development cycle, simple ordinary linear regression was chosen to avoid any unnecessary technical overhead. At the end of the project, we try to use discretization and spline-like approach to capture some nonlinearity in the mapping which could be further explored in the future. The model will take some variables as input and yield a LGD ratio as output, which was compared against the real loss severity to examine the model accuracy. At the end, we constructed a model with R-square around 0.28 and RMSE around 0.29.

### Conclusion

### Further Inquiry
