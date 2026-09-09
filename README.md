# 🚚 Freight Analysis Dashboard

## 📌 Project Overview

The **Freight Analysis Dashboard** is an interactive Power BI MIS reporting solution developed to analyze Sales and Freight performance across Financial Year (FY) Months, Entities, Units, and Weeks.

The dashboard is designed according to the provided **Freight Analysis framework** and is divided into two major phases:

**Phase 1 – FY MONTHLY FREIGHT ANALYSIS**
**Phase 2 – WEEKLY FREIGHT ANALYSIS**

The dashboard provides Actual and Budget analysis through interactive slicers, matrix reports, and graphical visualizations.

The Financial Year starts from **April** and the dashboard follows the required FY Month structure such as **Apr 22, Apr 23, Apr 24**, etc.
Example:

![Landing Page](https://github.com/ChintuCodes-dot/FREIGHT-ANALYSIS-DASHBOARD/blob/main/Freight%20Analysis_landing%20page.png)
![FY Month Freight Analysis phase1](https://github.com/ChintuCodes-dot/FREIGHT-ANALYSIS-DASHBOARD/blob/main/Phase%201-%20FY%20Monthly%20Freight%20Analysis%20pg1.png)
![FY Month Freight Analysis phase1](https://github.com/ChintuCodes-dot/FREIGHT-ANALYSIS-DASHBOARD/blob/main/Phase%201-%20FY%20Monthly%20Freight%20Analysis%20pg%202.png)
![Weekly Freight Analysis phase2](https://github.com/ChintuCodes-dot/FREIGHT-ANALYSIS-DASHBOARD/blob/main/Phase%202%20-%20Weekly%20Freight%20Analysis%20pg3.png)
![Weekly Freight Analysis phase2](https://github.com/ChintuCodes-dot/FREIGHT-ANALYSIS-DASHBOARD/blob/main/Phase%202%20-Weekly%20Freight%20Analysis%20pg4.png)




# 🎯 Project Objectives

The main objectives of the Freight Analysis Dashboard are:

- Analyze Sales performance across Financial Year Months.
- Analyze Freight performance across Financial Year Months.
- Calculate and monitor Freight % against Sales.
- Compare Actual performance with Budget performance.
- Analyze performance by Entity.
- Analyze weekly Freight/Sales performance by Unit.
- Provide an interactive MIS reporting solution.
- Present both tabular and graphical views for management analysis.

# 📂 Dataset

The dashboard is built using three fact tables:

## 1. Fact-MasterNew

The **Fact-MasterNew** table contains the Actual transaction-level data used for Actual Sales and Freight analysis.

Important fields include:

- Year
- Entity
- Unit
- Invoice
- Date
- Financial Year
- Week
- Month
- Quarter
- Destination
- Region
- Mode
- Customer Name
- Product
- Incoterm
- Value in INR
- Revenue Recognised
- GIT
- Net Weight
- Gross Weight
- Forwarder Name
- C&F Charges
- Freight Value
- Total Amount (C&F + Freight)

The table is used to calculate Actual Sales, Actual Freight, and Freight %.

## 2. Fact-BudgetSales

The **Fact-BudgetSales** table contains budget sales information.

Fields include:

- Entity
- Date
- Budget Sales
- Year

This table is used for Budget Sales analysis.

## 3. Fact-FreightBudget

The **Fact-FreightBudget** table contains budget freight information.

Fields include:

- Entity
- Date
- Freight
- Year

This table is used for Budget Freight analysis.

# 🏗️ Data Model

The Power BI data model uses fact and dimension tables to provide consistent filtering and analysis.

### Dimension Tables

- DimDate
- Entity

### Fact Tables

- Fact-MasterNew
- Fact-BudgetSales
- Fact-FreightBudget

The **DimDate** table provides the date, Financial Year, FY Month, Month Number, and Week Number structure required for the dashboard.

The **Entity** dimension is used to filter the Actual and Budget data by Entity.

# 📅 Date & Financial Year Structure

The dashboard uses a Financial Year that starts from **April**.

The date structure includes:

- Date
- Year
- Month
- Month Number
- FY Month
- FY Month Number
- FY Year
- Week Number
- Week Label

FY Month is displayed in a format such as:

- Apr 22
- May 22
- Jun 22
- ...
- Apr 23
- Apr 24

The dashboard uses the Financial Year Month structure for monthly analysis and the Week Number structure for weekly analysis.

# 📊 Key Metrics

The dashboard includes the following key metrics:

### Actual

- Sales
- Freight
- Freight %

### Budget

- Budget Sales
- Budget Freight
- Budget Freight %

### Metric Definitions

**Sales**  
Total Actual Sales based on the Value in INR, presented in Crores.

**Freight**  
Total Actual Freight based on Total Amount (C&F + Freight), presented in Crores.

**Freight %**  
Freight as a percentage of Sales.

**Budget Sales**  
Budget Sales amount presented in Crores.

**Budget Freight**  
Budget Freight amount presented in Crores.

**Budget Freight %**  
Budget Freight as a percentage of Budget Sales.

# 📊 PHASE 1 – FY MONTHLY FREIGHT ANALYSIS

The first phase focuses on **Financial Year Month-wise Freight Analysis**.

The purpose of this phase is to analyze Actual and Budget Sales and Freight performance across Entities and FY Months.

## 🎛️ Filters / Slicers

The dashboard includes:

 **FY Month Slicer**
 **Entity Slicer**

The FY Month slicer provides Financial Year Month selections such as:

- Apr 22
- Apr 23
- Apr 24
- etc.

The Entity slicer allows users to analyze individual Entities or view the overall data.

## 📋 Actuals Matrix

The Actuals matrix is structured according to the framework.

### Rows

- Entity

### Columns

- FY Month

### Values

- Sales
- Freight
- Freight %

This allows users to analyze Actual Sales, Actual Freight, and Freight % for each Entity across Financial Year Months.

## 📋 Budget Matrix

The Budget matrix follows the same monthly reporting structure.

### Rows

- Entity

### Columns

- FY Month

### Values

- Sales
- Freight
- Freight %

The Budget view allows comparison of planned performance across Entities and Financial Year Months.

## 📈 Actuals Graph

The Actuals graphical analysis presents the monthly trend of:

- Sales
- Freight

### Chart Structure

**Dimension:**
- FY Month

**Facts:**
- Sales
- Freight

This provides a visual representation of Actual Sales and Freight performance over the Financial Year.

## 📈 Budget Graph

The Budget graphical analysis presents the monthly trend of:

- Budget Sales
- Budget Freight

### Chart Structure

**Dimension:**
- FY Month

**Facts:**
- Budget Sales
- Budget Freight

This provides a visual representation of Budget performance across Financial Year Months.

# 📊 PHASE 2 – WEEKLY FREIGHT ANALYSIS

The second phase focuses on **Weekly Freight Analysis**.

This phase provides a more detailed view of performance by Week Number and Unit.

The framework specifies weekly analysis using Unit and Week Number, with Sales as the primary value for the weekly analysis.


## 🎛️ Filters / Slicers

The Phase 2 dashboard includes:

 **FY Month Slicer**
 **Entity Slicer**

The FY Month slicer allows the user to select a particular Financial Year Month, while the Entity slicer allows analysis for a specific Entity or all Entities.

# 📋 Actuals Weekly Matrix

The Actuals matrix provides weekly Unit-level analysis.

### Rows

- Week Number

### Columns

- Unit

### Values

- Sales

The matrix allows users to analyze Sales performance for each Unit across the weeks of the selected FY Month.

The Week Number restarts for each month, allowing the selected month to display:

- WK1
- WK2
- WK3
- WK4
- WK5

depending on the available weeks in that month.

# 📋 Budget Weekly Matrix

The Budget section follows the weekly reporting structure defined in the framework.

### Rows

- Week Number

### Columns

- Unit

### Values

- Sales

This provides the required weekly Budget reporting structure for Unit-level analysis.

# 📊 Weekly Actuals Graph

A **Stacked Column Chart** is used for the weekly graphical analysis.

### Chart Configuration

**X-axis:**
- Unit

**Y-axis:**
- Sales

**Legend:**
- Week Number

Each column represents a Unit, while the individual sections represent the different Week Numbers.

This allows users to compare weekly Sales performance across Units.

# 📊 Weekly Budget Graph

A corresponding graphical view is provided for Budget analysis.

### Chart Configuration

**X-axis:**
- Unit

**Y-axis:**
- Sales

**Legend:**
- Week Number

This provides a visual comparison of weekly Budget Sales performance across Units.


# 🔄 Dashboard Workflow

The overall reporting workflow is:

Raw Data
↓
Data Model
↓
Date & Entity Dimensions
↓
Actual & Budget Fact Tables
↓
Calculated Metrics
↓
FY MONTHLY FREIGHT ANALYSIS
↓
WEEKLY FREIGHT ANALYSIS
↓
Interactive FREIGHT ANALYSIS Dashboard


# 🔍 Dashboard Analysis Capabilities

The completed dashboard provides:

- Financial Year Month analysis
- Entity-wise analysis
- Actual Sales analysis
- Actual Freight analysis
- Actual Freight % analysis
- Budget Sales analysis
- Budget Freight analysis
- Budget Freight % analysis
- Monthly Actual vs Budget analysis
- Weekly Unit-level analysis
- Week-wise Sales analysis
- Matrix-based reporting
- Graphical reporting
- Interactive filtering through FY Month and Entity slicers

# 🛠️ Tools & Technologies

- **Microsoft Power BI**
- **DAX**
- **Power Query**
- **Microsoft Excel**
- Data Modeling
- Data Analysis
- Data Visualization
- MIS Reporting


# 📁 Project Structure

text
Freight-Analysis/
│
├── Dataset/
│   └── freight_data.xlsx
│
├── Dashboard/
│   └── Freight Analysis.pbix
│
├── Framework/
│   └── Freight Analysis Framework.pdf
│
└── README.md
