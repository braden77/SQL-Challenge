
# Research Project on Employees

## About The Project

### Background

* As a new data engineer at Pewlett Hackard, my first major task is a research project on employees of the corporation from the 1980s and 1990s.

* All the data is included in six CSV files. 

* Task 1: Data engineering. 
    * Design the tables to hold data in the CSVs, and import the CSVs into a SQL database

* Task 2: Data analysis. 
    * Answer questions about the data. 
### Dataset

* Six csv files in the folder of CSVs

    * Department name
    * Employees' department
    * Manager of each department
    * Employee personal information
    * Employee's salary
    * Title name

### Built With

* PostgreSQL
* Python
* Jupyter Notebook

## Procedures

### 1. Inspect the CSVs and sketch out an ERD of the tables.
<img src = "images/ERD.png" >

### 2. Creat a table schema for each of the six CSV files. Define data types,   primary keys, foreign keys, and other constraints.
* Use [QUICK DBD](http://www.quickdatabasediagrams.com) to sketch out ERD
* Primary keys should be unique, otherwise create a composite key to uniquely identify a row.
* All table schema can be found in "schema.sql" file.
* Use PostgreSQL as our database, creat 6 tables using the "schema.sql"
* Tables should be created in correct order to handle foreign keys.
* Import each CSV to corresponding SQL table, be sure to import the data in the same order that the tables were creawted and account for the headers when importing to avoid errors.
<img src = "images/tables.jpg" >

### 3. Data analysis.
* List the following details of each employee: employee number, last name, first name, sex, and salary.
<img src = "images/1.jpg" >

* List first name, last name, and hire date for employees who were hired in 1986.
<img src = "images/2.jpg" >

* List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.
<img src = "images/3.jpg" >

* List the department of each employee with the following information: employee number, last name, first name, and department name.
<img src = "images/4.jpg" >

* List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."
<img src = "images/5.jpg" >

* List all employees in the Sales department, including their employee number, last name, first name, and department name.
<img src = "images/6.jpg" >

* List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.
<img src = "images/7.jpg" >

* In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.
<img src = "images/8.jpg" >

### 4. Data visualization





## Findings 
### 1. Statistical summary (full table in Jupyter notebook)
   <img src = "images/ERD.png" >

### 2. Distribution of each attribute value 
   <img src = "images/distribution.png" >

### 3. Correlation coefficients matrix
  * 3 paris of strong correlation
  * "PURCHASES" and "ONEOFF_PURCHASES" -- 0.92
  * "PURCHASES_FREQUENCY" and 'PURCHASES_INSTALLMENT_FREQUENCY' --0.86
  * "CASH_ADVANCE_TRX" and "CASH_ADVANCE_FREQUENCY" --0.8
  <img src = "images/correlation.png" >

### 4. Divide customres into 8 clusters according to "Elblow Method"
  <img src = "images/elbow.png" >

### 5. Statistical summary for each cluster (full table in Jupyter notebook)
  <img src = "images/clusters.JPG" >

  * Credit card issuers usually have more interests in "Transactors" and "Revolvers"
  * Cluster 6 belongs to "Transactors": Those are customers who pay least amount of intrerest charges and careful with their money, Cluster with lowest balance ($104) and cash advance ($303), Percentage of full payment = 23%
  * Cluster 0 belongs to "Revolvers" who use credit card as a loan (most lucrative sector): high balance (more than $5000) and cash advance (more than$5000), low purchase frequency, high cash advance frequency (0.52), high cash advance transactions (16) and low percentage of full payment (3.8%)

### 6. Visualizations of balance distribution for each cluster (distribution for other attributes can be found in Jupyter notebook)

  <img src = "images/cluster_plot.png" >

### 7. Visualize the clusters in 2-axies plane
  <img src = "images/2_axes_plane.png" >

## Raw Data Explanation


## References
* [Market Segmentation from Wikipedia](https://en.wikipedia.org/wiki/Market_segmentation)










