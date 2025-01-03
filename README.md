# Modelling the UST Yield curve using Principal Component Analysis (PCA)
This project illustrates how PCA can be used to better understand the underlying factors driving the changes in US Treasury yields movements. I run the PCA the entire dataset between July 2001 and December 2024, and also on multiple parts intervals within the dataset to explore how different monetary policy regimes affect the principal components explaining the changes of the yield curve. 

This project is my first take on using PCA to analyse fixed-income markets, the objective is mostly educational, although in the future I aim to extend it to the analysis of the other markets, as well as incorporate modelling some of the identified principal components using mean-reversion models.

The time intervals that are subject to analysis of this project are as such:

July 2001 - GFC (8th August 2007; I've chosen the last date before the interest markets started to behave disorderly as a consequence of the GFC)

December 2008 - November 2015 | Post-GFC ZIRP era

December 2015 - February 2020 | Fed's monetary policy cycle interrupted by Covid pandemic

March 2020 - February 2022 | Covid ZIRP era

March 2022 - December 2024 | Current monetary policy cycle

# Data
US Treasuries constant maturity yields daily data, as well as data used for correlation analysis is provided by FRED's website.
<img width="819" alt="Screenshot 2025-01-03 at 17 16 03" src="https://github.com/user-attachments/assets/934db4c8-1e22-4a2f-9951-39ddbc01c693" />

# Findings
Overall, we find that the principal components that drive the US Yield curve change over time, and whereas they usually represent similar behaviours of the curve (shift, slope and curvature), their magnitude and the effect on different maturities differs in different market regimes.

We further find that in the ZIRP regimes, the first PC explained significantly less variance of the yield curve than in other monetary policy regimes. This makes sense on a very intuitive level, as in the regimes with little variance across all the maturities (i.e. a shift of the entire curve occurring rarely), different types of movements will naturally be responsible for more variance

# Comparison of the PCA results of two chosen market regimes

# 2020-2022 ZIRP
<img width="518" alt="Screenshot 2025-01-03 at 17 20 10" src="https://github.com/user-attachments/assets/466be6d5-c4ca-4e47-beb4-d9a9d8e75ec1" />
<img width="589" alt="Screenshot 2025-01-03 at 17 20 35" src="https://github.com/user-attachments/assets/d9c1498b-b0ee-47c4-aa0f-12082e7bf1cb" />
<img width="587" alt="Screenshot 2025-01-03 at 17 21 08" src="https://github.com/user-attachments/assets/a9212653-2707-4404-aecf-61f9bc0c0613" />

# 2022 - 2024 Monetary Policy Cycle
As mentioned previously, in market regimes other than ZIRP first three principal components are enough to explain virtually all (>99%) of the variance. 

<img width="524" alt="Screenshot 2025-01-03 at 17 25 46" src="https://github.com/user-attachments/assets/8b21abf8-65eb-463d-974c-e46b58ef848c" />
<img width="589" alt="Screenshot 2025-01-03 at 17 26 06" src="https://github.com/user-attachments/assets/0125ba25-8072-48af-88d7-1932ad601c2a" />
<img width="586" alt="Screenshot 2025-01-03 at 17 26 19" src="https://github.com/user-attachments/assets/49a2ada6-7bc5-4342-9ccc-1a0bf0eac914" />

# Further research
An interesting idea for further research is to try to model PC2 (slope) in the current monetary policy cycle as a mean-reversion process.
<img width="755" alt="Screenshot 2025-01-03 at 16 57 36" src="https://github.com/user-attachments/assets/2f7016db-0d77-4cf4-a283-0ff10a97e7a7" /> 

Whereas this factor seems to exhibit some mean-reverting property, it is rather non-linear, and modelling it as such would require particular care for the numerical stability of the result. Further, the model could require using some functional form of the diffusion coefficient of the model, but this would again require particular care about the coefficient estimation process, to ensure stable results.
<img width="676" alt="Screenshot 2025-01-03 at 16 58 40" src="https://github.com/user-attachments/assets/d76f40b7-440a-4367-be02-0c768779c97c" />

# Limitations
One of the limitations this project has is the lack of availability of high-quality data in smaller timeframes available for free. The access to such data could potentially support the mean-reversion modelling of the PC2 mentioned in the last part. Clearly, a small sample size may be problematic here and increasing it could give some degree of confidence about the stability of estimated coefficients. Yet, if we are interested in the behavior of the PC2 in the current market regime, our only option to increase the sample size is to try to run the analysis on a smaller time interval.



