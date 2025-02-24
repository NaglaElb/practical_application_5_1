# practical_application_5_1
UC Berkeley Assignment

https://github.com/NaglaElb/practical_application_5_1.git

# Overview
This notebook contains an analysis of data from UCI Machine Learning Repository that was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver.
The objective of the code is to identify characteristics of those who accepted the coupon versus those who did not.
Data:
Beyond data cleansing that needs to happen with multiple columns in the data set, and the null values that need to be addressed, there are two major flaws with this data set.
First, acceptance of the coupon is not differentiated enough.  Combining “right away” or “later before the coupon expires” could mask an important differentiator.  Additionally, accepting a coupon is not the same as using the coupon, especially considering there is no “down side” to accepting a coupon that you may or may not use.
The fact that there is no down side plays out in the data.  Everyone in the data set accepted the coupon if they were within 5 minutes of the destination.  In this case, the characteristics of the people who accepted the coupon are the characteristics of the people who happen to be in your dataset. 
The only columns that will help with differentiation are the columns showing those who accepted the coupon at 15 minutes and at 25 minutes. It turns out that 50% accepted the coupon within 25 minutes, 50% accepted the coupon within 15 minutes.  When these columns were added together, the only outcomes were 1 and 3 accptances, which means that everyone who accepted at 25 minutes also accepted at 15 minutes and again at 5 minutes.  
Were they the same 50%? Yes.  So coupons offered at 15 minutes and 25 minutes to destination are redundant.  Probably 15min to destination is better than 25 because the number of acceptances goes up as they get closer.

## Observations about drivers who accepted bar coupons:
Bar coupons  were accepted 66% of the time
90% of drivers who frequented bars less than 3 times/month accepted a coupon
4% of drivers who frequented bars more than 3 times/month accepted a coupon
30% of drivers who frequented a bar more than once/month and are over 25 years old accepted a ooupon
5% of drivers who frequented a bar more than once a month and are under 25 years old accepted a coupon
These drivers tended to be over the age of 25 and more than likely don’t have kids as passengers.
I can interpret the low proportion of only 11 percent of drivers who frequent bars more then 4 times/month and accepted the coupon demonstrates that frequency of customer habits is not necessarily a driver for accepting the coupon. Those who frequented bars less frequently accepted the coupon at 90%. While this seems counterintuitive, it could be because those who like to drink are more picky about their bars.

## Observations of drivers who accepted Carry Away coupons
•	Equally split between men and women
•	Definitely higher for people <30
•	Marital status and destination are not significant factors
•	Sunny weather makes a big difference
•	Warm weather tends to help
•	Less effective around 2pm and most effective at 7am
•	It helps that they are going in the same direction
•	On their way home

## Next Steps
Because the acceptance of a coupon doesn't show if it is actually used, the next step would be to focus on coupons that were actually redeemed.  Find out the percentage of each type of coupon that was actually redeemed and if possible a total amount spent at the establishment where they redeemed the coupon.  

Additionally, it would be useful to get more fidelity on whether the coupon was accepted immediately or later. In this data set, the two were combined and appeared as Yes or 1 for accepting the coupon.  Being able to differentiate those two would be helpful. 

Finally, other driver attributes can be collected like 
--day of the week to see if there is more coupon acceptance on weekdays versus weekends
--highway versus city driving
--coupon by specific vendor establishment


