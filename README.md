# Salaries EDA using Pandas
In this project, we will explore the San Francisco city employee salary dataset using Pandas library. The dataset can be found on Kaggle and it contains information about city employee salaries in San Francisco from 2011 to 2014. 

The following are the main steps we will take in this project:

* Import the Pandas and NumPy libraries.
* Read the Salaries.csv file as a Pandas dataframe.
* Use the .info() method to find out how many entries there are in the dataset.
* Use the .describe() method to get descriptive statistics of the dataframe.
* Answer several questions about the data to extract insights from it.

## Dataset
The dataset is a CSV file containing 148,650 records with 13 columns:

* Id: employee ID
* EmployeeName: employee name
* JobTitle: job title
* BasePay: base pay
* OvertimePay: overtime pay
* OtherPay: other pay
* Benefits: benefits
* TotalPay: total pay
* TotalPayBenefits: total pay including benefits
* Year: year of payment
* Notes: additional notes
* Agency: agency for which payment was made
* Status: status of employee (FT = full-time, PT = part-time)

## Questions and Answers

The following questions were answered using Pandas functions:


* What is the average BasePay?
* To answer this question, we used the .describe() method to get the descriptive statistics of the 'BasePay' column, and then we used .dropna(), .replace(), .dropna(), and .astype() methods to clean the data and get the mean of the 'BasePay' column. The answer is: 66325.44884050643.


* What is the highest amount of overtimePay in the dataset?
* To answer this question, we used .dropna(), .replace(), .dropna(), and .astype() methods to clean the data and get the maximum of the 'OvertimePay' column. The answer is: 245131.88.


* What is the job title of JOSEPH DRISCOLL? Note: Use all caps, otherwise you may get an answer that doesn't match up.
* To answer this question, we used boolean indexing to filter the rows that have 'EmployeeName' equal to 'JOSEPH DRISCOLL' and then selected the 'JobTitle' column. The answer is: CAPTAIN, FIRE SUPPRESSION.


* How much does he make? (including benefits)
* To answer this question, we used boolean indexing to filter the rows that have 'EmployeeName' equal to 'JOSEPH DRISCOLL' and then selected the 'TotalPayBenefits' column. The answer is: 270324.91.


* What is the name of the highest paid person (including benefits)?
* To answer this question, we used boolean indexing to filter the row that has the maximum value in the 'TotalPayBenefits' column and then selected the 'EmployeeName' column. The answer is: NATHANIEL FORD.
 
 
* What is the name of the lowest paid person (including benefits)? Do you notice something strange about how much he or she is paid?
* To answer this question, we used boolean indexing to filter the row that has the minimum value in the 'TotalPayBenefits' column and then selected all columns. We noticed that the employee has a negative 'TotalPayBenefits' value, which means they have debts instead of being paid.


* What was the average (mean) TotalPay of all employees per year? (2011-2014)
* To answer this question, we used the .groupby() method to group the data by year and then applied the .mean() method to get the mean of the 'TotalPay' column for each year.


* How many unique jobs are there?
* To answer this question, we used the .unique() method to get the unique job titles and then used .nunique() method to get the number of unique job titles. The answer is: 2159.


* What are the top 5 most common jobs?
* To answer this question, we used the .value_counts() method to get the frequency of each job title, and then selected the top 5 most frequent job titles.


## Conclusion
Through the use of Pandas functions, we were able to answer a variety of questions about the salaries dataset and extract valuable insights. This project demonstrates the power and flexibility of Pandas for data exploration and analysis.
