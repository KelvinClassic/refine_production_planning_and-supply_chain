# refine_production_planning_and_supply_chain

### Problem Statement

- Inefficient Production
- Customer Disconnection
- Inventory Management

### Aim of Project

#### - Cutomer Segmentation:
    - To segment and profile Mas-More Ventures customer base to gain insights into their preferences, buying behaviours, and geographic distribution.
#### - Data_Driven Planning:
    - To enhance production planning, inventory management, and distribution strategies based on customer segments, thereby reducing overpoduction and minimize excess inventory.
#### - Customer-centric Approach
    - To improve on-time deliveries, increase customer satisfaction and align production with customer demands.

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
    - Correct date_type issue with Sales data, and extract date and time. Refer to [data_type_correction](/working_dir/date_type_correction.ipynb)
    - Confirm data types of all datasets (numbers/dates columns should align to the right, while text should be align to the left)

- Data Exploration on Customer Dataset
    - Customer Segregation
        - Distribute Customers based on age (Adult:18-40; Middle-aged:41-60; Senior:61-69)
        - Distribute customers based on income
        - Segregate customers based on the combination of the inital distributions 

- Merge datasets using Power Pivot
    - Customer 1 ---> * Sales
    - Inventory 1 ---> * Sales
    - Inventory 1 ---> * Production

- Understand Customers Preferences (use pivot table from the merged datasets)
    - Quantity of product sold, by Demographic Segmentation, by Product SKU
    - Quantity of product sold, by Geographic Location, by Product SKU
- Investigate Sales Trend by Month

#### - Project Questions:
    - #### Customer types by Location:
        - Show popular are our customers in each city? 
    - #### Customers types by quantity sold: 
        - How well are the customers buying from us? (Customer monthly sales by trend)
    - #### Sales Quantity of each customer type by month:
        - What is the monthly sales by each customer type? (customer monthly sales trend)
    - What are the best selling SKUs based on quantity sold?
    - What is the current inventory levels of each SKU:
        - visualize the top SKUs by each customer
    - What is out of stock and by how many days can it be replenished?
    - What is the current production capacity for each SKU in hours?