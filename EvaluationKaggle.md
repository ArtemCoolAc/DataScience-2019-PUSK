
## This text has been copied from Kaggle Competition
>Your submission is scored according to the penalty cost to Santa for suboptimal scheduling. The constraints and penalties are as follows:
>- The total number of people attending the workshop each day must be between 125 - 300; if even one day is outside these occupancy constraints, the submission will error and will not be scored.
>-  Santa provides consolation gifts (of varying value) to families according to their assigned day relative to their preferences. These sum up per family, and the total represents the preferencecost. 
>    - _choice\_0_: no consolation gifts
>    - _choice\_1_: one **$50** gift card to Santa's Gift Shop
>    - _choice\_2_: one **$50** gift card, and 25% off Santa's Buffet (value **$9**) for each family member	
>    - _choice\_3_: one **$100** gift card, and 25% off Santa's Buffet (value **$9**) for each family member
>    - _choice\_4_: one **$200** gift card, and 25% off Santa's Buffet (value **$9**) for each family member	
>    - _choice\_5_: one **$200** gift card, and 50% off Santa's Buffet (value **$18**) for each family member
>    - _choice\_6_: one **$300** gift card, and 50% off Santa's Buffet (value **$18**) for each family member
>    - _choice\_7_: one **$300** gift card, and free Santa's Buffet (value **$36**) for each family member
>    - _choice\_8_: one **$400** gift card, and free Santa's Buffet (value **$36**) for each family member	
>    - _choice\_9_: one **$500** gift card, and free Santa's Buffet (value **$36**) for each family member, and -50% off North Pole Helicopter Ride tickets (value **$199**) for each family member
>    -  otherwise: one **$500** gift card, and free Santa's Buffet (value **$36**) for each family member, and free North Pole Helicopter Ride tickets (value **$398**) for each family member
>
>- Santa's accountants have also developed an empirical equation for cost to Santa that arise from many different effects such as reduced shopping in the Gift Shop when it gets too crowded, extra cleaning costs, a very complicated North Pole tax code, etc. This cost in in addition to the consolation gifts Santa provides above, and is defined as:
>
>![element2](http://latex.codecogs.com/gif.latex?%24%24accounting%5C%20penalty%20%3D%20%5Csum_%7Bd%3D100%7D%5E%7B1%7D%20%5Cfrac%7BN_%7Bd%7D%20-%20125%7D%7B400%7D%20%7BN_d%7D%5E%7B%28%20%5Cfrac%7B1%7D%7B2%7D%20&plus;%20%5Cfrac%7B%5Clvert%20N_d%20-N_%7Bd&plus;1%7D%20%5Crvert%7D%7B50%7D%20%29%7D%20%24%24)
>
>where ![nd](http://latex.codecogs.com/gif.latex?N_%7Bd%7D) is the occupancy of the current day, and ![ndp1](http://latex.codecogs.com/gif.latex?N_%7Bd&plus;1%7D) is the occupancy of the previous day (since we're counting backwards from Christmas!). For the initial condition of ![deq100](http://latex.codecogs.com/gif.latex?d%3D100), ![n101](http://latex.codecogs.com/gif.latex?N_%7B101%7D)=![n100](http://latex.codecogs.com/gif.latex?N_%7B100%7D).
>
>To be clear on the above summation, it starts on the date 100 days before Christmas and ends on Christmas Eve.
>
>And **_finally_**:
>
>_score=preference\_cost+accounting\_penalty_
>
> This may seem complicated, but this nifty-difty starter notebook should get you started fast!
>
**Link to _[original]( https://www.kaggle.com/c/santa-workshop-tour-2019/overview/description)_**
