# MADRL

## Problem Statement
- From a real-world perspective, the most fluid data with multiple known variables while being able to be quantized is data from the Stock Market. Stock Market Agents use a variety of patterns and techniques to summarize available data, make predictions and increase their portfolio value. Irrespective of how the data is gathered or summarized, humans cannot process such vast amounts of data and make precise predictions to change with the market flow. Often inaccuracies tend to pop up during the collection and processing stage or the summarizing stage. Often, this leads to incorrect estimations and huge
losses in portfolio value. To prevent such issues, agents have been designing programs to make decisions and implement them in split seconds to augment
portfolio value. But these programs do not understand the data. Instead, they are programmed to make decisions on existing trend and hence need heavy
supervision, which is counterproductive.

## Proposed Solution
- To eliminate such issues, we have worked on simulating agents which can make decisions to buy, sell or hold stocks based on OHCL data, which
has been processed to reflect trends in the market. This eliminates the need for constant supervision and can augment our portfolio significantly. Agents have been implemented using PPO and A2C, and multiple trials have been done to determine the most optimal parameters.

## Parameters available
The information available from the stock market is listed as follows:
- Open: Open price of a stock refers to the price it started trading when the opening bell rang. We need to understand that while in most cases, it would be equal to the previous day’s closing value, changes like negative news after trading hours can affect the opening price next day.
- High: High refers to the highest value that a stock has been traded in the given period of time.
- Low: Low refers to the lowest value a stock has been traded in the given period of time.
- Close: A stock’s performance can be determined by its closing price of the day. The closing price of a stock is determined by the traders on the basis of all the actions performed during the day. Hence this serves as a yardstick of the stock’s progress during the day and can be an indication of the progress made by the stock.
- Adjusted Close: As the entities listed on the stock market are entities which make decisions that can affect progress of the company, or decisions by shareholders which might lead to influx of additional stock into the market, these will have a significant effect on the direction and price of the stocks. Some companies issue dividends to the shareholders, which on the long run tends to devalue stock price, as this money can be used for further expansion instead of paying out now. All such factors are accounted for in calculating the Adjusted Close value of a stock. These factors, in addition to Volume, make the candlestick graph, which is the choice of graph for traders to understand values and estimate patterns to make decisions to buy, sell or hold the
stocks.

### Using the information available, we are calculating the below indicators which signify the trend of the stocks and are widely recognized as acceptable parameters:
- MACD
- RSI
- CCI
- ADX

## Algorithms used:
- PPO
- A2C

## Result:
- We initiated our agent with an opening balance of 2000 and analyzing most recent stocks of Dogecoin, our agent was able to gather a mean value of 3042.2952026182747 for PPO and 3037.5357370164065 for A2C.
