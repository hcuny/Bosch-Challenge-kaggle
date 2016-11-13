# XGBOOST-kaggle
Data science competition
https://www.kaggle.com/c/bosch-production-line-performance

A good chocolate soufflé is decadent, delicious, and delicate. But, it's a challenge to prepare. 
When you pull a disappointingly deflated dessert out of the oven, you instinctively retrace your steps to identify 
at what point you went wrong. 

Bosch, one of the world's leading manufacturing companies, has an imperative to ensure that 
the recipes for the production of its advanced mechanical components are of the highest quality and safety standards. 
Part of doing so is closely monitoring its parts as they progress through the manufacturing processes.

Because Bosch records data at every step along its assembly lines, they have the ability to apply advanced analytics to improve these manufacturing processes. However, the intricacies of the data and complexities of the production line pose problems for current methods.

In this competition, Bosch is challenging Kagglers to predict internal failures using thousands of measurements and tests made for each component along the assembly line. This would enable Bosch to bring quality products at lower costs to the end user.
-------------------------------------------------------------------------------------------------------------------
Read order: numeric feature selection --> date feature selection --> categorical data selection

Numeric features are the most basic ones, thus it's the first one to choose (based on XGB's feature importance),
later two are based on the former combo.

Note that the data is too large to load on a single PC (especially categorical data), thus I used read-by-chunk technique, and then combine the chunk features by some order. As exploration, read random data is also tried, but it caused some problems such as the change of column names.

Feature engineering process is interesting but aslo addictive, see "additional featrues" and some descriptive ones (for instance, number of non-NAN values in a row, max, min, mean of a row, number of distinct operations in a row ect.) in the first three files.

Training: including XBG training and SKlearn API training, and also CVs.

--------------------------------------------------------------------------------------------------------
Rank: 154 / 1391 ( 11% )
