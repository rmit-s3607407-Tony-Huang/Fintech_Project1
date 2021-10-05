# Multi Asset Classs Market Analysis
## Monash University FinTech Bootcamp Project 1
Project Manager: Tony Huang

Senior Developer: Viseth Auk

Data Visualization Specialist: Ashley Neville

Data Consultant: Anh Thi Dang

---
## Summary
Our team has a combined capital of $50,000 and wishes to venture together and invest in a trading strategy across 3 asset classes: stocks, crypto and gold.

We have found in many finance literatures that the crossover moving average is a popular strategy people use and wish to explore this trading strategy as a possible technique to use to invest our funds.

---

## Major Findings

---
## Installation
### Creating a new anaconda environment
```shell
conda update anaconda
conda create -n backtrade_env python=3.7 anaconda -y
conda activate backtrade_env
conda install -c anaconda nb_conda -y
conda install -c conda-forge nodejs=12 -y
conda install -c pyviz holoviz -y
conda install -c plotly plotly -y
conda install -c conda-forge jupyterlab=2.2 -y
```
### To install PyViz, the for Jupyter Lab
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
### To install the the python dependencies
```shell
pip3 install -r requirements.txt
```
### Opening Jupyter Lab
```shell
jupyter lab
```
---
**Multi Asset Class Market Analysis**

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
Anh - dashboards, pulling api data
