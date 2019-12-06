<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
## This text has been copied from Kaggle Competition##
>Your submission is scored according to the penalty cost to Santa for suboptimal scheduling. The constraints and penalties are as follows:
<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
>- The total number of people attending the workshop each day must be between 125 - 300; if even one day is outside these occupancy constraints, the submission will error and will not be scored.
-  Santa provides consolation gifts (of varying value) to families according to their assigned day relative to their preferences. These sum up per family, and the total represents the preferencecost. 
 - _choice___0_: no consolation gifts
 - _choice___1_: one $50 gift card to Santa's Gift Shop
 - _choice___2_: one $50 gift card, and 25% off Santa's Buffet (value $9) for each family member	
 - _choice___3_: one $100 gift card, and 25% off Santa's Buffet (value $9) for each family member
 - _choice___4_: one $200 gift card, and 25% off Santa's Buffet (value $9) for each family member	
 - _choice___5_: one $200 gift card, and 50% off Santa's Buffet (value $18) for each family member
 - _choice___6_: one $300 gift card, and 50% off Santa's Buffet (value $18) for each family member
 - _choice___7_: one $300 gift card, and free Santa's Buffet (value $36) for each family member
 - _choice___8_: one $400 gift card, and free Santa's Buffet (value $36) for each family member	
 - _choice___9_: one $500 gift card, and free Santa's Buffet (value $36) for each family member, and
  -50% off North Pole Helicopter Ride tickets (value $199) for each family member
 - otherwise: one $500 gift card, and free Santa's Buffet (value $36) for each family member, and free North Pole Helicopter Ride tickets (value $398) for each family member
- Santa's accountants have also developed an empirical equation for cost to Santa that arise from many different effects such as reduced shopping in the Gift Shop when it gets too crowded, extra cleaning costs, a very complicated North Pole tax code, etc. This cost in in addition to the consolation gifts Santa provides above, and is defined as:
$$accounting\ penalty = \sum_{d=100}^{1} \frac{N\_{d} - 125}{400} {N\_d}^{( \frac{1}{2} + \frac{\lvert N\_d -N\_{d+1} \rvert}{50} )} $$

>where Nd is the occupancy of the current day, and Nd+1 is the occupancy of the previous day (since we're counting backwards from Christmas!). For the initial condition of d=100, N}=N100.
To be clear on the above summation, it starts on the date 100 days before Christmas and ends on Christmas Eve.

>And **_finally_**:

>_score=preference\_cost+accounting\_penalty_
>This may seem complicated, but this nifty-difty starter notebook should get you started fast!

**Link to _[original]( https://www.kaggle.com/c/santa-workshop-tour-2019/overview/description)_**
