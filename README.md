# Momentum Portfolio Alpha:  Fama-French Five-Factor Regime Analysis

**Author:** Syed Bashir Hydari, Pablo Rocha Gomez, Isabella Zhu
**Date:** December 16, 2025

## Project Overview

This project examines whether momentum portfolio returns exhibit statistically significant abnormal performance (alpha) after controlling for the Fama-French Five-Factor model. Using monthly U.S. equity data from 2010-2024, we test for both unconditional alpha and regime-dependent effects across market volatility states. 

### Research Questions
1. Do momentum portfolios earn significant alpha after controlling for FF5 factors?
2. Does momentum's effectiveness vary across high vs. low volatility regimes? 

### Key Findings
- Monthly alpha of 0.29% (~3.5% annually) with marginal statistical significance (p=0.074)
- **Significant negative market beta (-0.28)** indicating defensive/contrarian characteristics
- Momentum's defensive properties **strengthen during high-volatility periods**
- FF5 factors explain only 23.7% of momentum variance, suggesting unique return dimensions

## Methodology

- **Data Source:** Kenneth R. French Data Library
- **Sample Period:** January 2010 - December 2024 (180 monthly observations)
- **Models:** 
  - Model A: Standard FF5 factor regression
  - Model B:  Regime-interaction model with volatility-dependent betas
- **Statistical Methods:** OLS regression with Newey-West HAC robust standard errors
- **Regime Definition:** 12-month rolling volatility median split

## Repository Contents

- `Final-Code.rmd` - Complete R Markdown source code with data acquisition, analysis, and reporting
- `Final-Report.pdf` - Compiled academic report with full results and interpretation

## Reproducibility

### Requirements
- R (version 4.0+)
- Quarto
- Required R packages: `tidyverse`, `lubridate`, `knitr`, `kableExtra`, `zoo`, `car`, `lmtest`, `sandwich`, `ggfortify`

### How to Reproduce
1. Clone this repository
2. Open `Final-Code.rmd` in RStudio
3. Install required packages if needed: `install.packages(c("tidyverse", "lubridate", ...))`
4. Render the document: Click "Render" or run `quarto render Final-Code.rmd`
5. The analysis will automatically download data from the French Data Library and regenerate all results

**Note:** All data is downloaded programmatically during rendering - no manual data files needed.

## Key Visualizations

The analysis includes:
- Time series plots of momentum returns across volatility regimes
- Scatterplots showing momentum's negative correlation with market returns
- Diagnostic plots for model validation
- Correlation heatmaps of factor relationships

## Academic Context

This project was completed for [Course Name/Code] at [Institution], Fall 2024. The analysis follows established methodologies from:
- Jegadeesh & Titman (1993) - Original momentum documentation
- Fama & French (2015) - Five-factor asset pricing model
- Carhart (1997) - Momentum factor construction

## Citation

If you reference or build upon this work, please cite as:
Hydari, S. B., Rocha Gomez, P., & Zhu, I. (2025). Do Momentum Portfolio Returns Exhibit Abnormal Performance After Controlling for Fama-French Five Factors? A Regime-Dependent Analysis of Factor-Adjusted Returns. GitHub repository: https://github.com/syedhydari/momentum-alpha-ff5-regime-analysis

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

- Syed Bashir Hydari - [GitHub: @syedhydari](https://github.com/syedhydari)
- For questions about methodology or results, please open an issue

---

**Academic Integrity Notice:** This project represents original work completed for academic purposes. If you use this code or methodology for your own academic work, proper citation is required per your institution's academic integrity policies. 
