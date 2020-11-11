# Python For Finance
A repo of examples inspired by the book *Python for Finance*

Book: *[Python for Finance](https://www.amazon.com/Python-Finance-Mastering-Data-Driven/dp/1492024333/ref=sr_1_3?crid=Q54A45DY5MHP&dchild=1&keywords=python+for+finance+by+yves+hilpisch&qid=1604860574&sprefix=python+for+finance+yves%2Caps%2C196&sr=8-3), 2nd ed, Hilpisch, Yves*


## Why does this repo exist?

I started reading Python for Finance after being introduced to it through an online class on [Udacity](https://www.udacity.com/), Machine Learning for Trading.
I was unable to locate the dataset used in the book that demonstrates the code samples, so I began searching for available sources of similar data.
This repository is a result of that search.

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
3. use data.csv in this repository

*.ipynb files will need to be modified to load the data.csv file instead of utilizing the folder structure from the stooq.com zip file

dataLoader.ipynb will load the raw data files from the stooq.com zip file and format them into the data.csv file

## Please Star This Repo!
*It will heLp others to find it*

## Disclaimer
This information is provided for educational purposes and does not constitute financial or trading advice.
The information is provided without warranty, expressed or implied.  
This work is provided under the Apache 2.0 license included in this repository (the "License".)
