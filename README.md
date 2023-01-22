# ML-sample-questions
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
>Question 1-

The dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective is to diagnostically predict whether a patient is diabetic or not, based on diagnostic measurements included in the dataset. Create a classification model using AdaBoost Algorithm and GradientBoost Algorithm. Use grid search to find the optimal value for the hyperparameters: learning_rate, n_estimators, and random_state.

 

Dataset:

diabetes_train.csv
diabetes_test.csv
 

 Dataset Parameters:

* Pregnancies: Number of times pregnancies(0-14)
.
.
* Glucose: Glucose Level (0-198)
.
.
* BloodPressure: Diastolic blood pressure (0-122) 
.
.
* SkinThickness: Triceps skin fold thickness (0-52) 
.
.
* Insulin: 2-Hour serum insulin (0-543)
.
.
* BMI: Body Mass Index (0-57.3) 
.
.
* DiabetesPedigreeFunction: Diabetes Pedigree 
.
.
* Function(0.078-2.288)

.
.
* Age: Age of Patient (21-81)
Outcome: Patient is diabetic or not (0 or 1)
 

Tasks to be Performed:

 

1. What are the optimal values for learning_rate and n_estimators? (**Calculate the optimal values for AdaBoost)

 

Example: If 1 and 100 are optimal values then the output should be:

Output:   1 , 100                                                                               

Hint: Take hyperparameters as: 

learning_rate: 0.3 to 1 step 0.3
n_estimators: [50,100]
random_state: 42
Note: Use only the above-mentioned parameters

Note: For checking the optimal parameters, use GridSearchCV (cv=5)

2. Calculate the below precision values for both models( ADA Boost and GradientBoost) and find the larger value between them(up to 2 decimal places):

Accuracy 
Sensitivity
Specificity
 

Example:

If the precision values of AdaBoost are:

Accuracy: 80.0 
Sensitivity: 40.12
Specificity: 30.34
 And the precision values of GradientBoost are:
Accuracy: 90.0
Sensitivity: 50.56
Specificity: 20.78
 

 Then the output should be:

 

Output: 90.0, 50.56, 30.34

 Hint: Use the confusion matrix to calculate the above values and round off the output up to two decimal places.

 

Final Output Sample:

1, 100, 90.0, 50.56, 30.34

NOTE: Here, The multiple answers are separated by a comma.

NOTE: Don't use train_test_split as the training and testing data is provided separately

Input Format: 

The first file ‘diabetes_train.csv’ contains data as mentioned in the problem to train the models. The file is in *.csv format and is present at the location res/diabetes_train.csv.
The second file ‘diabetes_test.csv’ contains data as mentioned in the problem to test the models. The file is in *.csv format and is present at the location res/diabetes_test.csv.
 

Output Format:

Perform the above operations and write answers to all queries asked in the questions to a file named output.csv.
Each answer should be separated by a comma.
Your file output.csv should be present at the location output/output.csv.
**NOTE: For using GradientBoost use: from sklearn.ensemble import GradientBoostingClassifier and for AdaBoost use: from sklearn.ensemble import AdaBoostClassifier
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Question 2

Problem Statement:

 

You are provided with a data set named “Retail.csv”, you have to perform market basket analysis on the dataset. Apply the Apriori algorithm and association rules using appropriate parameters.


Dataset: Retail.csv


Dataset Parameters: 

POS Txn : Transaction ID
Dept: Department
ID: Item ID
Sales U: Units sold
 

      1. Remove the ‘0999: UNSCANNED ITEMS’ from the ‘Dept’ column and print number of times ‘0973:CANDY’ sold.
 

Example: If the number of times ‘0973:CANDY’ was sold 100 times then the output should be:

Output: 100

Hint: We need to find the number of times ‘0973:CANDY’ was sold not total units sold.

 

      2. For the Frequent Itemsets, keep the minimum support as 0.02 and find maximum support. (up to 5 decimal places) 

Group the data by POS Txn
Get all the itemsets for each group in a list(itemsets)
Use TransactionEncoder() to transform the list(itemsets)
Convert the tranformed list to a dataframe using:
transformed_df = pd.DataFrame(transformed_list, columns=transformed_list.columns_)
 Apply the apriori algorithm using parameters:
transformed_df, min_support=0.02, use_colnames=True
Find the max_support upto 5 decimal places
Example: If maximum support is 0.54321 then the output should be:

Output: 0.54321

Hint: Get rules using the “lift” Metric having minimum_threshold as 2 

 

      3. Filter rules having lift>=3  and confidence >=0.1 and calculate the total number of rules and filtered rules. 
 

Example: If the total number of rules is 40 and the number of filtered rules is 20 then output should be:

Output: 40, 20


HINT: You need to perform pre-processing using TransactionEncoder.
 

Final Output Sample:

100, 0.54321, 40, 20

 

NOTE: Here, The multiple answers are separated by a comma.

 

Input Format: 

The first file ‘Retail.csv’ contains data as mentioned in the problem. The file is in *.csv format and is present at the location res/Retail.csv.
 

Output Format:

Perform the above operations and write answers to all queries asked in the questions to a file named output.csv.
Each answer should be separated by a comma.
Your file output.csv should be present at the location output/output.csv.
***Note: Write the code only inside the solution() function and do not pass any additional arguments. For predefined stub refer stub.py. This question will be manually evaluated and score will be allotted accordingly*** 

Sample Output:

If you get this output that means your solution is submitted and will be manually evaluated.

 



Less 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
