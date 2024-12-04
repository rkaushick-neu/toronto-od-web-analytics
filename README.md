# Web Analytics for City of Toronto's Open Data Portal (2023 - 2024)
Analysis by: Jinesh Dutt, Rishabh Kaushick
<br>Supervised by: Dr. Omar Badreldin

## Aim
1. To analyze and visualize the existing data.
2. To identify external data sources to enhance existing visualizations.
3. To perform predictions on how the data may change over time.


## Visualizations
### Correlation Heat Map between Columns like User, Sessions, Views
Performed on Dataset: Referrer Domains  


## Documentation
### Data Description
**od-ips-clicks-durations-2023.csv**
| Sr. No | Column Name                     | Data Type |
|--------|---------------------------------|-----------|
| 1      | Client IP                       | String    |
| 2      | Date                            | Date      |
| 3      | Views                           | Integer   |
| 4      | Avg Session Duration (Sec)      | Float     |
| 5      | OD - File Download Clicks       | Integer   |
| 6      | Sessions                        | Integer   |

**od-referrer-domains-2023.csv**
| Sr. No | Column Name      | Data Type |
|--------|------------------|-----------|
| 1      | Referring Domain | String   |
| 2      | Date             | Date      |
| 3      | Session          | Integer   |
| 4      | Users            | Integer   |
| 5      | Views            | Integer   |


### Data Cleaning
1. For each dataset - segregated summary rows & non summary rows into two different sheets.
2. Extracted the date:
   1. month, day and year: for easy future analysis with respect to date
   2. day of the week: for example Mon, Tue, Wed
   ![Date column extracted to month, day and year](./screenshots/data_cleaning_date_columns.png)
3. In the user-ship metrics: Extracted details from 'Link Source Page URL' to understand the base url, which web page is visited, and if it a dataset - which dataset:
![Link Source Page URL data extraction](./screenshots/data_cleaning_usership_url_cleanup.png)
For example:
    | Link Source Page URL| Base URL | Category | Category Details 1 | Category Details 2 |
    |---------------------|----------|----------|--------------------|--------------------|
    | open.toronto.ca/dataset/central-intake-calls/{"csv":"77d6e185-90b2-48d0-94c5-e5cf68265c92" |  open.toronto.ca | dataset | central-intake-calls | {"csv":"77d6e185-90b2-48d0-94c5-e5cf68265c92" |
4. 