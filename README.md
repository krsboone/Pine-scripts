# Pine-scripts


## Details

A collection of some of the pine scripts I built and use in Trading View

Over tiem I'll add more that I'm comfortable sharing

**Historical-trends**

`projection-line-offset.pine`: Set a look back range, and offset. The script will plot 3 points based on average opening, range, and closed prices from 5 range candles, then draw a line to reflect the trend and yield over the look back range. 
For a lookback time of 100:
1. The first plot point will be the average opening price for the first 5 candles (candles 96 - 100)
2. The second plot point will be the average closing price for the last 5 candles (candles 1 - 5)
3. The third plot point will be the average of the high and low for the middle 5 candles (candles 48 - 52)
