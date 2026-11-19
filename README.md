# A/B Landing Page Experiment

**Author:** [Rodrigo Garza García](https://www.linkedin.com/in/rodrigogarzamx/)  
**Professional focus:** Public & International Affairs · Business Analysis · Data Analytics  
**Portfolio page:** [A/B Landing Page Experiment](https://rogarzag.github.io/projects/ab-landing-page/)  
**GitHub repository:** [ab-landing-page-experiment](https://github.com/rogarzag/ab-landing-page-experiment)  
**Project focus:** Data Analytics · A/B Testing · Conversion Rates · Statistical Tests  
**Project context:** Data Analytics portfolio project  
**Data / project coverage:** 40,000 user observations; experiment dates not specified in the project data summary  
**Professional links:** [GitHub profile](https://github.com/rogarzag) · [LinkedIn](https://www.linkedin.com/in/rodrigogarzamx/) · [Professional Website](https://rogarzag.github.io/)

## Project Overview



This project evaluates an A/B experiment conducted on two landing page versions, **A** and **B**, to determine which version performs better in terms of **conversion rate** and **average spending among converted users**.

The analysis also checks whether conversion differs by **traffic source** or **user type**. Statistical tests are used to see whether the differences in the data are strong enough to be meaningful.

## Business Questions

The project addresses four main questions:

1. Which landing page generates a higher conversion rate and higher average spending?
2. Which traffic sources are more effective at generating conversions?
3. Are there significant differences in conversion by user type?
4. What business actions are supported by the experiment results?

## Dataset

The dataset contains **40,000 observations** and **9 variables**:

- `user_id` — Unique user identifier
- `date` — Date on which the user was exposed to the page
- `landing` — Landing page version shown (`A` or `B`)
- `region` — User geographic region
- `dispositivo` — Device type
- `traffic_source` — Acquisition channel
- `user_type` — New or returning user
- `converted` — Conversion indicator (`0` or `1`)
- `gasto` — Amount spent by the user

The data contains no missing values, and each record represents a unique user.

## Methodology

The analysis follows these steps:

1. Data validation and exploratory analysis
2. Comparison of average spending between pages A and B
3. Comparison of conversion rates between pages A and B
4. Analysis of the relationship between traffic source and conversion
5. Analysis of the relationship between user type and conversion
6. Visualization of categorical results
7. Executive business interpretation and recommendations

### Statistical Tests

- **Levene's test** to assess equality of variances
- **Welch's t-test** to compare average spending between converted users on pages A and B
- **Two-proportion Z-test** to compare conversion rates
- **Chi-square test of independence** to test associations between categorical variables
- **Cramér's V** to check how strong the link is between traffic source and conversion

## Key Findings

### Page A vs Page B

- **Conversion rate**
  - Page A: **12.57%**
  - Page B: **15.96%**
  - Difference: **+3.38 percentage points** in favor of page B
  - The difference is statistically significant.

- **Average spending among converted users**
  - Page A: **61.09**
  - Page B: **68.75**
  - Page B is approximately **12.5% higher**
  - The difference is statistically significant.

Overall, **page B outperforms page A on both conversion and average spending among converted users**.

### Traffic Source

Conversion rates were:

- Email: **14.99%**
- Ads: **14.74%**
- Referral: **13.88%**
- Organic: **13.79%**

The chi-square test found a statistically significant association between traffic source and conversion. However, **Cramér's V ≈ 0.015**, indicating that the relationship is **very weak**.

### User Type

- New users: **14.36%**
- Returning users: **14.09%**

No statistically significant association was found between user type and conversion. The higher absolute number of conversions among new users is mainly explained by their larger share of the sample rather than higher conversion effectiveness.

## Business Recommendations

- **Prioritize page B** as the candidate version for implementation.
- Do not reallocate acquisition resources based only on traffic-source conversion rates, since the observed association is very weak.
- Do not prioritize different conversion strategies for new and returning users based on this experiment alone.
- As a next step, compare traffic source and user type separately for pages A and B. This will help check whether the overall results also hold within each page version.
- Complement the implementation decision with profitability and cost metrics.

## Reproducibility

The dataset used in the analysis is included in the `data/` directory. The notebook uses relative paths and is structured to execute from top to bottom in Jupyter Notebook.

## Technologies

- Python
- pandas
- NumPy
- Matplotlib
- SciPy
- statsmodels
- Jupyter Notebook

## Conclusion

In this dataset, page B had a higher conversion rate and higher average spending among users who converted. The differences were statistically significant. Traffic source had only a very weak link with conversion, while the results did not show a meaningful difference between new and returning users. Page B is the stronger option to review further, but costs and profit should also be considered before making a rollout decision.
