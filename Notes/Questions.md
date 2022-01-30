Modeling prices or returns?

- Stationarity: A stationary time series is one whose properties (e.g. mean and variance) do not depend on the time at which the series is observed
  - more technically: a stochastic process whose unconditional joint probability distribution does not change when shifted in time.
  - working with time series usually involves stationary data (comparable to iid in cross sectional data)
- Time series of prices are non-stationary (long term growth)
  - Prices have a memory, value depends on a series of historical values
  - Presence of memory makes time series non-stationary: History of previous levels that shift time series' mean over time
- Returns (or changes/differences -> returns are just scaled differences) are stationary and have no memory 
  - memory cut-off for each specific return calculation
  - data transformations needed to make time series stationary
  - typical workflow in statistics: achieve stationarity (by differencing) then extract residual signals that remain.
    - statistical causal inference relies on invariant processes -> regression of non-stationary data by using (first) differences
    - common trick for an alternative to differencing: test for cointegration to make regression work for non-stationary time series
- But: Memory might be good for predictive power of model?
  - maybe some useful information in it?
    - e.g. returns could use information that prices have drifted away from their long-term expected value (e.g. mean reversal, fair / fundamental value)
- Dilemma / trade-off: returns are stationary but without memory, prices have memory but are non-stationary
  - time series can always be made more stationary through differencing but at expense of foregoing memory
- Question: Minimum differencing to make price series stationary while preserving maximum possible memory?
  - returns are stationary but have some memory left -> some kind of price transformation
- Supervised learning typically requires stationary features
  - reason: map unlabeled data points to a collection of labeled observations and infer label of that new data point
  - if features are not stationary, the mapping does not work reliably for large sample number
  - however, stationarity is necessary but does not guarantee high performance of ML
- Solution: Cointegration or
  - explore fractional differencing of time series -> De Prado
  - in literature, typically first differences (adjacent data points) is used -> but why would this be optimal?
    - n-step differencing is arbitrary


Sources:
- https://stats.stackexchange.com/questions/19715/why-does-a-time-series-have-to-be-stationary
- https://stats.stackexchange.com/questions/497877/forecasting-prices-vs-returns-by-deep-learning
- https://quant.stackexchange.com/questions/489/correlation-between-prices-or-returns
- https://quant.stackexchange.com/questions/16481/why-do-we-usually-model-returns-and-not-prices
- https://www.youtube.com/watch?v=vvTKjm94Ars and https://www.youtube.com/watch?v=q5wbOSjbVW4

