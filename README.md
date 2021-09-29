# Investing-simulator

The program is a simulation of a "buy and hold" strategy, in which the user provides four different pieces of information:
- Which stock is bought (Defined through the ticker symbol)
- The duration of the investment period, defined between two dates
- The amount of money invested each time a purchase is made
- How often a purchase is made, defined through a regular interval.

Given these pieces of information, the program calculates how much profit (or deficit) the investment strategy would yield over the duration of the investment period in the following manner:


First, two different lists are made:
- The first list consists of the amount of shares bought at ervery given point in time, calculated through dividing the investment sum with the temporary share price.
- The second list is the compounded sum of all share purchases done at every point in time based on the first list.
 
To better explain this, here is an example:
Given the investment amount 500$ we buy

- 50 shares in month 1
- 100 shares in month 2
- 33 shares in month 3 
- 50 shares in month 4

This could be expressed in a list:

[50, 100, 33, 50]

The compounded sum of this list will therefore be:

[50, 150, 183, 233]

where every item in the list is the sum of itself and every previous item. 

If the price of the share is:

- 10$ in month 1
- 5$ in month 2
- 15$ in month 3 
- 10$ in month 4 

we multiply these values with the corresponding values in the compounded sum list:

[50, 150, 183, 233] * [10, 5, 15,10] = [500, 750, 2745, 2330]. 

The product corresponds to the value of our investment at every month.

The total amount invested each month is represented by the list: 

[500, 1000, 1500, 2000]

The last month we will have 2330$ and have invested a total of amount of 2000$. Lastly, the value of the investment and the total investment contributions are visualized in plots.

This program with above mentioned methods can be further used to for example, study which investment frequencies are most profitable given a set amount of money available.
