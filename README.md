# United Airlines Departure Delay Analysis

## Overview

This project investigates departure delay patterns for United Airlines (UA) using the `nycflights13` dataset in R. Through exploratory data analysis and permutation-based significance testing, we assess how temporal and meteorological factors contribute to delay variability, culminating in data-driven recommendations to optimize scheduling and improve operational resilience.

## Background

Flight delays incur substantial operational costs and passenger dissatisfaction. Understanding the drivers of departure delays enables airlines to implement targeted mitigation strategies, enhance resource allocation, and elevate customer experience.

## Data Source

* **Package**: `nycflights13` (built into RStudio)
* **Scope**: All NYC-origin flights in 2013, filtered for carrier code `"UA"` (United Airlines)
* **Key Fields**:

  * `dep_delay`: Delay in departure time (minutes)
  * `year`, `month`, `day`, `hour`: Scheduled departure timestamp components
  * `temp`, `wind_speed`, `precip`, `visib`: Surface weather measurements at time of departure

## Methodology

1. **Data Preparation**

   * Load `flights` and `weather` tables from `nycflights13`
   * Filter for `carrier == "UA"` and join weather by departure time and origin
2. **Exploratory Data Analysis**

   * Distribution analysis of `dep_delay` (histograms, density plots)
   * Temporal patterns by hour and month
   * Scatterplots correlating delays with weather variables
3. **Statistical Testing**

   * Permutation tests to evaluate significance of observed relationships (α = 0.05)
4. **Interpretation & Recommendations**

   * Synthesize findings into actionable operational strategies

## Key Findings

* **Temporal Effects**: Afternoon (12–18h) departures exhibit a mean delay increase of \~5 minutes compared to early morning flights (p < 0.01).
* **Seasonal Variation**: Peak delays occur during summer months (June–August), with average delays 8% higher than annual baseline (p < 0.05).
* **Weather Impact**: Elevated wind speeds (>15 mph) and precipitation (>0.1 in) are each associated with a 10% increase in delay probability. Low visibility (<5 miles) correlates with a 12% rise in delays.

## Usage

1. **Prerequisites**: R (v4.0+), RStudio, and the following packages installed:

   ```r
   install.packages(c("nycflights13", "dplyr", "ggplot2", "broom", "knitr", "rmarkdown"))
   ```
2. **Reproduce Analysis**: Open and knit `Code.Rmd` in RStudio to regenerate the report and figures.
3. **View Results**: The compiled `UA_Departure_Delays_Report.pdf` contains narrative, tables, and plots.

## Recommendations

* **Schedule Optimization**: Reevaluate flight schedules during identified high-delay hours.
* **Enhanced Weather Monitoring**: Invest in real-time weather analytics and dynamic ground operation adjustments.
* **Passenger Communication**: Deploy automated delay notifications with clear context around weather or operational factors.

## Contributing

Contributions are welcome! Please submit issues or pull requests to enhance analysis, extend methodology, or update documentation.

## Contact

**Sushmitha Meduri**
Master of Science, Data Science
Seattle University
