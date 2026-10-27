# Global Fuel Prices and Taxation Dashboard (2020–2026)

An interactive Tableau analytics project exploring global petrol, diesel, and LPG prices alongside Brent crude oil prices and fuel taxation. The workbook brings together geographic views, time-series trends, regional tax comparisons, and country-level fuel comparisons to help users explore how fuel prices and tax rates vary across countries and over time.

## Project Overview

Fuel prices are influenced by multiple factors, including crude oil prices, taxation, regional conditions, income levels, and government subsidy policies. This project uses a global dataset to explore these relationships through visual analytics.

**Project type:** Data analytics and visualization  
**Primary tool:** Tableau  
**Dataset format:** CSV embedded in the packaged Tableau workbook (`.twbx`)  
**Coverage:** 84 countries across 7 regions  
**Date range in the dataset:** 6 January 2020 – 6 April 2026  
**Records:** 27,468  
**Fields:** 10

> The dataset ends on 6 April 2026. “2020–2026” describes the available date range, not a complete calendar year of 2026.

## Project Objectives

- Compare petrol, diesel, and LPG prices across countries and regions.
- Explore how fuel prices change over time.
- Visualize geographic differences in petrol and diesel prices.
- Compare average fuel-tax percentages across regions and countries.
- Examine fuel-price patterns by income level and subsidy level where those categories are available.
- Present key metrics and comparisons in a Tableau workbook that is easier to explore than a raw spreadsheet.

## Dataset

The packaged workbook contains the source CSV under its `Data/Downloads/` folder. The dataset contains 27,468 records and no missing values in the ten fields checked in the included data.

| Column | Description |
|---|---|
| `date` | Date associated with the observation |
| `country` | Country name |
| `region` | Geographic region |
| `income_level` | Income category assigned in the dataset |
| `subsidy_level` | Subsidy category assigned in the dataset |
| `petrol_usd_liter` | Petrol price in USD per liter |
| `diesel_usd_liter` | Diesel price in USD per liter |
| `lpg_usd_liter` | LPG price in USD per liter |
| `brent_crude_usd` | Brent crude oil price, recorded in USD per barrel |
| `tax_percentage` | Fuel tax percentage recorded in the dataset |

### Dataset coverage

- **Countries:** 84
- **Regions:** 7
- **Start date:** 2020-01-06
- **End date:** 2026-04-06
- **Rows:** 27,468
- **Columns:** 10
- **Missing values:** None found in the included CSV during inspection

## Tools and Technologies

- **Tableau Desktop** — dashboards, charts, and story presentation
- **CSV** — source data included inside the packaged workbook
- **GitHub** — project versioning and sharing

This repository describes the Tableau workbook and its embedded data. It does not claim a separate Flask web application, SQL pipeline, or automated performance-testing suite unless those components are added separately.

## Visualizations in the Workbook

The workbook contains 14 worksheets and 4 dashboards. The worksheets include:

- **KPI cards:** average petrol price, diesel price, LPG price, and average tax rate
- **Global Petrol Price Map:** geographic view of petrol prices
- **Global Diesel Price Map:** geographic view of diesel prices
- **Petrol Price Trends:** petrol price trends over time
- **Diesel Price Trends:** diesel price trends over time
- **LPG Price Trends:** LPG price trends over time
- **Brent Crude Oil Price Trends (2020–2026):** Brent crude price trends over time
- **Average Tax by Region:** regional tax comparison
- **Highest Tax-Paying Nations:** country-level tax comparison
- **Fuel Type Comparison:** comparison across fuel measures
- **Top 3 Countries Fuel Comparison:** comparison of fuel measures for selected leading countries

### Dashboards

| Dashboard | Main focus |
|---|---|
| `1 - Global Overview` | High-level global overview and KPI indicators |
| `02 - Fuel Trends` | Fuel-price trends and comparisons |
| `03 - Tax & Country Analysis` | Taxation and country-level comparisons |
| `Global Fuel Prices and Taxation — Story` | Story-style presentation that brings selected workbook views together |

The workbook includes four dashboards. Exact appearance and interactivity depend on the Tableau version and how the workbook is opened.

## Key Dataset Summary

The following are descriptive averages calculated directly from the CSV embedded in the workbook. They summarize the included dataset; they are not forecasts or official policy conclusions.

| Metric | Dataset average |
|---|---:|
| Petrol price | USD 2.282 per liter |
| Diesel price | USD 2.134 per liter |
| LPG price | USD 1.711 per liter |
| Brent crude oil price | USD 107.982 per barrel |
| Tax percentage | 26.774% |

Country, date, and policy categories can affect comparisons. These overall averages should therefore be interpreted as dataset-level summaries rather than as values that apply to every country or every date.

## How to Open the Project

1. Download or clone this repository from GitHub.
2. Locate the packaged Tableau workbook (`.twbx`) in the repository.
3. Open the `.twbx` file using a compatible version of Tableau Desktop.
4. If Tableau displays a compatibility or version notice, follow the prompts provided by Tableau.
5. Explore the worksheets, dashboards, filters, and story using the workbook controls.

### Why the `.twbx` file is useful

A Tableau Packaged Workbook (`.twbx`) can include workbook content and supporting local data files. This project’s uploaded `.twbx` contains the CSV source data, so the source CSV does not need to be separately reconnected for the packaged workbook to access that embedded copy.

## Repository Contents

The main deliverable is the packaged Tableau workbook. A typical repository layout is:

```text
global-fuel-prices-tableau/
├── README.md
└── Global_Fuel_Prices_Taxation_Dashboard.twbx
```

Your actual GitHub repository may contain additional files. Update this section if you add SQL scripts, screenshots, documentation, or a demo video link.

## Methodology and Interpretation

The project uses Tableau to summarize and compare the dataset through geographic maps, time-series charts, KPI views, and categorical comparisons. Filters available in individual worksheets can help narrow the analysis by region, country, or measure.

Please keep the following points in mind:

- The dataset’s categories and recorded values are treated as supplied; this README does not independently verify them against official national statistics.
- Correlation or visual similarity between Brent crude prices, fuel prices, and tax rates does not by itself establish causation.
- Differences between countries can reflect multiple factors that are not represented in the dataset.
- The end date is 6 April 2026; there are no observations after that date in the included CSV.

## Limitations

- The analysis is limited to the fields and date range present in the source dataset.
- The dataset does not, by itself, explain every reason for cross-country price differences.
- The workbook is a Tableau visualization project; a separate hosted web application is not included in this description.
- Interactive online viewing depends on the publishing or sharing options available to the Tableau account and environment used.

## Possible Future Improvements

- Add documented SQL scripts for repeatable data validation and analysis.
- Add screenshots of the completed dashboards to the repository.
- Include a short demonstration-video link.
- Document any data-cleaning or transformation steps if they are performed separately.
- Add further analysis of relationships among crude oil prices, fuel prices, taxes, income categories, and subsidy categories.
- Publish an accessible online version if the available Tableau licensing and sharing options support it.

## Author

**Archit Chhabda**  
B.Tech Computer Science and Engineering

## License and Data Attribution

No license or original dataset source is specified in this README. Before redistributing the workbook or source data publicly, add the appropriate license and attribution details for the dataset and any third-party materials used.

---

*This README describes the contents of the supplied packaged Tableau workbook and its embedded CSV. Update it whenever the project files, charts, or repository structure change.*
