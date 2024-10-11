# Madhav-E-Commerce-Store-Performance-Analysis-Using-Power-BI

### What new have I implemented
✨ Bubble resizing on Map visual based on a feature |
✨ Button for clearing all slicers applied |
✨ Data Modelling on model view section |
✨ Decomposition Tree Visual |
✨ New Card visual for clubbing up multiple KPIs |
✨ Vertical Dropdown style slicer |
---

### Dashboard PDF : [powerBIDashBoard3 (1).pdf](https://github.com/user-attachments/files/17347258/powerBIDashBoard3.1.pdf)

## Problem Statement

This dashboard helps the e-commerce store understand its store better. It helps the store know their customers' preferences and shopping interests. 
The dashboard helps access their improvement area. The dashboard consists of a profit decomposition tree visual which explains the profit share based on category and sub-category of products sold. 
Negative sales profit indicates improvement areas to minimize the effects of negative profit.

### Steps followed 

- Step 1: Load datasets into Power BI Desktop, dataset are CSV files.
  - Two datasets were used "Orders" and "Details". One common column in these datasets is "order ID."
    - Columns in Orders dataset:
      - City
      - Customer Name
      - Order Date
      - Order ID
      - State
    - Columns in Details dataset:
      - Amount (Unit price)
      - Category
      - Order ID
      - Payment Mode
      - Profit
      - Quantity
      - Sub-category
- Step 2: This lands on the report view section. Under the Home tab click on Transform Data to make any necessary changes to the dataset. This will open the Power Query Editor window where transformations may be made.
  - Duplicate rows in the datasets were removed. Select the complete table by Ctrl + A, under the home tab, hover on the remove rows icon, and click remove duplicates. This will delete all redundant information if any.
  - Add necessary columns. Columns "Revenue" and "Cost" were added to the Details dataset.
    -  DAX query used for Revenue column

           Revenue = [Amount] * [Quantity]

    -  DAX query used for Cost column

           Cost = [Revenue] - [Profit]
  - Format Data types into appropriate types for analysis. All column data types were appropriately detected by Power BI.
  - Under home click close & apply icon. this will make all the changes committed permanently and further work is now performed on these transformed datasets.
- Step 3: Since we have multiple datasets model view helps Power BI make relations between these datasets. By default power BI detects these relationships.
  - On the model view section a one-to-many relationship is created between Orders and Details datasets.
  - Modelling integrates datasets and visuals for columns of different datasets can be produced. 

    Snap of Data Modelling View,

    ![Screenshot 2024-10-11 233435](https://github.com/user-attachments/assets/8860bfa4-41d5-4f8c-a460-5cd9be49afee)

- Step 4: On the report view section select appropriate visuals that answer questions on the performance of the store.
  - KPIs Key Performance Indicators added to the dashboard answers,
    - Total profit of the store.
    - total states that order from the store.
    - total cities that order from the store.
   
      A new version of card visual that clubs multiple cards was used to achieve it.

      Snap of KPIs,

      ![Screenshot 2024-10-11 235152](https://github.com/user-attachments/assets/9147b548-e48f-452b-a155-9b162fe82902)

  - A Real-time map visual represents,
    - 5 states that make up the highest share of the total profit the store makes.
      - The orange bubbles mark the geographical location of the states and the size of the bubbles varies on the profit by each state.
      - The + and - buttons are interactive zoom-in and out buttons.

      Snap of Map visual,

      ![Screenshot 2024-10-11 235724](https://github.com/user-attachments/assets/e2b96b6a-6c22-4238-8a9c-183dabc45e24)

  - A Profit Decomposition Tree on the dashboard indicates,
    - The distribution of the total profit the store makes based on the category and sub-category of products sold.
    - The bright green color represents profit and red represents loss.

      Snap of Decomposition tree visual, 

      ![Screenshot 2024-10-12 010823](https://github.com/user-attachments/assets/9b6b3c6b-b63b-4347-957f-e3ebcd0d8d96)
      
  - A Visual Filter(Slicer) added consists,
    - List of months.
      - The slicer style was set to dropdown style.
      - The "Select all" option was also added to the list.
      - Multiple selections from the list were allowed.

      Snap of Slicer visual,

      ![Screenshot 2024-10-12 010659](https://github.com/user-attachments/assets/4209ecac-5992-43c6-b9de-e78def23f9a6)

  - A Button on the top-right corner of the dashboard was added,
    - To clear all the slicers that may be applied on the dashboard.
      - To commit its action Ctrl + click is required.

        Under the Insert tab, click the icon that reads add a button to your report on hover to achieve it.

      Snap of the button,

      ![Screenshot 2024-10-12 003232](https://github.com/user-attachments/assets/bbe67450-8c13-4534-8319-b63eb9378e32)

- Step 5: A Line chart on the dashboard was added to represent trends in profit by month.
- Step 6: A Doughnut chart on the dashboard was added to represent customers' payment preferences.
- Step 7: A Bar chart on the dashboard was added to represent customers based on their expenditures (descending). This was narrowed down to the top 5.
- Step 8: In the report view, under the insert tab, ONE text boxes were added to the canvas, the title represented the store name and the purpose of the dashboard.
- Step 9: The report was then published to Power BI Service.
 
  ![Screenshot 2024-10-11 220859](https://github.com/user-attachments/assets/5406f71c-2f1c-44c4-ab11-b547049a1e7d)

# Snapshot of Dashboard (Power BI Service)

 ![Screenshot 2024-10-12 020452](https://github.com/user-attachments/assets/8ad36fa6-0f61-4906-aa41-f3f7c2b22641)

# Report Snapshot (Power BI DESKTOP)

 ![Screenshot 2024-10-12 020308](https://github.com/user-attachments/assets/e6ce872b-82d2-4acf-be30-b82677b34d23)

# Insights

A single-page report was created on Power BI Desktop & it was then published to Power BI Service.

The following inferences can be drawn from the dashboard;

### [1] Total Profit

    Total Profit of the store = 37.0 K Dollars.

This value will change if different visual filters are applied.  

### [2] Total number of states

    Total number of states that purchased from the store = 19

This value will change if different visual filters are applied.  
  
### [3] Total number of cities

    Total number of cities that purchased from the store = 25

This value will change if different visual filters are applied.  
  
### [4] Category and sub-category profit share

    Rank 1: Clothing

      Rank 1.1: Saree

    Rank 2: Electronics

      Rank 2.1: Printers

    Rank 3: Furniture

      Rank 3.1: Bookcases
 
### [5] Top 5 states

Rank 1: Tamil Nadu

Rank 2: Maharashtra

Rank 3: Gujrat

Rank 4: Kerala

Rank 5: Bihar 

    Thus, Tamil Nadu generates the highest profit for the store.
    
This insight may change if different visual filters are applied. 
         
### [6] Top 5 customers

Rank 1: Arushi

Rank 2: Bharat

Rank 3: Priyanka

Rank 4: Vrinda

Rank 5: Yogesh

       Thus, Arusuhi has made the highest expenditures in the store.
       
Thus, Tamil Nadu generates the highest profit for the store.

### [7] Customer payment preferences

Rank 1: COD (Cash On Delivery) (42.92%)

Rank 2: UPI (21.92%)

Rank 3: Debit card (15.07%)

Rank 4: Credit card (10.96%)

Rank 5: EMI (9.13%)

    Thus, it is significantly likely that the customer opts for the COD mode of payment for purchases.
