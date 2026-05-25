# Final-Project
This project analyzes reported crime patterns across Chicago community areas from 2020 to 2024. It combines two City of Chicago datasets: incident-level crime records and community-area socioeconomic indicators. The main goal is to explore how crime patterns differ across neighborhoods and how those patterns relate to poverty rate, per capita income, and hardship index.

## Files

- `Final_Project.ipynb`: Python notebook for data loading, cleaning, merging, EDA, and modeling
- `SQL_Project.ipynb`: SQL notebook for database-style queries and supporting analysis
- `README.md`: Project overview

## Data

The project uses two datasets from the City of Chicago Data Portal:

1. Chicago Crimes Data: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2
2. Selected Socioeconomic Indicators in Chicago: https://data.cityofchicago.org/Health-Human-Services/Selected-socioeconomic-indicators-by-neighborhood/i9hv-en6g

The crime dataset is loaded through the API because it is too large to upload directly to GitHub.

## Python Workflow
The Python notebook loads Chicago crime and socioeconomic data through APIs, cleans and merges them at the community-area level, then uses EDA and linear regression models to study how neighborhood crime profiles relate to poverty, income, and hardship.

The key finding is that total reported crime volume alone does not fully capture neighborhood safety: some areas have high crime counts but lower violent-crime shares, while higher hardship and poverty are strongly associated with higher violent-crime share and domestic-related crime share.

## SQL Workflow

The SQL notebook supports the analysis using SQL queries. It includes:

- Table validation
- Community-level crime summaries
- Joins between crime and socioeconomic data
- Filtering neighborhoods by crime and hardship conditions
- Ranking communities by total crimes and violent crime share
