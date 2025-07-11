# refine_production_planning_and_supply_chain

### Problem Statement
- Inefficient Production
- Customer Disconnection
- Inventory Management

### Aim of Project
- Cutomer Segmentation
- Data_Driven Planning
- Customer-centric Approach

### Data Description
- Customer Data
    - 
- Sales Data
    -
- Inventory Data
    -
- Production Data
    -

### Project Scope
- Exploratory Data Analysis
- Daat Analysis
- Visualisation and report
- Recommendation 

### Tech Stack
- Microsft Excel

### Procedures
- Data Cleaning and Processing
    - Import data to Excel Worksheets 
        - Data -> Get External Data -> From Other Sources -> From XML Data Import
    - Check missing values for each of the datasets.
        - Home -> Editing [Find & Select] -> Go To Special -> Blanks -> OK
    - Check duplicates (for all datasets)
        - Data -> Data Tools [Remove Duplicates]
    - Correct date_type issue with Sales data. Refer to [data_type_correction](/working_dir/date_type_correction.ipynb)
    - Extract date (new column: Text_Date) from Sales_data_new
        - =TEXT(E2, "DD/MM/YYY")
    - Convert extracted date to actual date (new column: Actual_Date)
        - =DATEVALUE(F2), then highlight and convert 'Actual_Date' column to Short Date (Home -> Number -> Short Date)
    - Confirm data types of all datasets (numbers/dates columns should align to the right, while text should be align to the left)
- Data Exploration on Customer Dataset
    - Customer Segregation
        - Distribute Customers based on age (Adult:18-40; Middle-aged:41-60; Senior:61-69)
        - Distribute customers based on income
        - Segregate customers based on the combination of the inital distributions 
- Merge datasets using Power Pivot
    - Customer 1 ---> * Sales
    - Inventory ---> * Sales
    - Inventory ---> * Production
- Understand Customers Preferences (use pivot table from the merged datasets)
    - Quantity of product sold, by Demographic Segmentation, by Product SKU
    - Quantity of product sold, by Geographic Location, by Product SKU
- Investigate Sales Trend by Month