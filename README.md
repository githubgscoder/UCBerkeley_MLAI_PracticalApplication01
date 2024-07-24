# UCBerkeley_MLAI_PracticalApplication01
In this first practical application assignment of the program, you will seek to answer the question, “Will a customer accept the coupon?” The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

Link to Jupyter Notebook: https://github.com/githubgscoder/UCBerkeley_MLAI_PracticalApplication01/blob/6749144a0cf076e1cbc08ececbd77981f33e4c15/prompt.ipynb

### Will a Customer Accept the Coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 


**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Summary**

1. Would you accept that coupon and take a short detour to the restaraunt? 

	Yes, as seen in the image below, a good proportion of drivers are willing to accept the coupon with no hesitation to do so even if the restaurant is in the opposite direction. Proportion_x representing drivers who accepted coupons even though the restaurant was in the opposite direction, 	while Proportion_y represented the drivers who accepted the coupons in the same direction.
	![image](https://github.com/user-attachments/assets/a05faec6-32ae-4c1d-9df7-b48a67bc5b7d)
	![image](https://github.com/user-attachments/assets/f47449d8-82d3-4401-a5a1-ae906f4aa084)

	While it hold true in the case of restaurant coupons offered, we see a slightly higher percentage of drivers accept the coupon in the same direction when we look at the whole dataset and ~60% of drivers had accepted coupons while the rest ~40% rejected them.
	![image](https://github.com/user-attachments/assets/39664d18-ec50-4dd9-9659-39a33a3dfb1b)
	![image](https://github.com/user-attachments/assets/8ac8f1de-9db0-461f-a76c-930a9e83b5e8)


2. Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely?

   While the dataset didn't have an identifier that differentiated if they used it on a subsequent or on during the same trip it was understood that there was a higher percentage of folks that did accepted the coupons that were sent to them.
	 ![image](https://github.com/user-attachments/assets/1cd20d79-59e2-488d-81bc-9db508f990b3)

3. What if the coupon was for a bar instead of a restaraunt?

	 Based on the dataset that was provided it was analyzed that 41% of the bar coupons were accepted. Data also shows that drivers that frequented the bars more than 3 times a month were more than likely to accept a coupon with an acceptance rate of 78%, while the acceptance rate of 				 drivers who visited less than 3 times were only ~37%. Analysis was also done to compare 2 groups, one group that visited the bar more than once and had no kids as passengers and were not alone and taking into consideration that they weren't working in the "Farming Fishing & Forestry" 	 vs everyone else that were offered a bar coupon. ~72% of drivers from group 1 ended up accepted the coupon.

Additional analysis was done to compare 2 groups of drivers based on the below,

		- go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
		- go to bars more than once a month and are under the age of 30 OR
		- go to cheap restaurants more than 4 times a month and income is less than 50K.

It was seen that ~57% of drivers from group 1 accepted the coupon vs ~33% from group 2 who were everyone else that didn't fall into the conditions above.

We applied a similar analysis on drivers that were sent coffee house coupons and noticed that drivers that visited a coffee house more than 3 times month were also more likely to accept the coupon at an acceptance rate of ~68% vs ~45% that visited the coffee house less than 3 times. 

When we looked at two groups of drivers based on the condition below,

		Group 1:
		- Drivers who've went to the coffee house more atleast once and 
		- were above the age of 25
		- accepted the coupon
		Group 2:
		- All others

 It was seen that drivers in group 1 were also more likely to accept coupons at an acceptance rate of ~64% vs drivers in group 2 who had an acceptance rate of ~43%

 Another grouping was done on all who were offered the coffee house coupon as seen below,

		Group 1:
 		- Drivers who visited the coffee house at least once.
	 	- Drivers who were retired
	 	- Drivers that accepted the coupon
	 Group 2:
		- All others

 As expected it was seen that drivers that normally visit a coffee house atleast once and were retired tend to accept the coffee house coupon with an acceptance rate of ~64% as oppposed to ~50% for all others that were offerred the coffee house coupon.

 One more set of grouping was done as seen below,

		Group 1:
 		- go to coffee house more than once a month, had passengers that were not a kid, and were not widowed OR
		- go to coffee house more than once a month and are under the age of 30 OR
		- go to cheap restaurants more than 4 times a month and income is less than 50K.
		Group 2:
		- All others

 In this analysis drivers in group 1 had an acceptance rate of 64% vs ~39% for group 2.

 It can be seen that factors such as occuptation, age and the times that they go out have an impact on drivers accepting the coupon, irrespective of the direction at which the coupon destination.

 It is also seen as expected that weather to plays and important role in whether drivers accept coupon with a higher percentage of drivers accepting when it is Sunny vs when it rains or snows with drivers least likely to accept a coupon during a snowy weather. A distribution plot was also drawn to see the temperature distribution and when grouped by temperature we can see a higher percentage of acceptance ~60% when then weather is 80 as opposed to ~53% when it's 30 and 55 respectively. 
 
 ![image](https://github.com/user-attachments/assets/a4780c76-be4e-4ca8-baaa-cf97603baf84)

![image](https://github.com/user-attachments/assets/320fb32d-8766-4c04-b40b-b6577e2ba1a3)
![image](https://github.com/user-attachments/assets/f175f259-9c7f-41f4-b513-0a425287972c)


We also looked into coffee house coupons and bar coupons to see if time is a factor in acceptance and based on the two plots as seen below, it is clearly evident that,

		- There was approximately a ~10% increase in acceptance rate when bar coupons were offered around 6 PM and 10 PM.
		- There was a higher acceptance rate of ~64% at 10 AM and ~54% at 2 PM when compared to all other time's the coupons were offered.
		
	Legend
		0 - Rejected
		1 - Accepted

![image](https://github.com/user-attachments/assets/42414c45-1d0f-4dda-9b02-51826a52a50f)
![image](https://github.com/user-attachments/assets/7d6c82a2-6477-468e-975b-7d196575ab42)

	
	
