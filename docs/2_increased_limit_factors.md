# Increased Limits Model

__Circumstances__

It was difficult in my generalized linear model to adequately represent the auto limit Factors.  I didn't understand the behavior of the risk.  By this, I mean, I didn't know how one split limit should be rated relative to another split limit in theory.  I needed a smooth transition from level to level in order to maintain control of my correlated variables like age and credit, but my attempts at curve fitting yielded erroneous results.  In general, I had two mass points 100/300 and 250/500, and all other levels were sparse.  If could figure out a way to convert the limit to a number, according to a solid theory, then I could leverage the two mass points to govern the shape of the entire rating plan.  

__Derivation__

We begin with the assumptions and derivation of the limit factor model.  Then we will extend it to a system where multiple claims may occur limited by L.  This would be similar to a multicar pile up.  

The first step is to consider one claim.  This will behave linearly and will look like the limit factor model:
<div align="center"><img src="https://latex.codecogs.com/gif.latex?F(L)=F_{0}S(1-e^{-L/S})" /></div>

Not too mysterious, we've seen this before.  If we continue to a two claim system and look at this graphically, we get:

![Two Claim System](images/two_claim_system.png)

As you can see, the two claim system is limited.  If claim1 is L1, then claim2 is the occurence limit (L) less L1.  The area is:

<div align="center"><img src="https://latex.codecogs.com/gif.latex?F(L)=\frac{1}{2}(F_{0}S(1-e^{-L/S}))^2" /></div>

Let's look at the 3 claim system.  

![Three Claim System](images/three_claim_system.png)

[1] [Three Claim System](assets/pythonrendering.ipynb)

Now, the three claim system is limited.  If claim1 is L1 and claim2 is L2, then claim3 is the occurence limit (L) less L1 and L2.  The volume is:

<div align="center"><img src="https://latex.codecogs.com/gif.latex?F(L)=\frac{1}{6}(F_{0}S(1-e^{-L/S}))^3" title="F(L)=\frac{1}{6}(F_{0}S(1-e^{-L/S}))^3" /></div>

There is no way to display a 4 dimensional claim system, but a pattern is starting to emerge.  If we add all outcomes in this series from 1 claim to infinity, we yield the following common scenarios:

### Occurance Limit = Claim Limit ex 500/500 or 500CSL:
<div align="center"><img src="https://latex.codecogs.com/png.image?F(L)=e^{F_{0}S(1-e^{(\frac{-L}{S})})}-1"/></div>

### Occurance Limit = 2xClaim Limit ex 250/500:
<div align="center"><img src="https://latex.codecogs.com/png.image?F(L)=(e^{F_{0}S(1-e^{(\frac{-2L}{S})})}-1)-(e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})*(e^{F_{0}S(e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})})"/></div>

### Occurance Limit = 3xClaim Limit ex 100/300:
<div align="center"><img src="https://latex.codecogs.com/gif.latex?\tiny&space;F(L)=(e^{F_{0}S(1-e^{(\frac{-3L}{S})})}-1)-(e^{(\frac{-L}{S})}-e^{(\frac{-3L}{S})})*(e^{F_{0}S(e^{(\frac{-L}{S})}-e^{(\frac{-3L}{S})})})&plus;\frac{1}{2}((e^{(\frac{-L}{S})}-e^{(\frac{-2L}{S})})^2)*(e^{F_{0}S(e^{({-L}{S})}-e^{({-2L}{S})})})" /></div>

When the expected limited loss above is divided by the limited expected loss at the base limit, we get the limit factor.  

What else can we learn from this model?  
1. If the model is correct, could we introduce more limit combinations (e.g. Occurance = 4xClaim)?
2. How do we transform this and use it in a multivariate analysis?
