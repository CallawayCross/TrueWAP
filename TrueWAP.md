# DESCRIPTION

```
Package: TrueWAP
Type: Package
Title: True Range-Weighted Average Price (TrueWAP)
Version: 0.1.0
Author: Joshua Callaway
Maintainer: Joshua Callaway <Callaway@roar-analytics.com>
Description: This groundbreaking technical indicator directly integrates volatility into price averaging by weighting median range-bound prices using the True Range.  Unlike conventional metrics such as TWAP, which focuses solely on time, or VWAP, which emphasizes volume, TrueWAP captures fluctuating market behavior by reflecting true price movement within high/low performance boundaries.
License: GPL (>=2)
URL: https://github.com/CallawayCross/TrueWAP
BugReports: https://github.com/CallawayCross/TrueWAP/issues
Depends: R (>= 4.3.2)
Imports: dplyr (>= 1.1.4), stringr (>= 1.5.1), zoo (>= 1.8-14), TTR (>= 0.24.4), quantmod (>= 0.4.27)
Encoding: UTF-8
LazyData: true
RoxygenNote: 7.3.2
Suggests: 
    knitr,
    rmarkdown,
    testthat (>= 3.0.0)
VignetteBuilder: knitr
Config/testthat/edition: 3
```

# `anchoredTrueWAP`: Title anchoredTrueWAP

## Description

Calculates Anchored True Range-Weighted Average Price (TrueWAP)

## Usage

```r
anchoredTrueWAP(high, low, close, true_range, period)
```

## Arguments

* `period`: Vector of bars since start of fixed period
* `mid_val`: Vector of Mid values
* `range_val`: Vector of Range values

## Value

Vector of Anchored TrueWAP values

## Examples

```r
data(nikkei)
anchoredTrueWAP(
high = nikkei$High
, low = nikkei$Low
, close = nikkei$Close
, true_range = nikkei$tr
, period = nikkei$bars_since_segment
)
```

# `anchoredTWAP`: Title anchoredTWAP

## Description

Calculates Anchored Time-Weighted Average Price (TWAP)

## Usage

```r
anchoredTWAP(OHLC, period)
```

## Arguments

* `OHLC`: Data frame object with Open, High, Low, & Close fields
* `period`: Vector of bars since start of fixed period

## Value

Vector of Anchored TWAP values

## Examples

```r
data(nikkei)
anchoredTWAP(
OHLC = nikkei$OHLC
, period = nikkei$bars_since_segment
)
```

# `anchoredVWAP`: Title anchoredVWAP

## Description

Calculates Anchored Volume-Weighted Average Price (VWAP)

## Usage

```r
anchoredVWAP(HLC3, volume, period)
```

## Arguments

* `HLC3`: Vector of High, Low, Close Average Values
* `volume`: Vector of Volume values
* `period`: Vector of bars since start of fixed period

## Value

Vector of Anchored VWAP values

## Examples

```r
data(nikkei)
anchoredVWAP(
HLC3 = nikkei$HLC3
, volume = nikkei$Volume
, period = nikkei$bars_since_segment
)
```

# `TrueWAP`: Title TrueWAP

## Description

Calculates True Range-Weighted Average Price (TrueWAP)

## Usage

```r
TrueWAP(high, low, close, true_range, period)
```

## Arguments

* `true_range`: Vector of True Range Values
* `period`: Rolling window length
* `true_mid`: Vector of True Mid Values

## Value

Vector of TrueWAP values

## Examples

```r
data(nikkei)
TrueWAP(
high = nikkei$High
, low = nikkei$Low
, close = nikkei$Close
, true_range = nikkei$tr
, period = 50)
```

# `TWAP`: Title TWAP

## Description

Calculates Time-Weighted Average Price (TWAP)

## Usage

```r
TWAP(OHLC, period)
```

## Arguments

* `OHLC`: Data frame object with Open, High, Low, & Close fields
* `period`: Rolling window length

## Value

Vector of TWAP values

## Examples

```r
data(nikkei)
TWAP(nikkei$OHLC, 50)
```

# `VWAP`: Title VWAP

## Description

Calculates Volume-Weighted Average Price (VWAP)

## Usage

```r
VWAP(HLC3, volume, period)
```

## Arguments

* `HLC3`: Vector of High, Low, Close Average Values
* `volume`: Vector of Volume values
* `period`: Rolling window length

## Value

Vector of VWAP values

## Examples

```r
data(nikkei)
VWAP(nikkei$HLC3, nikkei$Volume, 50)
```

