# Limit Rating Factors

[comment]: <> (https://codecogs.com/latex/eqneditor.php)

__Circumstances__

I had a miscelaneous coverage with several limits.  I had to set rates for each price point and do it with sparse data.  I had 6 years of data and 60 claims, not nearly enough for full credibility.  

__Derivation__

Suppose you have a box with length S and width F.  Area would be:

<img src="https://latex.codecogs.com/gif.latex?PP&space;=&space;F*S" /></a>

Further assume that if one side changes then in order for the PP to stay the same, then the change of the other side is governed as follows.  

<img src="https://latex.codecogs.com/gif.latex?\partial&space;PP&space;=&space;\partial&space;F*S&space;&plus;&space;F*&space;\partial&space;S&space;=&space;0" /></a>

Now, S obviously represents severity; F represents frequency, and PP represents pure premium.  The change in severity is proportional to the change in limit L.  

<img src="https://latex.codecogs.com/gif.latex?\partial&space;S&space;=&space;\alpha&space;\partial&space;L" /></a>

When we substitute in the above equation, it yields the following.  

<img src="https://latex.codecogs.com/gif.latex?\partial&space;F&space;*&space;S&space;=&space;-&space;F*&space;\partial&space;L" /></a>

<img src="https://latex.codecogs.com/gif.latex?\partial&space;F/F&space;=&space;-\partial&space;L/S" /></a>

<img src="https://latex.codecogs.com/gif.latex?lnF&space;=&space;-L/S&space;&plus;C_{0}" ></a>

<img src="https://latex.codecogs.com/gif.latex?F&space;=&space;F_{0}e^{-L/S}" /></a>

At this point, we can find the expected limited loss by integrating the above survival function from 0 to L.  

<img src="https://latex.codecogs.com/gif.latex?\int_{0}^{L}F_{0}e^{-x/S}dx&space;=&space;F_{0}S(1-e^{-L/S})" /></a>

When the expected limited loss above is divided by the limited expected loss at the base level, we get the following limit factor.  

<img src="https://latex.codecogs.com/gif.latex?factor&space;=&space;\frac{(1-e^{-L/S})}{(1-e^{-L_{B}/S})}" /></a>

At this point, if I calculate the severity S as the average of the 60 claim experience data, the limit factors can be calculated straight forward.   