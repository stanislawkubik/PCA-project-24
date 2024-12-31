# Modelling the UST Yield curve using Principal Component Analysis (PCA)
This project illustrates how PCA can be used to better understand the underlying factors driving the changes in US Treasury yields movements. I run the PCA the entire dataset between July 2001 and December 2024, and also on multiple parts intervals within the dataset to explore how different monetary policy regimes affect the principal components explaining the changes of the yield curve. 

The time intervals that are subject to analysis of this projects are as such:

July 2001 - GFC (8th August 2007; I've chosen the last date before the interest markets started to behave disorderly in anticipation of further problems)

December 2008 - November 2015 | Post-GFC ZIRP era

December 2015 - February 2020 | Fed's monetary policy cycle interrupted by Covid pandemic

March 2020 - February 2022 | Covid ZIRP era

March 2022 - December 2024 | Current monetary policy cycle

I further focus on a principal factor affecting the curve's slope, modelled on the timeframe after March 2022. The theoretical reasoning behind such a timeframe is the FED's monetary policy cycle which arguably affects not only the short rate but also the market's reaction across the entire curve.


# Data
US Treasuries constant maturity yields data is provided by FRED's website.



