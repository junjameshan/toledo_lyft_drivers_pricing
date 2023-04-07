# Case Study: Pricing for Toledo Lyft Drivers 

![image](https://user-images.githubusercontent.com/123096758/230654389-d8cdd790-5a9e-411f-8f92-e64d8bf13890.png)

## Background

Lyft is a ride-sharing and vehicles-for-hire as a service app that is mainly operating within the United States and parts of Canada. The app is used to request drivers by riders to take them from one destination to another for a price that is dynamically changing based on many factors such as time, location, and even weather as well. For this case study, how would you maximize the company's net revenue (the difference between the amount riders pay and the amount Lyft pays out to drivers) for the route from Toledo Express Airport to downtown Toledo for the next 12 months? 

**Core Question: How much more or less do you pay drivers per trip (by changing Lyft's take)? in order to maximize net revenue for Lyft for the next 12 months on this route.**

## Assumptions & Given Values 

In order to perform the analysis of the case study, it was imperative to take note of the given values and information in order to make educated assumptions. 

The following given values are as provided: 

**Current Prevailing Rates**

- Rider’s rate: $25 (This is the rate that riders will pay for a one-way route from Downtown Toledo to the airport or vice versa) 
- Driver’s wage: $19 (Rate that drivers will earn for their one-way route drive from Downtown Toledo to the airport or vice versa) 
- Wage rate percentage: ($19/$25) * 100% = 76% (This is the percentage of the total wages that drivers will earn for their drive) 
- Current Lyft take rate: $6/Ride (This is the rate that Lyft will earn as revenue for per drive)
- Current Lyft take rate percentage: ($6/$25) * 100% = 24% (This is the percentage of the total wages that Lyft will earn as revenue from a successful completion of a trip by a driver) 

**Experimental Pricing Rates**

- Experimental Lyft take-away price (Revenue): $3/ride 
- Increased Experimental Match Rate: 93% (From 60%, a 33% increase) 
- Based on the calculation shown below, it appears that for every $1 decrease in the revenue generated on Lyft’s end, there is an 11% match rate increase
- Change in Match Rate = ∆Match Rate / ∆Lyft Take Away Rate

**Unit Economics** 

- At the current rate, drivers are estimated to do roughly 100 rides/month
- At the current rate, riders request 1 ride/month on average

Once the given values were determined, it was necessary to make a few educated assumptions in order to conduct the analysis. Based on the information provided, what stood out for me were determining the estimated number of Lyft drivers in Toledo and the number of total passengers that would be commuting in and out of downtown Toledo to the airport in a month. After determining what values were missing, I was able to make an educated assumption on each value based on the research that I conducted: 

**Assumptions** 

-	No new drivers and riders will be signing up during this 12-month period and we will be only focusing on the current active users. 
-	The closest airport to Downtown Toledo is Toledo Express Airport, which is approximately a 30-minute commute one way. This is the airport that we will assume that travelers from Toledo will be commuting in and out from. 
-	I have estimated number of taxi drivers in Toledo to be 440. This value was calculated based on the estimated number of taxi drivers employed added by the increase in growing rate of 10% as referenced by the Trade College article. 
-	For this case analysis, we will assume that all 440 of the taxi drivers are also employed by Lyft.
-	I have estimated the total number of travelers into Toledo Express Airport to be approximately 179,911 passengers. We are using this value as this was the number estimated by the number of passengers at Toledo Express Airport in 2015 as referenced by the Toledo Blade article.
-	Based on the two closest nearing cities within Toledo (approximately <1-hour commute), I estimated the percentage breakdown of those who would be travelling to downtown Toledo from the Toledo Express Airport as opposed to the other two nearby cities based on the population size of each city:

1. Current population of Toledo estimated to be 267,503 people (Referenced by the world population review article.)
2. Current population of Detroit estimated to be 624,177 people (Referenced by the world population review article.)
3. Current population of Ann Arbor estimated to be 125,835 people (Referenced by the world population review article.)
4. Total of 1,017,515 people across all three cities 

- Based on population size, I broke down the total percentage of those who would be travelling to each of the city from the airport: 

1. Toledo: ((267,503/1,017,515) * 100%) * 179,911 = 47,298 average yearly travelers into Toledo  
2. Detroit: ((624,177/1,017,515) * 100%) * 179,911 = 110,364 average yearly travelers into Detroit
3. Ann Arbor: ((125,835/1,017,515) *100%) *179,911 = 22,249 average yearly travelers into Ann Arbor

- As estimated from the calculation, we can anticipate that in a year, approximately 47,298 travelers from the Toledo Express Airport will commute into Toledo or average of 3,942 travelers every month. 

## Analysis

After compiling the data needed to dive into the case study, I was able to conduct the analysis to help further breakdown each value that will factor into the total annual estimated revenue. 

To begin the analysis, I first looked at the estimated churn in drivers for each month as well as the estimated generated revenue per month from the drivers. By using a churn rate of 20% per month for the active drivers, I was able to write up a formula that will determine the number of active drivers per month. 

- D_f = D_i - (D_i * _Churn rate of drivers_)

  - D_f: Number of drivers in the next month 
  - D_i: Number of drivers in the previous month
  - _Churn rate of drivers_: 22% 
  
This formula took into account the rate at which the number of active drivers in Toledo would be decreasing by based on the churn rate of 20% and determined what the estimated number of active drivers would be for the following month. 

In addition to calculating the number of active drivers for each month, I was able to create a formula to determine the estimated revenue per month based on the number of active for each month as well. 

- Revenue per month = D_m * N_d * L * M

  - D_m: Number of drivers active in Toledo in the corresponding month
  - N_d: Number of rides a driver completes a month (100 rides/month) 
  - L: Lyft revenue rate (Take-Rate)
  - M: Match rate 
  
As an example, using the Lyft Take-Rate to be $6/ride and the Match Rate to be 60%, I was able to calculate the total estimated number of active drivers in Toledo for each month for a 12-month period as well as the generated revenue for each month shown by the chart below. 

![image](https://user-images.githubusercontent.com/123096758/230658322-84ad8083-2165-42e3-a897-fdf58629c5b1.png)

The next part of the analysis involved calculating the estimated number of riders active in Toledo for each month and the revenue the riders would generate for each month as well. In order to calculate the total number of churned riders per month, I had to take into account the two separate churn rates per month based on each of the rider’s experience. Ultimately, the formula I created to calculate the total number of riders active in Toledo per month is as shown below. 

- R_f = R_i - ((R_i *M) * C_1) + ((R_i * (1 - M) * C_2))

  - R_f: Number of active riders in Toledo the next month 
  - R_i: Number of active riders in Toledo the previous month
  - M: Match rate
  - C_1: Rider churn rate per month for those who don't experience "failed to find a driver" (10%)
  - C_2: Rider churn rate per month for those who do experience "failed to find a driver" once or more (33%) 
  
The equation to calculate the number of active riders in Toledo for the next month was formulated by first breaking down the churn rate calculations for each group of the riders. 

For the first group, we focused on the riders who did not experience a “failed to find a driver” while utilizing the app. This group would be calculated by taking the current match rate and multiplying it by the number of active riders for the previous month. The match rate indicates that a rider who requested a driver were able to find a driver at the prevailing price point that they are used to paying, so it was used to determine the number of active riders who did not experience a “failed to find a driver”. 

- (R_i * M)

The second group was focused on the riders who did experience a “failed to find a driver” at least once while utilizing the app. This group would be calculated by taking the difference of the current match by 100% and multiplying it by the number of active riders for the previous month. The difference of the current match rate or the “un-match rate” indicates the percentage of the riders who were unable to find a driver at the prevailing rate that they are accustomed to and therefore experience “failed to find a driver” at least once. 

- (R_i * (1 - M))

By multiplying the corresponding churn rate for each calculated group and adding them together, the estimated number of total churned riders can be determined by subtracting the difference to that of the number of active riders from the previous month. 

- ((R_i *M) * C_1) + ((R_i * (1 - M) * C_2))

Similar to calculating the total revenue generated per month by the drivers, I utilized the same formula to calculate the total revenue generated per month by the riders by substituting a few of the key values. 

- Revenue per month = R * N_r * L * M

  - D_m: Number of drivers active in Toledo in the corresponding month 
  - N_r: Number of rides a rider requests a month (1 ride/month)
  - L: Lyft revenue rate (Take-Rate)
  - M: Match rate 
  
As an example, using the Lyft Revenue Rate to be $6/ride and the Match Rate to be 60%, I was able to calculate the total estimated number of active riders in Toledo for each month for a 12-month period as well as the generated revenue for each month shown by chart below. 

![image](https://user-images.githubusercontent.com/123096758/230658951-81201dd4-ac14-4afa-a4f0-9b17934edf45.png)

## Conclusion & Recommendations 

From the analysis I have conducted, I was able to estimate the total annual revenue based on the revenue generated by the drivers as well as the riders. In order to see the differences in the generated revenue, I used various experimental values ranging from $3/ride - $7/ride for the take-rate as well as its corresponding match rate. 

As shown by the graph below, the annual estimated revenue generated by the drivers saw an upward trend, topping out at a maximum value of $737,574 when the take rate was set to $6. It then proceeded to a decline in the generated revenue as the take rate was increased further on from $6/ride. 

![image](https://user-images.githubusercontent.com/123096758/230659031-0603e5ba-5337-4429-9c73-802120125319.png)

For the annual estimated revenue generated from the riders, it saw the opposite trend from that of the drivers. As shown by the graph below, there is a downward slope in the total generated revenue as the take rate was increased. The exception to this pattern was the increase in take-rate from $3/ride to $4/ride and this is also where we see the maximum value for the revenue generated hit climax at a value of $76,754 when the take-rate was set at $4/ride.

![image](https://user-images.githubusercontent.com/123096758/230659062-d4e40629-837a-479c-9218-6139f794765d.png)

Combining both values calculated from the riders and drivers, I was able to compute the total annual estimated revenue based on the experimental take rates. The graph below captures the trend in the fluctuating annual estimated revenue generated per take rate. 

![image](https://user-images.githubusercontent.com/123096758/230659085-2cdc571b-34f0-46a7-9a43-613bbf9a610d.png)

The trend noticed in the “Total annual estimated revenue” graph is similar to that of the chart representing the total annual estimated revenue from the drivers. It shows an upward trend and reaches its peak value of $805,755 when the take-rate is set at $6/ride. The value then significantly declines once the take rate is greater than $6/ride. 

Based on the analyzation of what the total annual estimated revenue is forecasted based on the experimental take rates, I would recommend to setting the take rate to the current value of $6/ride. In order to align with the company’s ultimate goal of maximizing net revenue over a period of 12 months, the company will see its maximum estimated revenue when the take rate is set to a value of $6/ride. By maintaining a steady take rate, the company will see its maximum revenue generated increase as the number of users on both sides of riders and drivers increase as well. 

## References

- [Lyft Pricing Model](https://github.com/junjameshan/toledo_lyft_drivers_pricing/tree/main/pricing_model)
- https://creatingvalue.substack.com/p/real-problems-we-tackle-pricing-level 
-	https://tradecollege.org/careers/taxi-drivers-and-chauffeurs/ohio-us/
-	https://worldpopulationreview.com/us-cities/toledo-oh-population
-	https://worldpopulationreview.com/us-cities/ann-arbor-mi-population
-	https://worldpopulationreview.com/us-cities/detroit-mi-population 
-	https://www.toledoblade.com/local/2016/01/20/Traffic-up-at-local-airport-in-15.html 

























