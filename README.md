# Does growth still mean carbon?

A regression of fossil CO2 emissions per person on GDP per person for 164 countries in 2022, built for a GW data science assignment (week 10). In logs, each 1 percent of extra income goes with about 1.05 percent more CO2 per person (95 percent CI 0.97 to 1.12, R squared 0.83). A quadratic term shows the curve bends, but its peak would sit at about $2.8 million per person, far outside the data.

The notebook has a seaborn regplot and jointplot with confidence bands, a correlation heatmap (static and Plotly), a residual plot with a LOWESS smoother, the statsmodels summaries, a connected Altair view (brush and legend selection) and a Plotly scatter with an OLS trendline.

## Data

- Our World in Data (2026) CO2 dataset, `owid/co2-data` on GitHub: Global Carbon Budget emissions and Maddison Project 2023 GDP. Codebook in `data/`.
- ISO 3166 countries with regional codes, `lukes/ISO-3166-Countries-with-Regional-Codes` on GitHub.

## Running it

```
pip install -r requirements.txt
quarto render week10_assignment.ipynb --execute
```

`vl-convert-python` lets Altair embed the Vega libraries in the page, which avoids a loading conflict with Plotly and makes the chart work offline.

## Author

Souheil Mouhajir, Elliott School of International Affairs, The George Washington University.
