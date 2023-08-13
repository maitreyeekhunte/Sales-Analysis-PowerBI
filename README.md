# Sales-Analysis-PowerBI

### DAX Queries used - 
#### 1. Calendar = CALENDARAUTO()
#### 2. Month = FORMAT('Calendar'[Date],"mmm")
#### 3. Month Num = MONTH('Calendar'[Date])
#### 4. Quarter = FORMAT('Calendar'[Date],"\QQ")
#### 5. Year = FORMAT('Calendar'[Date],"yyyy")
#### 6. Revenue = SUM(Orders[Sales])
#### 7. Central Revenue = CALCULATE([Revenue],Geography[Region]="Central")
#### 8. Revenue vs Central = [Revenue]-[Central Revenue]
#### 9. PY Month Rev = CALCULATE([Revenue],PREVIOUSMONTH('Calendar'[Date]))
#### 10. Rev MOM Var = [Revenue]-[PY Month Rev]
#### 11. Rev Mom Var% = DIVIDE([Rev MOM Var],[PY Month Rev],0)
#### 12. Total Rev Year = CALCULATE([Revenue],REMOVEFILTERS('Calendar'[Month],'Calendar'[Month Num]))
#### 13. Monthly % Share = DIVIDE([Revenue],[Total Rev Year],0)
#### 14. REV SPLY = CALCULATE([Revenue],SAMEPERIODLASTYEAR('Calendar'[Date]))
#### 15. Revenue YTD = CALCULATE([Revenue],DATESYTD('Calendar'[Date])) 
