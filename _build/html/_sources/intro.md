# CrUX History API

The CrUX History API gives low-latency access to six months of historical real-user experience data at page and origin granularity.

## Metrics

Metrics are expressed in a histogram array, which represents the percent of users that experienced a metric with that value proportionally to all.

A simple three bin histogram for an example metric looks like this:

```
 {
    "histogramTimeseries": [
        {
            "start": 0,
            "end": 2500,
            "densities": [0.9190, 0.9203, 0.9194, 0.9195, 0.9183, 0.9187]
        },
        {
            "start": 2500,
            "end": 4000,
            "densities": [0.0521, 0.0513, 0.0518, 0.0518, 0.0526, 0.0527]
        },
        {
            "start": 4000,
            "densities": [0.0288, 0.0282, 0.0286, 0.0285, 0.0290, 0.0285]
        }
    ],
 }
```

The data points are presented in the order of the collection period dates also returned by the API, with the first point being the earliest period, and the final point being the most recent collection period.

This data indicates that 91.90% of users experience the example metric value between 0ms and 2,500ms for the first collection period in the history, followed by 92.03%, 91.94%, and so on. The units of the metric are not contained in this histogram, in this case we will assume milliseconds.

Additionally, 5.21% of users experience the example metric value between 2,500ms and 4,000ms in the first collection period in the history, and 2.88% of users experience a value greater than 4,000ms in the first collection period in the history.

This Jupyter book features CrUX historical data for `https://www.showmax.com/join/eng/welcome/za`

```{tableofcontents}
```
