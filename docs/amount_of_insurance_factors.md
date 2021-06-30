# Homeowners Amount of Insurance Factors

__Circumstances__
It was difficult in my generalized linear model to adequately represent the Homeowners Factors.  I needed a smooth transition from level to level, but my attempts at curve fitting yielded inadequate results.  Because there was sparse data in the lower limits, curve fitting attempts were not providing the business with adequate rates at the lower limits.  

__Derivation__

<div align="center"><img src="https://latex.oncodecogs.com/png.image?AOI-Factor=\frac{(e^{(1-e^{(\frac{-L}{S}))}}-1)}{(e^{(1-e^{(\frac{-L_b}{S})})}-1)}"/></div>

## Deductibles by amount of insurance factors: 
<div align="center"><img src="https://latex.oncodecogs.com/png.image?DED-by-AOI-Factor=(\frac{(1-\frac{(e^{(1-e^{(\frac{-D}{S})})}-1)}{(e^{(1-e^{(\frac{-L}{S})})}-1)})}{(1-\frac{(e^{(1-e^{(\frac{-D_b}{S})})}-1)}{(e^{(1-e^{(\frac{-L_b}{S})})}-1)})})"/></div>

