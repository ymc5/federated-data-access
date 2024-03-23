# federated-data-access
The code performs data analysis on patient records from multiple databases, including counting patients by condition, analyzing patient age distribution, gender distribution, and race distribution.

## Libraries Used
- `tidyverse`: Used for data manipulation and visualization.
- `RPostgres`: For connecting to PostgreSQL databases.
- `connections`: For establishing connections to multiple databases.
- `DBI`: For database interface.
- `yaml`: For reading YAML files.
- `dplyr`: For data manipulation.
- `ggplot2`: For data visualization.

## Objective
The objective of this analysis is to connect to multiple databases, load patient data from each database, and conduct various analyses to understand patient demographics and medical conditions.

## Step 1: Connect to Databases
- Defined a function `establish_connections` to connect to multiple databases using connection information stored in a YAML configuration file.
- Connected to multiple databases simultaneously using the defined function.
- Assigned individual connections to variables for further data extraction.

## Step 2: Load Tables
- Loaded patient data tables from each database separately.
- Filtered out records with missing death dates where applicable.

## Step 3: Data Analysis
### i) Number of Patients
- Calculated the count of distinct patients for each medical condition.
- Visualized the number of patients using a bar graph.

### ii) Age of Patients
- Calculated the age of patients from birthdates.
- Visualized the age distribution of patients for each medical condition using histograms.
- Calculated average, minimum, and maximum age of patients for each medical condition.

### iii) Gender of Patients
- Calculated the percentage of male and female patients for each medical condition.

### iv) Race of Patients
- Calculated the percentage of patients by race for each medical condition.

## Conclusion
The analysis provides insights into the demographics and medical conditions of patients across multiple databases. Further exploration and interpretation of the results can help in understanding trends and patterns related to patient health.
