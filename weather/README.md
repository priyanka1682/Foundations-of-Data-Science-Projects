# Precipitation Analysis: Seattle vs. Buffalo Precipitation

> A comparison of daily precipitation in Seattle, WA and Buffalo, NY, built on NOAA weather station data,

---

## Project Overview

Seattle is widely known as a rainy city, but is it actually rainier than a Buffalo, NY? This project uses daily precipitation records from NOAA weather stations in both cities from 2018 to 2022. It cleans, aligns and combines the two datasets, and then compares how often and how much it rains in each city.

- **Objective:** Determine whether Seattle receives more precipitation than Buffalo by comparing cleaned, aligned daily precipitation data from 2018 to 2022.
- **Domain:** Climate / Weather
- **Key Techniques:** Data cleaning and wrangling, exploratory data analysis (EDA), joining DataFrames, tidy data reshaping, missing value imputation, data visualization

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** [NOAA National Centers for Environmental Information (NCEI) – Climate Data Online](https://www.ncei.noaa.gov/cdo-web/) (GHCN-Daily)
- **Description:** Daily weather station observations in CSV format. Key columns include `STATION`, `NAME`, `DATE`, `PRCP` (precipitation, inches), `SNOW` (snowfall) and `SNWD` (snow depth).

---

## Analysis

All analysis is in [`code/Seattle_Weather_Template.ipynb`](code/Seattle_Weather_Template.ipynb). Run the cells from top to bottom. The notebook covers these steps:

1. **Load and explore:** Read both datasets and inspect their columns, data types, sizes, stations and date ranges.
2. **Convert types:** Convert `DATE` to a datetime type and plot daily precipitation for each city.
3. **Select subsets:** Limit the Buffalo data to 2018 onward and to the Buffalo airport station so it matches the Seattle data.
4. **Join and tidy:** Join the two datasets on `DATE`, reshape the result into a tidy format with `city` and `precipitation` columns, and rename columns and values using consistent conventions.
5. **Handle missing values:** Find missing values and omitted dates, then fill each gap with the mean precipitation for that day of the year across all years.
6. **Export:** Save the cleaned dataset as `clean_seattle_stlouis_weather.csv`.

To set up the environment:

```bash
pip install -r requirements.txt
jupyter notebook
```

---

## Results

Include a short discussion of the findings and what they imply.

---

## Authors

- Priyanka - [@priyanka1682](https://github.com/priyanka1682)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used
- Tutorials or papers referenced
- Inspiration or collaborators
