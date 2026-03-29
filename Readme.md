# Sales Data Cleaning, Analysis & Dashboard


## Project Overview 
This project showcases end-to-end Excel data analytics by taking raw sales data and turning it into actionable insights. It covers the full workflow: bringing data in, cleaning it, analyzing it, passing it to a visualization tool, visualizing trends, and presenting findings. The final interactive dashboard highlights sales performance, key metrics, and business insights, demonstrating practical skills in data cleaning, analysis, and visualization.

---

## Project Objectives
- Organize and clean raw sales data to ensure accuracy and consistency.  
- Enhance the dataset with additional columns for better analysis.
- Analyze revenue trends using PivotTables
- Calculate dynamic KPIs using GETPIVOTDATA for real-time insights. 
- Build an interactive and dynamic dashboard to visualize insights and support business decisions.

---

## Tools Used
- Excel (formulas, PivotTables, GETPIVOTDATA)
- Charts, slicers, & interactive dashboard features

---

## Dataset Information
- **Source:** The data set used in this project was generated using AI for portfolio purpose. All data is synthetic and does not represent real individuals. The raw data set has 95 rows including header row and duplicates row.
- **Type:** Excel Data Analytics / Dashboard Project 

---

## Privacy Notice
- Due to privacy considerations, the complete Excel dataset is not publicly shared. Selected sample screenshots from raw dataset is provided to demonstrate the cleaning and analysis workflow

---

## Full Data Analytics Pipeline
---
### Step 1: Bringing Data
Imported raw dataset (comma-separated in a single column) into Excel for processing
The raw dataset contained several inconsistencies including:
- Data was in a single column
- Inconsistent date formats & incorrect data type
- Casing inconsistencies in product category
- Leading spaces and special character issues, missing email domains and null values in Customer_Email Column
- Revenue column stored in incorrect format

---

**Raw Data from row 1 to 25**
Screenshot:
![1_to_25_Raw](Data/Raw/screenshot/messy_raw_data.png)

---

### Step 2: Data Cleaning and Formatting
The following cleaning steps are performed to clean the above raw data set to ensure data accuracy and consistency.

#### Text to Columns 
Split data into columns using delimiter comma and the data type of Sales_Date converted to MDY format by TEXT TO COLUMNS

Screenshot:
![Text to Columns](Cleaning/screenshots/text_to_Column.png)

**Organized Raw Data**
Screenshot:
![Organized_Raw_Data](Cleaning/screenshots/organized_raw_data.png)

---

#### Adjusting Column Width for Better Readability
Adjusted column widths to ensure all data is clearly visible and properly aligned for improved readability.

Screenshot:
![Columns_width](Cleaning/screenshots/Column_widthh_issue.png)

---

#### Sales_Date Cleaning and Formatting 
Standardized date format by correcting wrong format DMY of some dates as the Sales_Date Column was already Converted to MDY format by TEXT TO COLUMNS

Screenshot:
![Date_Cleaning_1](Cleaning/screenshots/invalid_Date_1.png)

Screenshot:
![Date_Cleaning_2](Cleaning/screenshots/invalid_date_2.png)

---

#### Fixing Casing Issue in Product_Category
Fixed casing in Product_Category Column using PROPER()

Screenshot:
![Fixed_Casing](Cleaning/screenshots/proper.png)

---

#### Email Column Cleaning and Standardization
##### Handling Domain Errors
Cleaned the email column by correcting domain formatting issues using IF()

Screenshot:
![Handling_Domain_Errors](Cleaning/screenshots/missing.com.png)

---

##### Special Character Cleanup & Case Standardization
Cleaned special character issues and standardized lowercase formatting in the email column using LOWER() + SUBSTITUTE() to ensure consistency.

Screenshot:
![Handling_special_character_and_Case](Cleaning/screenshots/Lower+Substitute.png)

##### Removing Extra Spaces  
The Email column contained extra leading space in an email which is cleared using TRIM()

Screenshot:
![Removing-Extra-Spaces ](Cleaning/screenshots/trim.png)

---

##### null Value Handling
Replaced null values with “No Email Provided” using IF()

Screenshot:
![Replacing_null](Cleaning/screenshots/null_email.png)

---

#### Duplicate Removal
Removed a single duplicate row using Excel’s “Remove Duplicates” feature from the ribbon to ensure unique records in the dataset.

Screenshot:
![Duplicate_Removal](Cleaning/screenshots/duplicate.png)

---

**Clean Data from row 1 to 25**
Screenshot:
![clean_1_25](Data/Clean/screenshot/final_clean.png)

---

## Step 3. Preparing Data For Analysis
---
### Dataset Enhancement by adding Month-Year and Month-Start Columns
Enhanced the dataset by creating two additional columns: Month_Year and Month_Start to support time-based analysis and improve trend tracking.

**Month_Year_Column**
Screenshot:
![Month_year](Analysis/screenshot/additional_column_1.png)

**Month_Start_Column**
Screenshot:
![Month_Start](Analysis/screenshot/additional_col_2.png)

---

### Step 4: Bringing data into a visualization tool
---
#### Revenue by Category
Created a pivot table to summarize total revenue by product category, highlighting top-performing categories.

---

#### Monthly Revenue Trends
Built a pivot table to track revenue trends over time, helping identify patterns and seasonal variations.

---

### Step 5: Visualizing Data by Pivot Charts
---
#### Revenue by Category
Created from pivot table to summarize total revenue by product category, highlighting top-performing categories.

---

#### Monthly Revenue Trends
Built from pivot table to track revenue trends over time, helping identify patterns and seasonal variations.

---

Analysis Screenshot:
![Analysis](Analysis/screenshot/pivot.png)

---

#### Insights Generated
- **1. High Revenue Concentration Risk**
The Electronics category dominates nearly half of the total revenue, creating a heavy reliance on a single product line or service. This means any market shift affecting that specific category will impact the entire business's financial health.
- **2. Post-Peak Retention Collapse**
Revenue peaks in Month 2 but then drops steadily over the next four months. This means the business can attract customers at first, but struggles to keep them coming back regularly.

---

## Step 6: Dashboard Creation
An excel dashboard was created to summarize insights visually. The dashboard includes:
- KPIs
- Pivot Charts
- Slicers

---

### Key Performance Indicators (KPIs) 
---
#### Dynamic KPI – Total Revenue
A dynamic Total Revenue KPI was created using Excel’s GETPIVOTDATA function, allowing the value to update automatically based on Pivot Table filters and slicers. This ensures that whenever the user interacts with the dashboard (e.g., selects a category or month), the KPI reflects the exact filtered revenue in real-time—making the dashboard fully interactive and insight-driven.

---

### Slicers

Slicers are interactive filters that allow you to quickly filter by categories like Product Category and Month helping you focus on specific insights without altering the underlying data. the following slicers are used

- Month_Start

- Product_Category

---

Dashboard Screenshot:
![Dashboard](Dashboard/screenshot/dashboard.png)

---

