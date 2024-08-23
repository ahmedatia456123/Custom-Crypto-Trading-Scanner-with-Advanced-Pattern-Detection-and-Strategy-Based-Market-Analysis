# Custom Crypto Trading Strategy Scanner

**Demo Link:** [Try Demo](https://coincove.blogspot.com/p/static.html)

## Shortcuts
- [Overview](#overview)
- [Skills and Technologies Used](#skills-and-technologies-used)
- [Features](#features)
- [Parameters Explanation](#parameters-explanation)
- [Timeframe Metrics](#timeframe-metrics)
- [Global Metrics](#global-metrics)
- [Scoring System](#scoring-system)
- [Note](#note)
- [Conclusion](#conclusion)
- [Contact](#contact)


## Overview

This report describes a custom trading strategy scanner designed for cryptocurrency trading, with a particular focus on BUSD pairs. The scanner leverages a variety of techniques to identify trading opportunities based on patterns, market phases, and volatility metrics. It is optimized for quick market analysis and can be adapted to various trading strategies.

## Skills and Technologies Used

### Hard Skills
- **JavaScript:** Utilized for developing the trading scanner, leveraging its capabilities for both front-end and back-end functionalities.
- **Parallel Programming:** Applied to handle multiple data streams efficiently.
- **Binance API:** Used for real-time data retrieval and trading operations.

### Soft Skills
- **Analytical Skills:** Applied to discover trading patterns and build a robust strategy.
- **Data Analysis and Visualization:** Enabled the creation of insightful charts and metrics, turning raw data into actionable trading signals.
- **Creativity:** Used to design a versatile and adaptive scanner that meets various trading needs.

## Features

- **Pattern-Based Strategy:** Identifies trading opportunities based on predefined times, including the opening of 4-hour, 1-hour, and 5-minute candles. Trades are executed within less than a minute.
- **Market Conditions:** Focuses on coins in the distribution phase, showing consolidation, and with prices at the bottom half of consolidation.
- **Color-Coded Indicators:** Provides a quick market overview using color-coded indicators for easy identification of trends.
- **FOMO Strategy:** Utilizes market FOMO to highlight opportunities where the majority of traders are likely to open their trades.
- **Volatility Metrics:** Measures market volatility and provides several metrics, including spread sums and anomalies. Uses color coding to indicate potential price increases or decreases based on market spreads.
- **Custom Charts:** Displays how the market behaves in the first three candles of each hour and the first three candles of 30-minute intervals for the past 1000 minutes. Compares coin prices with BTC prices to identify anomalies and potential market movements.

## Parameters Explanation

- **Top All Green:** Shows top coins currently increasing in price, ranging from 0 to the maximum number of coins.
- **Top All Red:** Shows top coins currently decreasing in price, ranging from 0 to the maximum number of coins.
- **Fav Coins:** A predefined list of coins used to show high winning rates with this indicator:
  - `['LEVERUSDT', 'PHBUSDT', 'AMBUSDT', '1000FLOKIUSDT', 'IDEXUSDT', 'KEYUSDT', 'DODOBUSD', 'TLMUSDT']`
- **Cards:** Displays coins showing anomalies and high volatility.
- **Sum All Spread:** Sorts coins based on the total sum of all spreads.
- **Sum All Amp:** Sorts coins based on the total sum of all amplitudes.
- **Red and Green:** Sorts coins based on the number of green or red candles.
- **Score:** A scoring system indicating the suitability of coins for scalping traders. Higher scores suggest higher profitability, but accuracy may vary and requires experienced traders.

### Timeframe Metrics
- **1-Hour Time Frame:**
  - **SpreadSum:** Absolute sum of all spreads in the 1-hour timeframe.
  - **AmpSum:** Absolute sum of all amplitudes in the 1-hour timeframe.
  - **Green Score:** Number of green candles in the 1-hour timeframe.
  - **Red Score:** Number of red candles in the 1-hour timeframe.

- **30-Minute Time Frame:**
  - **SpreadSum:** Absolute sum of all spreads in the 30-minute timeframe.
  - **AmpSum:** Absolute sum of all amplitudes in the 30-minute timeframe.
  - **Green Score:** Number of green candles in the 30-minute timeframe.
  - **Red Score:** Number of red candles in the 30-minute timeframe.

- **5-Minute Time Frame:**
  - **SpreadSum:** Absolute sum of all spreads in the 5-minute timeframe.
  - **AmpSum:** Absolute sum of all amplitudes in the 5-minute timeframe.
  - **Green Score:** Number of green candles in the 5-minute timeframe.
  - **Red Score:** Number of red candles in the 5-minute timeframe.

### Global Metrics
- **Last 20 Minute SpreadSum:** Absolute sum of spreads for the last 20 minutes, showing volatility in this period.
- **Last 300 Minute SpreadSum:** Absolute sum of spreads for the last 300 minutes, showing volatility over a longer period.
- **4-Hour Spread:** Spread of the last 4-hour candle.
- **1-Hour Spread:** Spread of the last 1-hour candle.
- **5-Minute Spread:** Spread of the last 5-minute candle.
- **Top 5-Minute Red:** Sum of red-colored spreads at the opening of 5-minute candles. Higher values indicate stronger downtrends.
- **Top 5-Minute Green:** Sum of green-colored spreads at the opening of 5-minute candles. Higher values indicate stronger uptrends.

## Scoring System

The scoring system is based on the following mathematical formula:

$$
\text{Score} = \text{sumAllSpread} + \frac{|\text{sumAllGreen} - \text{sumAllRed}|}{5} + \text{cardCount} \times 5 + \text{topAllRed} + \text{topAllGreen}
$$

Where:
- `sumAllSpread` is the total sum of all spreads.
- `sumAllGreen` is the sum of all green candle spreads.
- `sumAllRed` is the sum of all red candle spreads.
- `cardCount` is the count of anomalies.
- `topAllRed` is the top red spread value.
- `topAllGreen` is the top green spread value.

Coins with a higher score indicate a higher probability of being profitable for scalping, especially when evaluated by experienced traders.

## Note
Users can sort all coins based on any of the parameters listed above by clicking on the respective parameter headers.

## Conclusion

This custom trading strategy scanner is designed to offer a comprehensive tool for identifying trading opportunities in the crypto market. With its flexible and adaptive approach, it can provide valuable insights and assist traders in making informed decisions.

For any additional information or to try out the demo, visit the provided [demo link](https://coincove.blogspot.com/p/static.html).

## Contact

For further inquiries, please email [ahmedatia456123@gmail.com](mailto:ahmedatia456123@gmail.com).

