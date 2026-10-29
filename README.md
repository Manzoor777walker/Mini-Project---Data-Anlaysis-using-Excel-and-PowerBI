# Mini-Project 1
## Data Anlaysis using Excel and Power BI
*This dataset contains detailed information on employees across various departments and countries, capturing key aspects of their employment and performance metrics. It can be used for various HR analytics tasks, such as analyzing salary trends, studying the impact of leaves on productivity, or predicting employee turnover.
*Goal:Creating a dashboard for Employee work Overview, Payroll analysis, Operational Efficiency and Leave Analytics*
# Employees Management Analysis

## Data Cleaning and Data Preparation
                   1.	No Duplicates are found.
                   2.	Missing values like Blankcells, Error, Nullvalue are not found.
                   3.	Correcting inconsistencies data like standardize text format, typos,capitalization,space etc…
                   4.	Checking and verify the outliers.
                   5.	Setting data types for Categorical Data and Numerical Data  
                   6.	Round Down Function Applied for Currency values and Job Ratings column on the data set.
                   7.	In column “Year” is renamed as “Year of Service
                   8.	Using find and replace method to replace ‘&’ instead of ‘/’.
## POWER BI : DATA VISUALIZATION
                   1.	Created a calculated column based on “Job Rate’ and named as ‘Rating ‘
                      	 Formula for creating Rating:- if [Job Rate]=1 then “Very Low”
                         Else if [Job Rate]=2 then  “Low”
                         Else if [Job Rate]=3 then  “Average”
                         Else if  [Job Rate]=4 then “High”
                         Else “Very High”
                   2.	Create a calculated column based on “Years of Service” and named as “upd_Years of service” and the formula used as 
                                •	upd_Years_of_Serv = DATEDIFF(Employees[Start Date],TODAY(),YEAR)
                   3.	Create a calculated column based on “upd_years_of service” and named ‘years Group’ for making group classification by using switch function
                                •	Years_Group = SWITCH(TRUE(),Employees[upd_Years_of_Serv]<=6,"Below 6 year",Employees[upd_Years_of_Serv]<=7,"6-7 years",Employees[upd_Years_of_Serv]<=9,"8-9 years","10 years")


                   4.	Create some Basic measures before Data visualization
                                   •	Total annual salary = SUM(Employees[Annual Salary])
                                   •	Total employees = COUNTA(Employees[First Name])
                                   •	Total_Overtime = SUM(Employees[Overtime Hours])
                                   •	Total_Sick_Leave = SUM(Employees[Sick Leaves])
                                   •	Total_Unpaid_Leave = SUM(Employees[Unpaid Leaves])
                                   •	Overtime_per_employee = [Total_Overtime]/[Total employees] 
                                   •	Average Years of Service = AVERAGE(Employees[upd_Years_of_Serv])
                                   •	Average_Annual_Salary = AVERAGE(Employees[Annual Salary])
                                   •	Average_Job_Rating = AVERAGE(Employees[Job Rate])
                                   •	Average_Monthly_Salary = AVERAGE(Employees[Monthly Salary])
                   5.	Ensuring and fix the data types to Dates.
## Creating Dashboard 

### Workforce Demographics and Employees overview
                   On this page include measures, Button, Insights, Slicer, Linechart, Piechart, Clustered Barchart, Matrix,100% stacked Bar chart.
                           	Line chart : Employee headcount analysis
                           	Piechart: Gender Diversity
                           	Clustered Barchart: Total Employees by Department
                           	100% stacked Bar chart: Gender distribution by department
### Payroll and Compensation Analysis
                   On this page include Measures ,Tree map, Scatter chart ,Stacked column chart,table, Clustered Bar chart, Insights, Button Slicer,Water fall chart, Buttons for Page Navigation and clear filters.
                           	Tree map: Total Annual Salary By Department
                           	Scatter chart: Annual Salary Distribution By Job Rate And Gender
                           	Stacked column chart: Average Annual Salary By Department
                           	Table: Employee  Compensation Detail
                           	Clustered Bar Chart: Total Overtime By Center
                           	Waterfall Chart: Average Annual Salary and Total Annual Salary By Rating And Center.
                           	Button : Page Navigation and Clear filter.
                           	Include Bookmark and visual filtering; Based on center and gender on the Table.
                           	Button slicer : Count of department by country 
### Operational Efficiency And Leave Anlytics

                   On this Page include Measures, Clustered Column Chart , Scatter chart, Clustered Bar chart, Line and stacked Column Chart,Table, Insights,Slicer,Button

                           	Clustered Column chart:Total Sick leave, Unpaid Leave And Overtime By Department
                           	Scatter Chart: Sick Leave Distribution By Years  of Service.
                           	Line and stacked Column Chart: Total Sick Leave and Total Unpaid leave by Department.
                           	Table: Employee Detail Table
                           	Slicer : Based on department, Center and Start Date.
                             Button for Page Navigation and Clear all slicer
          
