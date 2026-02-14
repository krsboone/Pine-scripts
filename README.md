# Pine-scripts


## Details

A collection of some of the pine scripts I've built and use in Trading View

Over time I'll add more that I'm comfortable sharing

**historical-trends**

`projection-line-offset.pine`: Set a look back range, and offset. The script will plot 3 points based on average opening, range, and closed prices from 5 range candles, then draw a line to reflect the trend and yield over the look back range. 

For a lookback time of 100:
1. The first plot point will be the average opening price for the first 5 candles (candles 96 - 100)
2. The second plot point will be the average closing price for the last 5 candles (candles 1 - 5)
3. The third plot point will be the average of the high and low for the middle 5 candles (candles 48 - 52)

Configs:
1. Lookback range (how far back to examine)
2. Measure offset (how many candles back to beging lookback)

**candle-analysis**

`candle-enumeration.pine`: Assigns a numerical value to each candle; 1xx for bullish, 2xx for bearish. The higher the value the stronger the move. This is still a LONG work in progress with the broader goal of expanding this for historical pattern detection and fractal plotting.

Basic calculations:
Bullish
Second digit:
((Close price - Lower wick) / close price * 100 * weighting
Third digit:
((Higher wick - Open price) / open price * 100 * weighting

Bearish
Second digit:
((Higher wick - close price) / close price * 100 * weighting
Third digit:
((Open price - Lower wick) / open price * 100 * weighting

Configs:
1. Lookback range (how far back to examine)
2. Measure offset (how many candles back to beging lookback)
3. Weighting (gives returned values more strength. Default = 4, so roughly you can expect a 10% move to yield a 4 or a 20% move to yield an 8)
