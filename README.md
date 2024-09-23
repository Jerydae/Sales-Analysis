# Sales Analysis


## Table Of Contents

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Data Cleaning/Preprocessing](#data-cleaningpreprocessing)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Conclusion](#conclusion)

[Recommendations](#recommendations)

[References](#references)


### Project Overview

The objective of this data analysis project is to analyze an e-commerce data over a period of 3years and present comprehensive insights into sales, 
profit, orders, profit margin, and various comparisons. This aims to provide a clear understanding of key performance indicators and trends using Power BI.

<img width="479" alt="project-2" src="https://github.com/Habiba-Hussein/SalesAnalysis/assets/147278092/e75712d5-29f7-49ce-ad45-bed547343f51">


### Data Sources

Sales Data: The primary dataset used for this analysis is the "sales_analysis.xlsx" file ,which contains well-detailed information about the business and additionally has
4 datasets within it i.e sales orders,regions, products and customers

### Tools Used

- Power BI [Download Here](https://powerbi.microsoft.com/en-us/downloads/)

### Data Cleaning/Preprocessing

Perfomed this in the initial step,Utilized Power Query Editor in Power BI:
1. Data loading and Inspection: Ensuring the columns are of the correct data type
2. Removing duplicates and handling missing values 
3. Merging the datasets and creating calculated columns
4. Create Data Model

### Exploratory Data Analysis

  - What is the Total Sales?
  - Compute the Profit and Analyze the Orders
  - Calculate Profit Margin
  - Compare Sales by Product,month with Previous Year
  - Display the Top 5 Cities?
  - Compare Profit by Channel with Previous Year
  - Analyze Sales by Customer and Compare with Previous Year
  - Create Slicers for Date, City, Product, and Channel

### Data Analysis

Here are some of the DAX computations used:

To compute the total Sales:

``` Sales = SUM(Sales_Data[Sales]) ```

Previous Year Total Sales:

```Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))```

Difference Between Current & Previous Year Sales

```Sales vs PY = [Sales] - [Sales PY]```

Percentage Increase or Decrease in sales year on year (YOY%)

```Sales vs py % = DIVIDE([Sales vs PY],[Sales],0)```

Total Products Sold 

```SUM(Sales_Data[Order Quantity])```

Profit 

```SUM(Sales_Data[Profit])``` 

Profit LY(Last Year) 

```CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))```

Profit vs LY %(Percentage)
 
```[Profit Vs LY]/[Profit]```

 Profit Margin

``` DIVIDE([Profit],[Sales],0)```


### Conclusion

- The company sales in 2019 tends to be the lowest with 48.5M
- There is a drop in sales for all the top 7 Products
- All the cities have a negative profit margin with Waitakere city having the largest loss margin 
- The profit margin in the Export channel is the highest and Distributor channel leading with the highest loss

### Recommendations

Based on the analysis,we recommend the following:
- The company should focus on expanding  the distributor channel strategically
- The company should invest in proper marketing of their products
- Restrategize the company ways

### References

1. DataWolfs




  
  
