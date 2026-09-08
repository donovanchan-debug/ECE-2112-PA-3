# ECE-2112-PA-3

Name: Donovan C. Chan  
Section: 2ECE-A  

# A. POSITIONAL AND LABEL-BASED SLICING
After loading cars, complete the following operations.  
a. Display the shape and complete list of column names of cars.  
b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1.  
c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.  
Requirement: The row selection in part (b) must use iloc; the column selection in part (c) must
use column labels.  

**How it works:**
1. Display the cars spreadsheet:   
`cars = pd.read_csv('cars.csv')`      
`cars`   

2. Display the shape and complete list of column names of cars:   
`print("Shape of cars:", cars.shape)`   
`print("Column names:", cars.columns.tolist())`   

3. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1.   

`cars_6_to_10 = cars.iloc[5:10]`   
`cars_6_to_10`   

4. from cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order:   
`selected_columns = cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]`   
`selected_columns`   
   
# B. Model Lookup
Use Boolean indexing on the Model column to answer both requests:   
a. Display the complete row for Toyota Corolla.   
b. For Pontiac Firebird, display only Model, mpg, hp, and wt.   
Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.   

**How it works:**   
1. Display the cars spreadsheet:   
`cars = pd.read_csv('cars.csv')`      
`cars`   

2. Display the complete row for Toyota Corolla:   
`toyota = cars[cars['Model'] == 'Toyota Corolla']`  
`toyota`   

3. For Pontiac Firebird, display only Model, mpg, hp, and wt:   
`pontiac = cars[cars["Model"] == "Pontiac Firebird"][["Model", "mpg", "hp", "wt"]]`   
`pontiac`   
