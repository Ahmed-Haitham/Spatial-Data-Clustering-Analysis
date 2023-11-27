# Spatial-Data-Clustering-Analysis

In this project, we conducted a detailed spatial cluster analysis of respiratory diases in Glasgow for the years 2004 and 2005. Our focus was on identifying patterns, and comparing clustering results using diverse methodologies. Leveraging spatial autocorrelation, Bayesian modeling with CARBayes, bivariate mixture model clustering, and k-means clustering methods are used to provide insights into the spatial distribution of respiratory diseases. .

## Data:

expected_counts.csv: 271 observations with 3 variables (code, E2004, E2005)
respiratory_admissions.csv: 271 observations with 3 variables (IG, Y2004, Y2005)

Shapefiles in the SG_IntermediateZoneBdry_2001 folder with 1235 observations and 6 variables (IZ_CODE, IZ_NAME, STDAREA_HA, Shape_Leng, Shape_Area, geometry)

### Data Preparation:

Merged the datasets using an inner join based on matching variables (code and IG).
Linked shapefiles to data using the merge() function, ensuring preservation of dataset observations.
Calculated Standardized Mortality Ratios (SMR) for both 2004 and 2005.

### Exploratory Data Analysis (EDA):

Analyzed SMR distributions, detecting right-skewed patterns.
Identified outliers through box plots, indicating potential variability in specific areas.
Explored the positive linear relationship between SMR in 2004 and 2005 through scatter plots and correlation coefficients.

## Spatial Analysis:

Created spatial objects and observed geometry using shapefiles.
Mapped SMR values for 2004 and 2005 separately, identifying areas with higher or lower occurrences of respiratory diseases.

### Spatial Autocorrelation:

Checked for spatial autocorrelation using Moran's I statistic for both years.
Detected positive spatial autocorrelation, indicating clusters of similar SMR values in neighboring regions.

### Spatial Modeling with CARBayes:

Fitted spatial correlation models for 2004 and 2005 using Poisson regression with Leroux CAR spatial correlation.
Assessed model convergence and goodness of fit.
Mapped risks and Posterior Exceedance Probabilities (PEP) for both years.

### Bivariate Mixture Model Clustering:

Extracted mean fitted values from the spatial models.
Ran a bivariate mixture model clustering method and visualized the results.
Explored different covariance structures and cluster numbers, selecting the best-performing model.

### Comparison with k-means:

Applied k-means clustering on mean fitted values.
Explored multiple cluster numbers to find optimal solutions.
Compared the results with the bivariate mixture model clustering.

## Conclusion:
The project provided a thorough exploration of spatial patterns in respiratory diase in Glasgow, leveraging various analyses and clustering algorithms. The comparison between different clustering methods adds depth to our understanding of the underlying patterns in the data. Further investigation and interpretation of clusters can guide targeted interventions and public health strategies.
