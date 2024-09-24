#Vaccine cases by year

## Overview

This project performs a time series analysis on measles cases in the U.S. over the years, with a focus on analyzing the effects of a vaccine introduced in 1963. The project involves fitting regression models, transforming the data, and correcting for correlation using the Cochrane-Orcutt procedure. The analysis includes exploring how measles cases changed before and after the introduction of the vaccine.

## Objectives

- Analyze the relationship between the number of measles cases and time.
- Investigate the effect of the measles vaccine on the number of cases.
- Fit models to detect and correct for correlation in the data using time series methods.
- Perform separate analyses for pre- and post-vaccine introduction data.

## Key Processes

1. **Data Exploration and Visualization**  
   Visualizing the relationship between measles cases and years to identify patterns.
   
2. **Log Transformation**  
   Applying a log transformation to correct for non-linearity in the data and to stabilize variance.
   
3. **Model Fitting**  
   Fitting regression models, including a year-vaccine interaction model to understand how the vaccine influenced the number of cases.
   
4. **Cochrane-Orcutt Procedure**  
   Accounting for correlation in residuals by applying the Cochrane-Orcutt procedure to adjust the regression models.
   
5. **Separate Analyses for Pre- and Post-Vaccine Data**  
   Fitting models separately for the data before and after the vaccine's introduction to explore the impact of the vaccine over time.

## Tools and Technologies

- **R**: The entire analysis was conducted using R.
  - `Sleuth3`: Dataset library used for fetching the measles cases data.
  - `TSA`: Applied for time series analysis and correlation detection.
  - `orcutt`: Used for performing the Cochrane-Orcutt procedure to correct for autocorrelation.
  
## Results

- **Pre-Vaccine Data Analysis**  
   Before the vaccine was introduced, the number of measles cases showed no significant yearly trend, and there was no evidence of autocorrelation.
   
- **Post-Vaccine Data Analysis**  
   After the introduction of the vaccine, the number of measles cases decreased by about 0.08 units per year, and the time series model detected some level of correlation, which was adjusted for using the Cochrane-Orcutt procedure.

- **Vaccine-Year Interaction**  
   The interaction model revealed that the vaccine had a significant impact on the number of measles cases when first introduced, but no sustained significance was detected in later years without considering autocorrelation.

## Conclusion

The analysis indicates that while there was a sharp decrease in measles cases following the introduction of the vaccine, the yearly effect of the vaccine was not significant when viewed across the entire timeline. Correcting for autocorrelation confirmed the decrease in cases after the vaccine was introduced.

## Discussion

In time series models like AR(1), where correlation is assumed to be constant over time, failure to account for autocorrelation could lead to incorrect inferences. This project demonstrates the importance of testing for and correcting such correlations to ensure valid results in time series data.


