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
- 🧮 KPIs,Power Pivot,DAX,Formulas and Functions
- 📉 Interactive Pivot Charts with slicers and Visualization
- ❎ Conclusion and Recommendations


### 🧮 DAX,KPIs,Power Pivot,Formulas and Functions:

- DAX;
```
- Call count=COUNTROWS(calls)

- Total amount=SUM(calls[Purchase Amount])

- Total duration=SUM([Duration])

- Avr. rating=AVERAGE(calls[Satisfaction Rating])

- 5* calls=CALCULATE([call count],calls[Rating rounded]=5)
  
```
  
- Formulas and Functions;
```
- Sales and Amount selection by representative =IF
                                                 (F49=J$45,G49,NA())

-the total amount by Customer ID,by City and by each Representative=IF
                                             (pivots!D82:J99="","",pivots!D82:J99)

-Unit Price==INDEX
(products!$A$1:$G$49,=
  MATCH(orders!$D2,products!$A$1:$A$49,0),
    MATCH(products!$E$1,products!$A$1:$G$1,0))
```

### 📉 Interactive Pivot Charts with slicers and Visualization:
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
