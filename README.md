# Dude, Where’s My Bike?

A data-driven analysis of police-recorded bicycle theft in Berlin using Python, SQL and Tableau.

## Project overview

This project explores reported bicycle theft in Berlin across location, time, bicycle type and recorded financial damage.

The dataset contains **26,965 police-recorded incidents** from **1 January 2025 to 8 August 2026**, covering all **12 Berlin districts** and **534 planning areas**.

## Research questions

* Where are bicycle-theft reports concentrated?
* When are bicycles reported stolen?
* Which bicycle types are reported most often?
* What financial damage is recorded?
* How do district rankings change when population size is considered?

## Tools

- **Google Colab / Python** — data cleaning, validation and exploratory analysis
- **SQLite / SQL** — aggregations, comparisons, rankings and verification
- **Tableau** — interactive dashboards and data visualisation

## Data sources

* [Berlin Police bicycle-theft data](https://daten.berlin.de/datensaetze/fahrraddiebstahl-in-berlin)
* Official Berlin LOR geographic lookup and boundary data
* Berlin population data by LOR planning area, measured on 31 December 2025

## Methodology

The raw data was cleaned and validated in Python. Dates and time fields were converted, LOR codes were preserved as eight-character text values, and additional variables were created for temporal and financial analysis.

The theft records were joined to the official Berlin LOR geographic lookup using the planning-area code. All **26,965 records matched successfully**.

The main calculations were performed in Python and verified with SQL before the results were visualised in Tableau.

## Selected findings

* Mitte recorded the highest total number of reports, but Friedrichshain-Kreuzberg ranked first after accounting for population size.
* During the matching period from 1 January to 8 August, reports fell by **13.9%** from 2025 to 2026.
* Friday had the highest daily average, while Sunday had the lowest.
* Men’s bicycles were the most frequently reported category.
* The median recorded damage in the eligible financial subset was **€899**.

## Repository structure

* `01_Data/` — raw, geographic and processed data
* `02_Notebooks/` — data audit, cleaning and analysis notebooks
* `03_SQL/` — SQLite database and SQL queries
* `04_Tableau/` — final Tableau workbook
* `Dude_Wheres_My_Bike_Final_Presentation.pdf` — final project presentation

## Limitations

The dataset contains police-recorded reports, so unreported incidents are not represented.

Report counts do not measure individual theft risk. The data does not include the number of bicycles or the number of people travelling through each area for work or tourism.

For the financial analysis, attempted thefts, reports without a positive damage value and cellar cases were excluded. Cellar burglary values may include losses involving items other than bicycles.

## Authors

**Halyna Shabarovska and Selina Reuter**

Data Analytics Final Project · August 2026

