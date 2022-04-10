# Challenge-3

## Crypto Arbitrage

I am an analyst at a high-tech investment firm. In this Challenge, I will demonstrate how to capitalize on simultaneous price dislocations in the crypto markets by using the powers of Pandas. 

In this Challenge, I'll sort through historical trade data for Bitcoin on two exchanges: Bitstamp and Coinbase. I will apply three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin.


1. Collect the data.

2. Prepare the data.

3. Analyze the data. 

---

## Technologies

This project leverages Pandas on Jupyter notebook

---

## Open Guide

Before running the application first open Jupyter lab in terminal:

```
  1. Activate dev environment by: "conda activate dev"
  2. Open Jupyter Notebook by: "Jupyter lab"
```
![<terminal>](<Images/Terminal.png>)

---

## Usage

To use the analysis simply clone the repository and run the **crypto_arbitrage.ipynb** within the Jupyter Notebook.\
*Import the following libraries and dependencies:*

``` python
Import pandas as pd
from pathlib import Path
%matplotlib inline 
```

---

## 1. Collect the Data 

1. Import both data from csv file.
2. Use *.head* function to confirm that Pandas properly imported the data. 
![<collect the data>](<Images/Collect the Data.png>)

---

## 2. Prepare the Data 

1. Replace or drop all NaN in DataFrame by using *.dropna* function. 
2. Use *str.replace* function to remove all the dollar signs from the values in the **Close** column.
3. Convert data type of the **Close** column to *float*. 

![<prepare the data>](<Images/Prepare the Data.png>)

---

## 3. Analyze the Data
1. Use *loc* and *iloc* functions to select **'Timestamp'** and **'Close'** for both Bitstamp and Coinbase DataFrames. 
2. Generate the summary statistics for each DataFrame by using *.describe* function. 
3. Create a line plot for the full period of time in the dataset using *.plot* function and remember to include *figsize*, *title* on the plot. 
4. Overlay the visualizations to see the trends of both data. 
5. Select three dates to evaluate for arbitrage profitablity. 
    >Early date - Jan 16\
    Middle Date - Feb 24\
    Late Date - Mar 26
6. Use *describe* function to generate summary of each date and plot *box* graph to read the spread.
7. To calculate the arbitrage spread of each date by using the formula: **Arbitrage Spread = Coinbase closing price - Bitstamp closing price** 
    >*Bitstamp is lower purchase price*
8. Use conditional statement to generate the summary statistics for each arbitrage spread DataFrame, where *arbitrage spread > 0*.
9. To calculate the spread retun by using the formula: **Spread return = arbitrage spread/Bitstamp**.
10. Narrow down the trading opportunities to determine the profit which is *spread returns > 1%*.
11. To calculate the profit for each dates, use the formula: **Profit = profitable trades * Bitstamp**. 
12. Use *dropna* function to drop any missing values.
13. *describe* and *plot* functions will generate summary and graph of profits of each date.
14. Use *cumsum* function to determine cumulative sum of each date. 

![<analyze the data>](<Images/Analyze the Data.png>)
    

---

## Contributors

Feier Ou 

ffeierou1003@gmail.com 

---

## License

Feier Ou 
