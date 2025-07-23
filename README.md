# Brief Overview Report

Using the given dataset found in the data folder (and available here: https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation) we explore a survey of different driving scenarios each with unique factors before asking a person whether they would accept usage of the coupon. The dataset was downloaded and read before being cleaned on via the removal of attributes that weren't necessary (particularly the 'car' file) and all rows with missing values were dropped. The final cleaned dataset was 12079 rows witth 26 unique columns. The full exploration of this dataset can be found in the provided notebook. Meanwhile this file will serve as a brief, nontechnical summary report of the study.

First I determined that exploring each unique coupon proved better than to treat each coupon as the same. This proved sound as each group determined to have their own unique factors. Because of this decision, each group is analyzed indivudally below.

### Bar Coupons:

The most important variable here was the number of visits a person had to a bar per month. Customers who listed their monthly visit rates to bars between 4 and 8 and greater than 8 saw higher likelihood of utilizing the bar coupon. This groupings under these values also had a correlation to another value within the ride passenger column, where trips that did not contain children also saw increased chances of coupon usage. Both of these values make sense since people more likely to visist bars would also be more likely to want a bar coupon, and would rather not bring their kids to there either. Following these values, widowed individuals, those below age 30, and those with less than 50k income saw increased coupon usage as well. That said, it seemed the more impactful variables were the former two due to showing up more often and great correlation strength.

### Takeout Coupons:

Temperature proved quite interesting in that all 3 of its unique values (30, 55, and 88) were useful towards predicting greater coupon usage, where temperatures of 33 and 80 saw great coupon usage by itself, while a temperature of 55 also saw good coupon usage under sunny and snowy weather. Meanwhile, education played an important part for higher predictions where those falling under a some high school, some college but no degree, and an associate degree saw higher coupon usage. Time also proved useful, with higher usage linked at times 2 PM, 6 PM, and 10 PM.

### Coffee Coupons:

Monthly visits to a coffeehouse proved most useful as expected, where having at least 1 visits saw increased coupon usage and below that threshold saw decreased usage. Interestingly, the factor of whether the coffeehouse was in the direction of the vehicle's trip also proved useful in a similar manner (along the way saw higher rates and vice versa). The final important factor were the passenger and expiration date variables. Those with friends and/or kids as passengers and an expiration time periods of 1d saw higher usage but those with friends, kids, and/or were alone along with an expiration time period of 2h saw lower usage. Time was also useful for higher usage, particuarly at 10 am and 2 pm.

### 20$ or less Restaurant Coupons:

Destination seemed to be an important factor where customers saw greater coupon usage when there was no urgent place for destination. Income saw greater usage for less than $20 coupons as well, particularly in ranges $50-75k, $25-37k, and less than $12.5k. Conversely, income also proved useful to predicting less coupon usage in ranges $87.5k-100k. Another variable that proved useful on both sides was weather where sunny weather saw higher usage rates and rainy/snowy weather saw lower. Other useful features for predicting usage were times at 6 pm and 7 am improving usage, expiration times of one day improving usage, and marital statuses of divorced or widowed worsening usage. Interesting, bar visits per month were actually useful for prediction here, where 1-3 or 4-8 visists per months saw greater coupon usage.

### 20$ to 50$ Restaurant Coupons:

Once again visits to the area a coupon focused on proved useful here where less than 1 visits to $20-50 restaurants led to lower coupon usage and gr8 visits led to higher. Passengers were also important where kid(s) or being alone led to low usage but having a parter led to high usage. Following these two variables, weather under snowy or rainy saw decreasing coupon usage here in conjunction. The remaining values proved useful only to lower coupon usage, such as age at 21 or 50 plus; income less than $12.5k or $75k-99k; destination being home; and time being 10 pm. Interestingly, there were a lot of values here that led to lower coupon usage, much more than higher coupon usage.

## Overall and Next Steps

In the end, we found useful variables to help explain both higher and lower coupon usage for each category. Certain variables aligned across categories such as weather or passengers but we also saw unique variables and variable combinations depending on the coupon in question. The next step should to put our findings to the test with a prediction model to see if we can accurately use our found variables to predict a coupon's usage.
