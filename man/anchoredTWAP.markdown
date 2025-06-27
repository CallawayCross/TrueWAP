```{=tex}
\name{anchoredTWAP}
\alias{anchoredTWAP}
\title{Title anchoredTWAP}
\usage{
anchoredTWAP(OHLC, period)
}
\arguments{
\item{OHLC}{Data frame object with Open, High, Low, & Close fields}

\item{period}{Vector of bars since start of fixed period}
}
\value{
Vector of Anchored TWAP values
}
\description{
Calculates Anchored Time-Weighted Average Price (TWAP)
}
\examples{
data(nikkei)
anchoredTWAP(
OHLC = nikkei$OHLC
, period = nikkei$bars_since_segment
)
}
```
