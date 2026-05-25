# Beyond Crime Counts: Chicago Neighborhood Safety Profiles

## Project Overview

This project analyzes reported crime patterns across Chicago community areas from 2020 to 2024. It combines City of Chicago crime incident data with community-area socioeconomic indicators.

The target audience is Chicago public safety planners, community development analysts, and neighborhood organizations. The main goal is to show why total reported crime count alone is not enough to describe neighborhood safety. A more useful profile combines crime volume, violent-crime share, domestic-related share, and socioeconomic context.

## Files

- `Final_Project.ipynb`: Polished Python notebook for data loading, cleaning, merging, EDA, feature engineering, and modeling.
- `SQL_Project.ipynb`: Separate SQL notebook with validation queries, joins, grouped comparisons, rankings, and additional socioeconomic investigation.
- `Presentation_Slide.pdf`: PDF version of the in-class presentation deck.
- `README.md`: Project overview and file guide.

## Data

The project uses two datasets from the City of Chicago Data Portal:

- Chicago Crimes Data: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2
- Selected Socioeconomic Indicators in Chicago: https://data.cityofchicago.org/Health-Human-Services/Selected-socioeconomic-indicators-by-neighborhood/i9hv-en6g

The crime dataset is loaded through the API because it is too large to upload directly to GitHub. The analysis focuses on reported incidents from 2020 to 2024 and aggregates them to Chicago’s 77 community areas.

## Python Workflow

The Python notebook provides the main analysis. It loads the data through APIs, cleans and merges the datasets, conducts EDA, builds community-level crime measures, and runs descriptive regression models.

Key Python outputs include:

- Citywide crime type and yearly trend analysis.
- Community-level crime concentration analysis.
- Comparisons between total crime volume and violent-crime share.
- Hardship-group analysis for violent-crime and domestic-related shares.
- Risk profile classification based on crime volume and violent-crime share.
- Descriptive models for violent-crime share and domestic-related share.

## SQL Workflow

The SQL notebook is separate from the Python notebook. It reloads and cleans the data, stores it in SQLite, aggregates crime data to the community-area level, and joins crime summaries with socioeconomic indicators.

The SQL analysis supports and extends the Python findings by:

- Validating 1.18M+ crime records and all 77 community areas.
- Identifying high-volume communities by hardship type.
- Finding high-volume / lower-violent-share communities and lower-volume / higher-violent-share communities.
- Ranking communities by violent-crime share using a SQL window function.
- Extending the analysis to unemployment, age dependency, and combined unemployment-dependency profiles.

## Main Findings

- Reported crime is concentrated across community areas, but high-volume areas are not all the same.
- Total crime volume and violent-crime share measure different types of risk.
- Hardship is more clearly aligned with violent-crime share and domestic-related share than with raw crime volume.
- Socioeconomic indicators such as unemployment and dependency add useful context for identifying more severe crime profiles.
- For planning purposes, neighborhoods should be evaluated using crime volume, severity mix, and socioeconomic context together.

## Limitations

This analysis is descriptive, not causal. Reported crime counts are not population-normalized, so future work should add crime rates per 1,000 residents. Additional data on land use, transit, business activity, police staffing, and population mobility would also improve the analysis.

## Final Takeaway

Total reported crime count alone is not enough. A more useful neighborhood safety profile combines crime volume, violent-crime share, domestic-related share, and socioeconomic context.
