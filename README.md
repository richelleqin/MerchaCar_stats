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
    - R^2 is close to 1 but not close enough (0.7149) with a total p-value being statistically significant. This indicates that the model could be a good predictor for mpg, but there are still many variables at play that could affect its.

## Summary Statistics on Suspension Coils

![2](https://user-images.githubusercontent.com/67567087/163655029-65cee33e-a308-410a-9f32-7c2ed1f551ec.png)

![3](https://user-images.githubusercontent.com/67567087/163655035-e18bcd9f-5e65-44d9-8f9b-a7d3b034c838.png)

The mean is 1498.78 for this sample and the population mean was determined to be 1500.

Looking into the overall variance, it is 62.3 which is less than 100, fitting the requirements of 100 pounds per square inch. However looking into the lots, it would show that Lot3 has a variance of 170.3, much higher than the required 100 pounds per square inch. Thus, the current manufacturing data meets the design specification in total and for lot 1 and 2. Lot 3 does not meet the design specification.

## T-Tests on Suspension Coils

![for all](https://user-images.githubusercontent.com/67567087/163655100-279673c8-534e-4aa2-9289-f92fe6ce9613.png)

![for 1](https://user-images.githubusercontent.com/67567087/163655103-311506aa-75ed-4c5c-8942-95b42f0ab09e.png)

![for 2](https://user-images.githubusercontent.com/67567087/163655107-8a50ca80-0ba7-477f-a858-cca7b7cf89cd.png)

![for 3](https://user-images.githubusercontent.com/67567087/163655113-dd9470bd-0fed-49ac-95c0-870e5a7aa746.png)

- The overall manufacturing, Lot 1, and Lot 2 do not have sufficient statistical evidence to reject the null hypothesis (i.e. p>0.05), which shows the two means are statistically similar.
- Lot1: p-value = 1, alpha = .05, 1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
- Lot2: Lot 2: p-value = .6072, alpha = .05, .60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
- Lot3: p-value = .04168, alpha = .05, .04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

## Study Design: MechaCar vs Competition

To compare MechaCar to its competitors, serveral factors could be considered.

- What metric or metrics are you going to test?
    - The next metrics to test should be the cost, horsepower, and highway fuel efficiency, which addresses consumer’s recent need to be cost effective in the inflating economy.

- What is the null hypothesis or alternative hypothesis?
    - The null hypothesis is that the mean of the cost to fuel rating is zero. The alternative hypothesis is that the mean of the cost to fuel rating is not zero.

- What statistical test would you use to test the hypothesis? And why?
    - Using a multiple linear regression statistical summary would show how the variables impact the cost to fuel rating for MechaCar and their competitors.
    - 
- What data is needed to run the statistical test?
    - A random sample for MechaCar and their competitor, would need to be collected to include the distance travelled on a full tank, cost for a full tank, cost of vehicle, horsepower, fuel efficiency at 60km/hr, fuel efficiency at 100km/hr.
