# Call Center Data Analysis Dashboard
![](call.png)
--

## Introduction
it's a call center dashboard where managers want to know the performance of their team based on KPIs etc ...
The data is from an Excel document, which provides a foundation in analyzing data using Power Pivot,interactive Pivot Charts with slicers,conditional formatting. The data contains detailed information on Call number,Customer ID,Purchase Amount,Satisfaction Rating,Duration Bucket,City etc...

## Dashboard File
My final [dashboard](https://github.com/Othmane-data/Call-Center-Data-Analysis-Report-by-Excel/blob/main/Call-Center-data-excel-portfolio-project.xlsx)

## Problem statement
1. What is the total of calls for each day and month?
2. What is the total of calls and the total amount for each Representative?
3. What is the count of calls by Gender and by City?
4. What is the total amount by Customer ID,by City and by each Representative?

## Skills/ concepts demonstrated
- 🧮 Formulas and Functions
- 📉 Charts and Visualization
- ❎ Conclusion and Recommendations


### 🧮 Formulas and Functions:
- Customer Name,Email,Country;
```
- Customer Name=XLOOKUP
  (C2,customers!$A$1:$A$1001,
    customers!$B$1:$B$1001,,0)
  
- Email=IF
  (XLOOKUP(C2,customers!$A$1:$A$1001,
    customers!$C$1:$C$1001,,0)=0,"",
      XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0))

- Country=XLOOKUP
  (C2,customers!$A$1:$A$1001,
    customers!$G$1:$G$1001,,0)
```
  
- Coffee Type,Roast Type,Unit Price;
```
- Coffee Type=INDEX
(products!$A$1:$G$49,
  MATCH(orders!$D2,products!$A$1:$A$49,0),
    MATCH(products!$B$1,products!$A$1:$G$1,0))

-Roast Type=INDEX
(products!$A$1:$G$49,
  MATCH(orders!$D2,products!$A$1:$A$49,0),
    MATCH(products!$C$1,products!$A$1:$G$1,0))

-Unit Price==INDEX
(products!$A$1:$G$49,
  MATCH(orders!$D2,products!$A$1:$A$49,0),
    MATCH(products!$E$1,products!$A$1:$G$1,0))
```

### 📉 Charts and Visualization:
The report comprises 3 charts:

___1. Top Sales Of Coffee;___

___2. Top Sales By Country;___

___3. Top Sales By Customers Name.___

we're use the pivot table for every shart

__- Features:__
- Order Date by Mounth Timeline;
- Size Slicer;
- Roast Type Name Slicer;
- Loyalty Card Slicer.
