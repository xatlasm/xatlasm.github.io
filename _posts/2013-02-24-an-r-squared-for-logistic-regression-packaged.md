---
layout: post
title: An R-squared for logistic regression, packaged
tags:
- Stata
- logistic regression
---
This morning I checked Paul Allison's Statistical Horizons blog and found [a post on \\(R^2\\) measures for logistic regression](http://www.statisticalhorizons.com/r2logistic). It introduced me to Tjur's \\(R^2\\) by way of an example, which I repackaged below:

```

// Reference: http://www.statisticalhorizons.com/r2logistic
// program definition
capture prog drop tjur2
program tjur2, rclass
if !inlist(e(cmd),"logit","logistic") {
   di as err "Tjur's R-squared only works after logit or logistic."
   exit 498 // Thank you, Nick Cox.
}
tempname yhat
predict `yhat' if e(sample)
local y `e(depvar)'
quietly ttest `yhat', by(`y')
local r2logistic r(mu_2)-r(mu_1)
di "Tjur's R-squared " _col(20) %4.3f `r2logistic'
return local r2logistic `r2logistic'
end

// use case
use "http://www.uam.es/personal_pdi/economicas/rsmanga/docs/mroz.dta", clear
logistic inlf kidslt6 age educ huswage city exper
tjur2

```

I'm not sure yet if it's worth saving this program as `ado/personal/t/tjur2.ado` for my future logistic regression diagnostic needs, but I haven't posted anything Stata-related in too long, so there you have it.
