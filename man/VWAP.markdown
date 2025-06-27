```{=tex}
\name{VWAP}
\alias{VWAP}
\title{Title VWAP}
\usage{
VWAP(HLC3, volume, period)
}
\arguments{
\item{HLC3}{Vector of High, Low, Close Average Values}

\item{volume}{Vector of Volume values}

\item{period}{Rolling window length}
}
\value{
Vector of VWAP values
}
\description{
Calculates Volume-Weighted Average Price (VWAP)
}
\examples{
data(nikkei)
VWAP(nikkei$HLC3, nikkei$Volume, 50)
}
```
