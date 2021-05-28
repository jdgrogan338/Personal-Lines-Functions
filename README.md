###### Renders better in the jupyter notebook.

# Personal Lines Functions

## Loss Development Model - Damped Harmonic Oscilator
### Over Damped: Cummulative Development $$Factor = 1-(C)e^{(-at)}-(1-C)e^{(-bt)}$$ 
### Under Damped: Cummulative Development  $$Factor =  1-(C)sin(at)e^{(-bt)}-cos(at)e^{(-bt)}$$ 
### Critically Damped: Cummulative Development $$Factor =  1-(C)te^{(-at)}-e^{(-at)}$$  

<br>
<br>
<br>
<br>

## Amount of insurance model factors $$Factor(L) = \frac{(e^{(1-e^{(\frac{-L}{S}))}}-1)}{(e^{(1-e^{(\frac{-L(b)}{S})})}-1)}$$
## Deductibles by amount of insurance factors $$Factor(D|L) = (\frac{(1-\frac{(e^{(1-e^{(\frac{-D}{S})})}-1)}{(e^{(1-e^{(\frac{-L}{S})})}-1)})}{(1-\frac{(e^{(1-e^{(\frac{-D(b)}{S})})}-1)}{(e^{(1-e^{(\frac{-L(b)}{S})})}-1)})})$$

<br>
<br>
<br>
<br>

## Increased Limits Model
### Occurance Limit = Claim Limit ex 500/500 or 500CSL
#### $$ILF = e^{(1-e^{(\frac{-L}{S})})}-1$$
### Occurance Limit = 2xClaim Limit ex 250/500
#### $$ILF = (e^{(1-e^{(\frac{-2L}{S})})}-1) - (e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})*(e^{(e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})})$$
### Occurance Limit = 3xClaim Limit ex 100/300
###### $$ILF = (e^{(1-e^{(\frac{-3L}{S})})}-1) - (e^{(\frac{-L}{S})}-e^{(\frac{-3L}{S})})*(e^{(e^{(\frac{-L}{S})}-e^{(\frac{-3L}{S})})}) + \frac{1}{2}((e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})^2)*(e^{(e^{({-L}{S})}-e^{({-2L}{S})})})$$

<br>
<br>
<br>
<br>

## Homeowners Catastrophe Model (aggregate)
### Mean of aggregate distribution = mean(f)*mean(s)
#### $$mean(F)*mean(S) = E(F)*E(S) = \frac{rp}{1-p}(\alpha AOI)(\Gamma(1+\frac{1}{d})).$$
#### Assume: 
#### The frequency follows a negative binomial distribution.
#### The severity follows a weibull distribution - behaves like a fractal. 
### Variance of aggregate distribution 
###### $$Var(AggDist)= \sum_{n=1}^{\infty} (nE(S^2))+n(n-1)E(S)^2-2nE(S)(E(F)*E(S))+(E(F)*E(S))^2)\binom{r+n-1}{n}p^n(1-p)^r.$$ 
<a target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{150}&space;\tiny&space;Var(AggDist)=\sum_{n=1}^{\infty}(nE(S^2)&plus;n(n-1)E(S)^2-2nE(S)(E(F)*E(S))&plus;(E(F)*E(S))^2)\binom{r&plus;n-1}{n}p^n(1-p)^r" /></a>
#### Where:  
#### E(S) = Mean of Severity distribution.
#### E(S^2) = Second Moment of the Severity Distribution about the origin.
#### n = number of events 
#### r = number of successes.

<br>
<br>
<br>
<br>

## Price implementation model
#### Many times we can only move toward the proposed from current due to disruption.
#### The following optimizes it and assumes that the rates will be in effect for a year.  
#### $$Filed Factor = \frac{(PC)}{(C+(P-C)e^{(-\alpha)})}$$

<br>
<br>
<br>
<br>
