```{=tex}
\name{anchoredTrueWAP}
\alias{anchoredTrueWAP}
\title{Title anchoredTrueWAP}
\usage{
anchoredTrueWAP(high, low, close, true_range, period)
}
\arguments{
\item{period}{Vector of bars since start of fixed period}

\item{mid_val}{Vector of Mid values}

\item{range_val}{Vector of Range values}
}
\value{
Vector of Anchored TrueWAP values
}
\description{
Calculates Anchored True Range-Weighted Average Price (TrueWAP)
}
\examples{
data(nikkei)
anchoredTrueWAP(
high = nikkei$High
, low = nikkei$Low
, close = nikkei$Close
, true_range = nikkei$tr
, period = nikkei$bars_since_segment
)
}
```
