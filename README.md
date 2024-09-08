# Power BI Project: AdventureWorks Cycles

### Role: **Business Intelligence Analyst**

In this project, I play the role of a Business Intelligence Analyst for AdventureWorks Cycles, a fictional manufacturing company. My role is to transform raw data into professional-quality reports and dashboards to track KPIs, compare regional performance, analyze product-level trends, and identify high-value customers. The project was completed in four distinct stages, as outlined below:

---

## Project Overview

- **Project Name**: AdventureWorks Cycles BI Analysis
- **Project Type**: Power BI Desktop Project
- **Tools Used**: Power BI Desktop, DAX, Power Query
- **Industry**: Manufacturing


---

## Stages of the Project

### **Stage 1: Connecting & Shaping Data**

In this stage, I focused on building automated workflows to extract, clean, transform, and load our project data using Power Query. Key tasks included:

- **Data connectors**: Connecting data from multiple sources.
- **Storage & import modes**: Used Import mode for connecting to the data.
- **Query editing tools**: Utilizing Power Query for data shaping.
- **QA & profiling tools**: Ensuring data quality through profiling.
- **Text, numerical, date & time tools**: Manipulated text and numbers.
- **Rolling calendars**: Created dynamic calendar table for date time calculations.
- **Index & conditional columns**: Adding calculated columns for logic.
- **Grouping & aggregating**: Summarizing data.
- **Appending queries**: Combining data from multiple table by connecting to a folder.
- **Data source parameters**: Building dynamic connections.
- **Importing Excel models**: Integrating data from Excel.

---

### **Stage 2: Creating a Relational Data Model**

This stage involved designing the AdventureWorks data model using best practices, including:

- **Database normalization**: Organizing data for efficiency.
- **Fact & dimension tables**: Defining key data structures.
- **Primary & foreign keys**: Creating relationships between tables.
- **Star & snowflake schemas**: Designing a star schema model.
- **Active & inactive relationships**: Managing table relationships.
- **Relationship cardinality**: Defining one-to-one, one-to-many relationships.
- **Filter context & flow**: Controlling the flow of data filtering.
- **Bi-directional filters**: Using bidirectional relationships.
- **Hierarchies**: Building hierarchies for drilldown analysis.

---

### **Stage 3: Adding Calculated Fields with DAX**

This stage involved working with DAX (Data Analysis Expressions) to create calculated columns and measures:

- **Calculated columns & measures**: Defining business metrics.
- **Implicit, explicit & quick measures**: Understanding different measures.
- **DAX syntax & operators**: Writing DAX for data calculations.
- **Math & stats functions**: Performing calculations like `SUM`, `AVERAGE`.
- **Conditional & logical functions**: Using `IF`, `SWITCH`, and logical functions.
- **The SWITCH function**: Simplifying complex calculations.
- **Date & time functions**: Performing time-based analysis.
- **The RELATED function**: Accessing data across relationships.
- **CALCULATE, FILTER & ALL**: Controlling filter context.
- **Iterator (X) functions**: Using iterators for row-level calculations.
- **Time intelligence patterns**: Applying time-based DAX functions.

---

### **Stage 4: Visualizing Data with Reports**

In this stage, I transformed the processed data into interactive and insightful reports:

- **Dashboard design framework**: Designing effective reports and dashboards.
- **Cards & KPIs**: Displaying key metrics.
- **Line charts, trend lines & forecasts**: Visualizing trends.
- **Table & matrix visuals**: Displaying tabular data.
- **Conditional formatting**: Applying rules to highlight data.
- **Top N filtering**: Identifying top-performing data.
- **Map visuals**: Creating geographical analysis.
- **Drill up, drill down & drillthrough**: Enabling data exploration.
- **Report slicers & interactions**: Adding filters and slicers for interactivity.
- **Bookmarks & page navigation**: Enhancing report navigation.
- **Numeric & field parameters**: Allowing user customization.
- **Custom tooltips**: Adding dynamic tooltips to visuals.
- **Importing custom visuals**: Enhancing report capabilities with custom visuals.

---

## Instructions for Viewing the Project

1. **Download the Repository**: Download the entire repository as a ZIP file and extract it to a folder on your local machine.
2. **Ensure Folder Structure**: Make sure the extracted folder contains the `.pbix` Power BI project file and the necessary CSV files used as data sources.
3. **Open in Power BI Desktop**: Open the `.pbix` file using Power BI Desktop. Power BI will attempt to load the CSV files from the same folder.
4. **Fixing Data Source Path Issues**: If Power BI cannot find the data files and throws a path error, you will need to manually update the data source paths:
    - Go to **Transform Data** > **Data Source Settings**.
    - Select the data source, click **Change Source**, and browse to the new folder where the CSV files are stored.

    Here’s the Power Query M code to edit the source paths if needed:

    ```m
    let
        Source = Folder.Files("C:\Path\To\Your\Data\Folder"),
        FilteredFiles = Table.SelectRows(Source, each Text.EndsWith([Name], ".csv"))
    in
        FilteredFiles
    ```

5. **Refresh the Data**: After updating the data source, refresh the data to ensure everything is loaded correctly.


---

### Notes

- The project uses relative paths, so ensure that all the files are in the same folder when downloading and opening in Power BI.
- If the paths do not work due to changes, refer to the instructions above for updating the file paths.


---
