# Estimating American Commute Times

## Abstract 

Using data from the US Census Bureau, specficially the 2019 American Community Survey, I will analyze the data and attempt to build a model to predict commute times given other demographic variables. I split commute times into 6 even buckets and used the Keras API and Keras preprocessing layers. For the features, I selected Age, household income, Rent as a percent of income, bedrooms, gas cost and property value as numeric values. I selected multigenerational household, race, sex, units in housing structure, and lot size as categorical values. The best result of the model used two 128 unit Keras dense layers and was able to accurately place the results in the correct bucket (with 6 total buckets) 25% of the time. Models that overfit were able to correctly place the training data up to 40% of the time, but it hurt validation accuracy. The linear correlations between this data are extremely low, with no feature having a correlation above .1, so there appears to be a limit in how accurate these models can be. With more features and processing power this accuracy may be able to be overcome. The lack of correlation is an interesting observation in itself, as it appears that transport time is relatively weakly connected to almost all demographic variables, and is quite similar across the board. 



## [Presentation](https://docs.google.com/presentation/d/1D3daSWO6kgrrGgWWUD-U__ZssHlr0__o_0J6_QRzM6c/edit?usp=sharing)

## [Video](https://youtu.be/r5LYVGgI0rc)

