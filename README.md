# UK Road Accident Data Analysis 2020
## Project Overview
This project explores, cleans, and analyzes UK road accident data from 2020, sourced from the Department for Transport. The data consists of over 50 attributes per accident including location, vehicle details, driver and casualty information, and environmental conditions. The objective is to uncover trends, patterns, and factors contributing to accident severity, and to provide actionable recommendations for improving road safety.

## Tools & Technologies
   * Python
   * Pandas
   * NumPy
   * Matplotlib & Seaborn
   * Scikit-learn
   * SQL (Data Extraction)

## Data Cleaning
The raw dataset required significant preprocessing:
   * Addressed missing values in critical columns such as coordinates, police force, and accident conditions.
   * Replaced placeholder values (-1, 0, 9, 99) with NaN and filled them using appropriate methods like mode imputation, forward fill, or KDE.
   * Used the STATS20 and Doogal resources to map local authority districts and resolve out-of-range or unknown values.
   * Merged cleaned accident, casualty, and vehicle tables using SQL joins and transformed into a consolidated pandas dataframe.

## Exploratory Data Analysis
Key findings include:
   * Peak accident time: 17:00 on Fridays.
   * High-risk zones: Liverpool (Merseyside), Hull (Humberside), and East Riding regions.
   * Vehicle types: Motorcycles (up to 125cc and 500cc) and larger motorcycles frequently involved.
   * Demographics: Majority of accidents involved male drivers and occurred at non-junction locations.
   * Environmental factors: Most accidents occurred under fine weather, daylight conditions, and on dry road surfaces.

## Machine Learning & Insights
   * Association Rule Mining: Identified correlations between driver gender, location, road conditions, and accident severity.
   * Outlier Detection: Used Isolation Forest to assess and retain meaningful outliers relevant to domain-specific scenarios.
   * Classification Models: Compared datasets with and without outliers using Random Forest, achieving up to 82% accuracy.
   * Key predictors: Speed limit, number of vehicles involved, road type, driver maneuver, and junction detail.

## Geographic Analysis
Generated cluster maps for accident density in:
   * Kingston upon Hull
   * Humberside region
   * East Riding of Yorkshire

## Recommendations
   * Enforce reduced speed limits on A-class roads in rural areas.
   * Prohibit driving for individuals aged 80+ due to higher fatality rates.
   * Install additional pedestrian crossing facilities within 50 meters in high-risk areas.
   * Introduce more road signage on rural A-class roads and blind junctions.
