<img width="1920" height="890" alt="Dashboard_GIF" src="https://github.com/user-attachments/assets/0207a999-7a84-4913-9025-e5704bc9f125" />

# Introduction

This GDP analysis dashboard provides insights on various parameters of the GDP between any two countries. The main questions answered in building this dashboard are:

1. How does the GDP progression of Bangladesh compare with that of countries independent after 1971?
    - How does the recent average GDP of the two countries compare?
2. How did the GDP of the USA compare to that of the countries which suffered US-influenced wars?
    - What is the ratio of that particular country’s GDP compared to US GDP?

You can find my interactive dashboard here: https://github.com/HasinatRifa/Data_Analysis_Projects/blob/main/Excel_GDP_Analysis/GDP_1975_2025_uploaded.csv.xlsx

## Excel Skills Used

The following skills were used in analysing this dataset:

- Charts
- Data validation
- Filter
- Formulas and functions

# Building The Dashboard

## Bangladesh vs Other Countries Independent After 1971

<img width="826" height="494" alt="Chart1_GIF" src="https://github.com/user-attachments/assets/d16c37a1-bc39-4283-8815-87c3e9c56a7a" />

- I used the FIND and LEN functions to identify the character separating country names from dates of independence, and the character number from which the country name starts respectively. Afterwards, MID was used to isolate the country name.

```

=FIND(":",A2)+LEN(": ")

=MID(A2,B2,LEN(A2))

```

<img width="287" height="782" alt="Table1_img" src="https://github.com/user-attachments/assets/514a0d3b-05c0-45d7-bab2-3350bc45a4f9" />

- Used Advanced FILTER option from the Data tab to filter out the desired countries’ gdp data from the original sheet.
- Used Data Validation to create a drop-down list of the country names.
- Used SUMIF to create a dynamic row that changes according to the country chosen in the drop-down menu. Created a separate row for Bangladesh to keep it as constant. Finally, I created a line graph using both the rows, that shows the GDP progression of the chosen country and that of Bangladesh on the same graph for comparison.

`=SUMIF('Data for 1st chart'!$A$2:$A$52, GDP_Dashboard!$F$7, 'Data for 1st chart'!B2:AZ2)`

- To compare the average GDP of the chosen country with that of Bangladesh, I created a matrix card using the AVERAGE formula.

<img width="617" height="214" alt="MatrixCard1_img" src="https://github.com/user-attachments/assets/6be64454-ebcf-4a27-b211-4209f5ec30cb" />
