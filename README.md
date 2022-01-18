# Personal AlgoBot
This project was a project done by Daniel Jiang, Jodie Zhu and Eric Liu. Throughout the Jupyter Notebook, we have made various comments on how the code works. But to give an overall outlook onto the project, it is our personal method to develop a portfolio of 20 stocks that will produce 0% return (thereby creating a safe portfolio). 

## How it works 
First, you input a .csv file of any stock tickers. Using our threading tool, we will filter the data and create a new file that meets our follwoing requirements:
- currency must be denominated by USD
- based in the US market
- average volume of shares traded must be greater than 10,000
* Note that ETFs are considered valid tickers

Sample ticker list: 

<img width="212" alt="Screen Shot 2022-01-18 at 12 00 26 AM" src="https://user-images.githubusercontent.com/82774370/149873686-46ef8348-5853-4559-839d-f7fc9c285c83.png">

Then, we measure the risk of each stock based on alpha, beta, standard deviation, and maximum drawdown. We pair the riskiest stock with its least correlated stock in order to offset the risk, storing the tickers in a tuple list. This is based on the concept of overdiversifying our shares (For more info on diversification, visit: https://www.investopedia.com/terms/d/diversification.asp). 

Sample tuple list: 
![Screen Shot 2022-01-18 at 12 05 17 AM](https://user-images.githubusercontent.com/82774370/149874146-3ccdd0d9-3f2d-48cb-8dd6-9c6afde7f401.png)

Aftering running through our weight optimization algorithm, you are produced with your original ticker list along with its optimal weightings.

Sample optimal weight list: 

![Screen Shot 2022-01-18 at 12 09 34 AM](https://user-images.githubusercontent.com/82774370/149874451-e8e14c3f-a81d-4f4b-b47a-0ad02a9b441f.png)
