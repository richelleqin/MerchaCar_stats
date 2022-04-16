# MerchaCar_stats
## Overview
###
The purpose of this project is to:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings
## Linear Regression to Predict MPG

![1](https://user-images.githubusercontent.com/67567087/163654733-887147aa-1ec7-4269-ad34-b1f8fdd448b0.png)

The statistical summary of the linear regression is to determine the quality of the dataset. 

1) Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    - mpg: p = 0 < 0.05; statistically significant; non-random amount of variance
    - vehicle_length: p = 0 <0.05; statistically significant; non-random amount of variance
    - vehicle_weight: p = 0.0776>0.05; not statistically significant; random amount of variance
    - spoiler_angle: p = 0.3069>0.05; not statistically significant; random amount of variance
    - ground_cliearance: p = 0 <0.05; statistically significant; non-random amount of variance
    - AWD: p = 0.1852>0.05; not statistically significant; random amount of variance

2) Is the slope of the linear model considered to be zero? Why or why not?
   - Looking at the coefficients (“Estimate” on the table), the slope of all coefficients are not zero and would give the formula: 
mpg = -.01 + 6.267(vehicle_length)+.001(vehicle_weight)+.069(spoiler_angle)+3.546(ground_clearance)-3.411(AWD). Further looking into the R^2 value (0.7149) indicates that it is not close to zero and thus the slope is not zero. 

3) Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    - R^2 is close to 1 but not close enough (0.7149) with a total p-value being statistically significant. This indicates that the model could be a good predictor for mpg, but there are still many variables at play that could affect its .




