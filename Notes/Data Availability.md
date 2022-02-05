A lot of data is needed for the training of ML applications
- as much as possible but as little as necessary

Bitcoin
- data is freely available
- data for prices but also fundamental blockchain metrics are available
- But is it enough?
  - daily data for 10 years -> 3650 data points
  - hourly data for 10 years -> 24 x 365 x 10 = 87,600 data points
    - is there hourly data for variables except price?
- Is it possible to use daily with hourly data in the same training data frame?
  - by assigning each hourly value the value of the day
  -  what are the implications for the models?
  -  -> multicollinearity? 

Stock market data
- Use Yahoo Finance as data source
- longer time horizon -> more data available
- e.g. SPY since 1993 -> roughly 7k data points with daily frequency
- strictly: still not enough data

Weather data
- https://github.com/earthobservations/wetterdienst
- enough data for machine learning
  - Historical (last ~300 years), recent (500 days to yesterday), now (yesterday up to last hour)
  - Every minute to yearly resolution
  - Time series of stations in Germany
- also in time series format



-> Build a ML Cockpit that is not specific to one use case?
- Cockpit takes data as input and gives prediction as output
- what about use case specific data preprocessing? Data transformations?
  - -> provide the necessary tools for data preprocessing
  - user can then select what to do exactly
-> Need to decide whether to tackle one specific use case or build a generalized tool
  - e.g. backtesting and monitoring takes significant amount of time








