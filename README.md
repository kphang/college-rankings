# College Rankings
An analysis of U.S. college rankings issued by various ranking organizations compared against that cohort's future earnings and employment data based on data taken from the U.S. Department of Education College Scorecard. Because discipline can have a significant impact on earnings, we attempted to factor this out by calculating an expected value for each cohort based on the breakdown of degree types issued for each college in conjunction with U.S. Census data. Various metrics were created against which rankings could be scored. Rankings were assessed on: (1) their success in identifying top-n colleges, (2) ranking correlation (using Spearman and Kendall), and (3) the the range and dispersal of errors.

This code was used as part of a school project. 

## Notes on Functionality
Due to the large and numerous data sources involved, rather than loading these sources into memory each time, the relevant data was first extracted into a smaller single file version of each data set. In the future, code was run to load this pre-compiled data.


# Data Sources
## College Scorecard
Taken from the U.S. Department of Education's College Scorecard data to provide future results against which rankings were scored.

## Census Data
U.S. Census data was used to benchmark general earnings for cohorts with varied educational backgrounds.

## College Rankings
Various sources were used and cleaned to meet a standard format for college names.


# Methodology
College scorecard data was restructured for analysis along two large categories: (1) earnings, and (2) working rate (active employment). Earnings were further broken down by average and quartiles.

Census data was taken for each cohort to determine earnings of random individuals with different educational backgrounds. An average was taken for each discipline, then a weighted average calculated for each college and cohort to calculate an expected degree value based on a given breakdown of educational types. This was then deducted from the college cohort's actual earnings to create a premium associated specifically to a degree from the college independent of degree type. In the cases of quartiles, stratified sampling was used to simulate a relevant distribution, from which expected value quartiles could be estimated to determine quartile premiums.
