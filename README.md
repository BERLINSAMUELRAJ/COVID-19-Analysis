# COVID-19 Analysis: COVID Deaths and Vaccinations
![Corona Analysis LOGO](https://github.com/BERLINSAMUELRAJ/COVID-19-Analysis/blob/main/GITHUB%20INSIDE.jpeg)
This project contains an SQL-based analysis of COVID-19 deaths and vaccinations, based on two datasets:

- **COVID Deaths**: Data related to COVID-19 cases, deaths, and other health indicators.
- **COVID Vaccinations**: Data on the progress of COVID-19 vaccination efforts.

## Project Overview

The goal of this project is to provide insights into the relationship between COVID-19 vaccination rates and COVID-19 deaths across various regions and time periods. By analyzing this data, we aim to assess trends, compare death rates with vaccination coverage, and explore other factors such as healthcare infrastructure and socio-economic conditions.

## Tables Description

### 1. COVID Deaths Table

This table contains detailed information about COVID-19 deaths, cases, and various health metrics related to the pandemic.

#### Columns:

- `iso_code` (VARCHAR): ISO code of the country/region.
- `continent` (VARCHAR): Continent of the region.
- `location` (VARCHAR): The specific location or country name.
- `date` (DATE): Date of the record.
- `population` (INT): Population of the region.
- `total_cases` (INT): Total number of COVID-19 cases.
- `new_cases` (INT): New COVID-19 cases for the day.
- `new_cases_smoothed` (INT): Smoothed new cases (for trend analysis).
- `total_deaths` (INT): Total number of COVID-19 related deaths.
- `new_deaths` (INT): New deaths for the day.
- `new_deaths_smoothed` (INT): Smoothed new deaths.
- `total_cases_per_million` (FLOAT): Total cases per million people.
- `new_cases_per_million` (FLOAT): New cases per million people.
- `new_cases_smoothed_per_million` (FLOAT): Smoothed new cases per million.
- `total_deaths_per_million` (FLOAT): Total deaths per million.
- `new_deaths_per_million` (FLOAT): New deaths per million.
- `new_deaths_smoothed_per_million` (FLOAT): Smoothed new deaths per million.
- `reproduction_rate` (FLOAT): Estimated reproduction rate of the virus.
- `icu_patients` (INT): Number of ICU patients due to COVID-19.
- `icu_patients_per_million` (FLOAT): ICU patients per million.
- `hosp_patients` (INT): Number of hospitalized COVID-19 patients.
- `hosp_patients_per_million` (FLOAT): Hospitalized patients per million.
- `weekly_icu_admissions` (INT): Weekly ICU admissions.
- `weekly_icu_admissions_per_million` (FLOAT): Weekly ICU admissions per million.
- `weekly_hosp_admissions` (INT): Weekly hospital admissions.
- `weekly_hosp_admissions_per_million` (FLOAT): Weekly hospital admissions per million.
- `new_tests` (INT): New tests conducted.
- `total_tests` (INT): Total number of tests conducted.
- `total_tests_per_thousand` (FLOAT): Total tests per thousand people.
- `new_tests_per_thousand` (FLOAT): New tests per thousand people.
- `new_tests_smoothed` (INT): Smoothed new tests.
- `new_tests_smoothed_per_thousand` (FLOAT): Smoothed new tests per thousand.
- `positive_rate` (FLOAT): Percentage of tests that returned positive.
- `tests_per_case` (FLOAT): Tests per reported case.
- `tests_units` (VARCHAR): Units used for tests.
- `total_vaccinations` (INT): Total number of vaccinations.
- `people_vaccinated` (INT): Number of people vaccinated.
- `people_fully_vaccinated` (INT): Number of people fully vaccinated.
- `new_vaccinations` (INT): New vaccinations conducted.
- `new_vaccinations_smoothed` (INT): Smoothed new vaccinations.
- `total_vaccinations_per_hundred` (FLOAT): Total vaccinations per 100 people.
- `people_vaccinated_per_hundred` (FLOAT): People vaccinated per 100.
- `people_fully_vaccinated_per_hundred` (FLOAT): Fully vaccinated people per 100.
- `new_vaccinations_smoothed_per_million` (FLOAT): Smoothed new vaccinations per million.
- `stringency_index` (FLOAT): Stringency of lockdown measures.
- `population_density` (FLOAT): Population density of the region.
- `median_age` (FLOAT): Median age of the population.
- `aged_65_older` (FLOAT): Percentage of population aged 65 or older.
- `aged_70_older` (FLOAT): Percentage of population aged 70 or older.
- `gdp_per_capita` (FLOAT): GDP per capita of the region.
- `extreme_poverty` (FLOAT): Percentage of population living in extreme poverty.
- `cardiovasc_death_rate` (FLOAT): Cardiovascular death rate per 100,000 people.
- `diabetes_prevalence` (FLOAT): Diabetes prevalence rate.
- `female_smokers` (FLOAT): Percentage of female smokers.
- `male_smokers` (FLOAT): Percentage of male smokers.
- `handwashing_facilities` (FLOAT): Percentage of population with access to handwashing facilities.
- `hospital_beds_per_thousand` (FLOAT): Hospital beds per thousand people.
- `life_expectancy` (FLOAT): Life expectancy of the region.
- `human_development_index` (FLOAT): Human development index score.

### 2. COVID Vaccinations Table

This table contains data on the progress of COVID-19 vaccinations, including the number of people vaccinated and other related health metrics.

#### Columns:

- `iso_code` (VARCHAR): ISO code of the country/region.
- `continent` (VARCHAR): Continent of the region.
- `location` (VARCHAR): The specific location or country name.
- `date` (DATE): Date of the record.
- `new_tests` (INT): New tests conducted.
- `total_tests` (INT): Total number of tests conducted.
- `total_tests_per_thousand` (FLOAT): Total tests per thousand people.
- `new_tests_per_thousand` (FLOAT): New tests per thousand people.
- `new_tests_smoothed` (INT): Smoothed new tests.
- `new_tests_smoothed_per_thousand` (FLOAT): Smoothed new tests per thousand.
- `positive_rate` (FLOAT): Percentage of tests that returned positive.
- `tests_per_case` (FLOAT): Tests per reported case.
- `tests_units` (VARCHAR): Units used for tests.
- `total_vaccinations` (INT): Total number of vaccinations.
- `people_vaccinated` (INT): Number of people vaccinated.
- `people_fully_vaccinated` (INT): Number of people fully vaccinated.
- `new_vaccinations` (INT): New vaccinations conducted.
- `new_vaccinations_smoothed` (INT): Smoothed new vaccinations.
- `total_vaccinations_per_hundred` (FLOAT): Total vaccinations per 100 people.
- `people_vaccinated_per_hundred` (FLOAT): People vaccinated per 100.
- `people_fully_vaccinated_per_hundred` (FLOAT): Fully vaccinated people per 100.
- `new_vaccinations_smoothed_per_million` (FLOAT): Smoothed new vaccinations per million.
- `stringency_index` (FLOAT): Stringency of lockdown measures.
- `population_density` (FLOAT): Population density of the region.
- `median_age` (FLOAT): Median age of the population.
- `aged_65_older` (FLOAT): Percentage of population aged 65 or older.
- `aged_70_older` (FLOAT): Percentage of population aged 70 or older.
- `gdp_per_capita` (FLOAT): GDP per capita of the region.
- `extreme_poverty` (FLOAT): Percentage of population living in extreme poverty.
- `cardiovasc_death_rate` (FLOAT): Cardiovascular death rate per 100,000 people.
- `diabetes_prevalence` (FLOAT): Diabetes prevalence rate.
- `female_smokers` (FLOAT): Percentage of female smokers.
- `male_smokers` (FLOAT): Percentage of male smokers.
- `handwashing_facilities` (FLOAT): Percentage of population with access to handwashing facilities.
- `hospital_beds_per_thousand` (FLOAT): Hospital beds per thousand people.
- `life_expectancy` (FLOAT): Life expectancy of the region.
- `human_development_index` (FLOAT): Human development index score.

## SQL Queries

The project uses SQL queries to extract valuable insights, such as:

- **COVID Death Trends**: Queries to analyze death rates over time and across different regions.
- **Vaccination Trends**: Queries to track vaccination rates and progress.
- **Impact of Vaccinations on Death Rates**: Analysis comparing vaccination rates with death rates.
- **Healthcare Indicators**: Queries to explore correlations between healthcare infrastructure (e.g., ICU beds, hospital beds, etc.) and COVID-19 outcomes.

### 1. Count the Number of Movies vs TV Shows
```sql
SELECT TYPE, COUNT(TYPE) AS TOTAL_COUNT FROM NETFLIX_TITLES
GROUP BY TYPE
ORDER BY TOTAL_COUNT DESC;
GO
```
