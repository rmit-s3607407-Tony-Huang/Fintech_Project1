# Multi Asset Classs Market Analysis
## Monash University FinTech Bootcamp Project 1
Project Manager: Tony Huang

Senior Developer: Viseth Auk

Data Visualization Specialist: Ashley Neville

Data Consultant: Anh Thi Dang

---
## Summary
Our team has a combined capital of $60,000 and wishes to venture together and invest in a trading strategy across 3 asset classes: stocks, crypto and gold.

We have found in many finance literatures that the crossover moving average is a popular strategy people use and wish to explore this trading strategy as a possible technique to use to invest our funds.

Based on our research, results suggest that a buy and hold approach is more superior, and we should allocate most of our investments to buy and hold rather than applying the popular  moving average strategy

The Bitcoin data used for analysis and comparison included  a period where the market was in a booming trend for a new and highly innovative financial asset. This trend may not continue in the future.

The performance on bitcoin buy & hold strategy could have shown as even more favourable had we been able to obtain data a bit earlier. The earliest data we could get was in Sept 2017.

The result on the market analysis on the moving average strategy is a bit bias as the strategy was constructed on a very long time frame ( daily data )

---

## Major Findings
1. Was there any relationship between these assets?

Plotting the correlation of the three assets, little to no correlation is found.


2. How should we best allocate the capital across these asset classes to minimize risk?

Since there is little to no correlation, we decided to equally divide the funds into the three assets to hedge against large price movements of one asset.

![](/images/asset_correlation.PNG)

3. Which asset were inherently more risky?

The boxplot of daily returns shows that the mean and standard deviation of bitcoin is the largest, and hence the most risky.

![](/images/daily_return_boxplot.PNG)

4. Which asset will this strategy work best for?

The moving average strategy yields profits across all three assets, but little optimization was done to get better performance.

5. Could a buy and hold strategy have performed better?

The buy and hold strategy outperforms the moving average strategy in all three assets.

![](/images/pnl.PNG)

6. On what basis do we decide that this strategy is better for a 
particular asset compared to the others?

Using sharpe’s ratio, to normalize the profit against risk, the strategy can be compared across each asset.

![](/images/sharpe_ratio.PNG)

---
## Installation
### 1. Creating a new anaconda environment
```shell
conda update anaconda
conda create -n backtrader_env python=3.7 anaconda -y
conda activate backtrader_env
conda install -c anaconda nb_conda -y
conda install -c pyviz holoviz -y
conda install -c plotly plotly -y
conda install -c conda-forge jupyterlab=2.2 -y
conda install -c conda-forge nodejs=12 -y
```
### 2. Install PyViz dependencies for Jupyter Lab
```shell
# (OS X/Linux)
export NODE_OPTIONS=--max-old-space-size=4096

# (Windows)
set NODE_OPTIONS=--max-old-space-size=4096

jupyter labextension install @jupyter-widgets/jupyterlab-manager --no-build
jupyter labextension install jupyterlab-plotly --no-build
jupyter labextension install plotlywidget --no-build
jupyter labextension install @pyviz/jupyterlab_pyviz --no-build
jupyter lab build

# Unset NODE_OPTIONS environment variable
# (OS X/Linux)
unset NODE_OPTIONS

# (Windows)
set NODE_OPTIONS=
```
### 3. Install python dependencies
```shell
pip3 install -r requirements.txt
```
### 4. Running inside Jupyter Lab
```shell
jupyter lab
```

### 5. Launching a bokeh dashboard on localhost
```shell
panel serve visualizations.ipynb
```

---

<!-- **Multi Asset Class Market Analysis**

**Team Members
Anh Thi Dang
Tony Huang
Viseth Auk
Ashley Neville

**Project Description 
The purpose of this project is to analyse three different asset classes and apply the same trading strategy across the asset classes to determine

**Research question to answer
Divise a trading algorithm and see how it performs across three different asset classes (Stocks, Crypto, Gold)


**Datasets to be Used
Data sets from the last 5 years to be used for;
Stocks - S&P 500
Crypto - Bitcoin/USDT
Gold

In addition we will apply out of sample testing to ensure performance of strategy is consistent with in sample testing. 


**breakdown of tasks
Tony - project manager, initial backtrader implementation 
Ash - visualization, pulling api data
Viseth - documentation, code reviewing 
Anh - dashboards, pulling api data -->
