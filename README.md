# Determining Optimal Stock Indicators

### ** Please note that this is NOT a completed project, but a work in process  **

The goal of this project to determine some behaviour of trading based on the stock indicator. This project is specificially for my own personal stock interest. 
The stock indicator monitors three key indicators that I generally follow. 
These indicators include : 
* RSI
* MFI 
* Boiler's Bands 
* Combination of all three 


### Objectives 
The objective of this project is broken into three parts : 
#### 1) Visualize the trades for each stock within my portfolio based on trading with indicators (completed)



#### 2) Create Monte Carlos simulations of varying stocks for trading using each indicator. 
 * Random number of stocks will be traded using each indicator 
 * The key is to determine the average and standard deviation of return/loss for small,medium and large cap stock (In process)

 The simulated enviornment (repeated by randomling sampling different stocks) : 
 * The simulation will follow a 5, 10 and 15 year interval 
 * On january 1 of each year the portfolio will gain 10K to invest into the single stock 
 * Each time a buy signal is triggered, 2K worth of stocks will be bought, unless there is no more money. 
 * Each time a sell signal is triggered, 2K worth of that stock will be sold, unless there is no more stock.
 * Note that more monte carlos simulation could also be performed to determine the optimal % of portfolio that should be bought or sold each time 
 * The year over year growth/loss of the portfolio's asset (stock+cash) of that stock is reported 
 
#### 3) Using OpenAI gym to create an agent based reinforcement learning (Not started)
* The simulation enviornment will be similar of the #2 
* The agent result will be bench marked against the statistical methods 


### 1 Visualization of trading using specific stock indicators on my portfolio 
The figure below is the sample visualization of TELUS traded using these stock indicators. 
From this figure:
* Boiler's bands[BBand] triggers the most number of buy and sell signal, fixing on every single local minimum and local maximum. This process is a little aggressive considering that every trade costs $5, and is more suitable for short term trader using brokage-fee free platforms like Robinhood. 
* RSI triggers less amount of buy and sell signals compared to BBands. However, when stocks are on the hype train (aggressively retail buyers that introduces a sharp increase in the stock price), the sell signal will be triggered throughout this entire timeline. This can lead to early trigger of stock sell (before the maximal price). 
* MFI triggers the least amount of 
* Combining all three triggers significantly reduces the number of triggers 
The observed trends were also cohesive for other companies ( see notebook). 


![image](https://user-images.githubusercontent.com/29676594/115354572-c7d1bb80-a187-11eb-9e3a-0a1dcc0893f5.png)






