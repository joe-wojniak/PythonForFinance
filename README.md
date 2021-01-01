# Python For Finance
A repo of examples inspired by the book *Python for Finance* (Py4Fi)

Book: *[Python for Finance](https://www.amazon.com/Python-Finance-Mastering-Data-Driven/dp/1492024333/ref=sr_1_3?crid=Q54A45DY5MHP&dchild=1&keywords=python+for+finance+by+yves+hilpisch&qid=1604860574&sprefix=python+for+finance+yves%2Caps%2C196&sr=8-3), 2nd ed, Hilpisch, Yves*

For a comprehensive online training program covering Python for algorithmic trading see http://certificate.tpq.io.

![OHLC_EUR-USDwBB](https://github.com/joe-wojniak/PythonForFinance/blob/main/Data%20Visualization/PFF_Ch7_Fig_7-27_OHLC_EUR-USDwBB.PNG)

## Why does this repo exist?

I started reading Python for Finance after being introduced to it through an online class on [Udacity](https://www.udacity.com/), Machine Learning for Trading.
I was unable to locate the dataset used in the book that demonstrates the code samples, so I began searching for available sources of similar data.
This repository is a result of that search.

## Update: 2020-Nov-15

Yves has a companion repository for the book here:  [py4fi](https://github.com/yhilpisch/py4fi)

Working the example code has been a great learning experience for me, which wouldn't have been possible without the book. -jw

## How do I use this repo?

1. Download the source code (*.ipynb)
2. Download the data from [Stooq](https://stooq.com/db/h/)

*The source code requires the following folder structure:*

| Path | Comments |
| --------- | -------- |
| ./ | Run Jupyter Lab or Python from this level in the folder structure |
| ./data/daily/us/ | Data files are located under this branch |
| ./data/daily/world/ | More data files |

## OR
3. use data.csv from this repository

## File Folder Structure
Each topic has a Jupyter Lab notebook (*.ipynb) under a topic folder.  The markdown (*.md) files provide a summary of each topic.  Each topic builds upon the previous topic, so it is helpful to skim Data Visualization before covering Financial Time Series; skim Financial Time Series before Trading Strategies, etc.

### Topics:
* Data Visualization (Chapter 7, Py4Fi)
* Financial Time Series (Chapter 8, Py4Fi)
* Trading Strategies (Chapter 15, Py4Fi)

### Markdown Summaries
* 07-0 Data Visualization.md
* 08-1 Time Series Line Plots.md
* 08-2 08-3 Bar Plot and Cum Log Returns.md
* 08-4 Resampling.md
* 08-5 08-6 08-7 Rolling Statistics.md
* 15-0 Trading Strategies (Coinbase Pro Sandbox / Cryptocurrency Demo)

*.ipynb files will need to be modified to load the data.csv file instead of utilizing the folder structure from the stooq.com zip file

+dataLoader.ipynb will load the Stooq raw data files from the stooq.com unzipped folder structure and format them into the data.csv file

## Please Star This Repo!
*It will heLp others to find it*

## Disclaimer
This information is provided for educational purposes and does not constitute financial or trading advice.
The information is provided without warranty, expressed or implied.  
This work is provided under the Apache 2.0 license included in this repository (the "License".)
