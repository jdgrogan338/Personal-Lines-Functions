[comment]: <> (https://codecogs.com/latex/eqneditor.php)

# Limit Rating Factors

__Circumstances__

I had a miscelaneous coverage with several limits.  I had to set rates for each price point and do it with sparse data.  I had 6 years of data and 60 claims, not nearly enough for full credibility.  

__Derivation__

Suppose you have a box with length S and width F.  Area would be:

<div align="center"><img src="https://latex.codecogs.com/gif.latex?PP&space;=&space;F*S" /></div>

Further assume that if one side changes then in order for the PP to stay the same, then the change of the other side is governed as follows.  

<div align="center"><img src="https://latex.codecogs.com/gif.latex?\partial&space;PP&space;=&space;\partial&space;F*S&space;&plus;&space;F*&space;\partial&space;S&space;=&space;0" /></div>

Now, S obviously represents severity; F represents frequency, and PP represents pure premium.  The change in severity is proportional to the change in limit L.  

<div align="center"><img src="https://latex.codecogs.com/gif.latex?\partial&space;S&space;=&space;\alpha&space;\partial&space;L" /></div>

When we substitute in the above equation, it yields the following.  

<div align="center"><img src="https://latex.codecogs.com/gif.latex?\partial&space;F&space;*&space;S&space;=&space;-&space;F*&space;\partial&space;L" /></div>

<div align="center"><img src="https://latex.codecogs.com/gif.latex?\partial&space;F/F&space;=&space;-\partial&space;L/S" /></div>

<div align="center"><img src="https://latex.codecogs.com/gif.latex?lnF&space;=&space;-L/S&space;&plus;C_{0}" ></div>

<div align="center"><img src="https://latex.codecogs.com/gif.latex?F&space;=&space;F_{0}e^{-L/S}" /></div>

At this point, we can find the expected limited loss by integrating the above survival function from 0 to L.  

<div align="center"><img src="https://latex.codecogs.com/gif.latex?\int_{0}^{L}F_{0}e^{-x/S}dx&space;=&space;F_{0}S(1-e^{-L/S})" /></div>

When the expected limited loss above is divided by the limited expected loss at the base limit, we get the following limit factor.  

<div align="center"><img src="https://latex.codecogs.com/gif.latex?factor&space;=&space;\frac{(1-e^{-L/S})}{(1-e^{-L_{B}/S})}" /></div>

At this point, if I calculate the severity S as the average of the 60 claim experience data, the limit factors can be calculated straight forward.  This is the base for the other limit functions developed in this repository.  In addition, think of S as a hyperparameter which can be used to optimize the function.  This will be handy when inserting into a generalized linear model.  