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









