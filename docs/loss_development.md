# Loss Development Model
## Damped Harmonic Oscillator - Cummulative Development
<!---
Comment:
https://codecogs.com/latex/eqneditor.php
about.gitlab.com/handbook/markdown-guide/
--->

__Circumstances__

In order to speed up processing during the quarterly ratemaking process, I needed to have the machine process as much of the analysis as possible.  This would give me more time to evaluate the performance measures.  I let the machine process, and I would perform the reasonability check.  When this was in full use, it changed my total processing time from a day and half to about 10 minutes.  

__Derivation__

The claims process begins with the occurrence of a claim event.  When the event occurs the claimant is displaced from his equilibrium.  To the extent that the claimant is willing and able to make a claim, he will return to equilibrium.  To the extent that the claims organization is willing or able to pay the claim, via contract language and processing, the company will dampen the return to equilibrium.  This is a damped harmonic oscillator, represented as follows:
<div align="center"><img src="https://latex.codecogs.com/gif.latex?\frac{d^{2}L(t)}{dt^{2}}+\lambda\frac{dL(t)}{dt}+\omega^2(L(t))=\omega^2(L(\infty))" /></div>

Where <img src="https://latex.codecogs.com/gif.latex?L(t)"> is the loss at time t. <img src="https://latex.codecogs.com/gif.latex?L(\infty)"> is the Ultimate loss.  <img src="https://latex.codecogs.com/gif.latex?\lambda"> and <img src="https://latex.codecogs.com/gif.latex?\omega"> are parameters.  

This can be solved 3 ways.  When we group claim types and analyze them over time, these are the paterns that emerge.  
### Over Damped: 
<div align="center"><img src="https://latex.codecogs.com/gif.image?LDF_{cumm}=1-(C)e^{(-at)}-(1-C)e^{(-bt)}"/></div>

Where a and b are function of <img src="https://latex.codecogs.com/gif.image?\lambda"/> and <img src="https://latex.codecogs.com/gif.image?\omega"/>.  Bodily injury claims develop this way.  

![Over Damped](images/overdamped.png) 

### Under Damped: 
<div align="center"><img src="https://latex.codecogs.com/gif.image?LDF_{cumm}=1+(C)sin(at)e^{(-bt)}-cos(at)e^{(-bt)}"/></div>

Underinsured and uninsured motorist coverage with the low frequency and high severity claim types behave this way.  

![Under Damped](images/underdamped.png)

### Critically Damped: 
<div align="center"><img src="https://latex.codecogs.com/gif.image?LDF_{cumm}=1+(C)te^{(-at)}-e^{(-at)}"/></div>

Comprehensive and Collision coverage, with the salvage and subrogation behave this way.

![Critically Damped](images/criticallydamped.png)

What else can we learn from this model?  
1. Proof:  How do we prove that this is actually the pattern that claims follow?
2. How should we interpret the parameters a and b?
3. Can it be used to analyze claims at the claim level?