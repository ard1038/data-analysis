# Exploratory Data Analysis: Will the Customer Accept the Coupon?

Inspired by the ***CRISP-DM*** data analysis framework, the following summary uses statistical analysis and visualizations to explore the viability of a new business opportunity, to suggest if further investment is worthwhile to further mature the opportunity.

## 1 Business Understanding

Imagine driving through a town, and a coupon is delivered to your cell phone for a restaraunt near where you are driving. 
* Would you accept that coupon and take a short detour to the restaraunt?
* Would you accept the coupon but use it on a sunbsequent trip? 
* Would you ignore the coupon entirely? 
* What if the coupon was for a bar instead of a restaraunt?
* What about a coffee house? 
* Would you accept a bar coupon with a minor passenger in the car? 
* What about if it was just you and your partner in the car? 
* Would weather impact the rate of acceptance? 
* What about the time of day?


### 1.1 Background

ADCo, a company specializing in distributing physical coupons for its local, small/medium business advertisers ("SMB"), is evaluating a new *digital* coupon revenue model. They seek to create a digital coupon serving platform which targets and delivers a relevant digital coupon to a vehicle's driver ("driver" or "customer") through a mobile application, as they are driving proximate distances to one of their SMB's business locations. Before significantly investing to build this new revenue model (mobile application, middleware, infrastructure, product marketing, etc), ADCo has smartly solicited a survey to gather key information that can be investigated statistically to offer insights into it's viability.

### 1.2 Business Goals and KPIs

From an exploration of the survey data, the Company is keen to understand:
* What are the factors that determine whether a driver accepts the coupon once it is delivered to them?
* How would you determine whether a driver is likely to accept a coupon?
* Are there any types of drivers we could target to encourage a higher coupon acceptance rate?

> *Presumption:* The Company's technology is capable of sending/notifying a driver's cellphone a coupon offer through their mobile appto a business in proximity to their current location.

### 1.3 Data Mining Goals and KPIs

#### 1.3.1 Data
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).

## 2 Data Understanding
## 3 Data Preparation
## 4. Conclusions and Findings
## 5. Next Steps
* **Interpolating Missing Data:**
   * Seek any additional data/correlations to interpolate values for `car`
   * Can the missing data for visits (`CoffeeHouse`, `Restaurant20To50`, `CarryAway`, `RestaurantLessThan20`, `Bar`) be interpolated some correlative means, as statistical interpolation would not be appropriate for the categorical values (converting category values to numerical representation would be incorrect, based on the implied ranges)
* **Consider Legislative/Regulation Adherence:**
   * Review any existing laws within each geographical region this coupon product would target a driver, e.g. [US' "Distracted Driving | Cellphone Use" laws](https://www.ncsl.org/transportation/distracted-driving-cellphone-use#:~:text=Hand%2Dheld%20cellphone%20use%20ban,hand%2Dheld%20cellphones%20while%20driving. "Source: ncsl.org"), indicating 29 states/regions prohibit the use of cell phones while driving
   * Consider adjusting *geo-fencing* whitelist/blacklist to comply with any discovered restrictions, as we can infer it unlikely for a solo driver to *legally* act on a coupon notification while driving. Is there a means to know if the recipient is a non-driver, and therefore may more readily see the coupon offer in a timely manner?
* **Ethnographic Influences on Coupon Targeting:** 
   * While target regions for the survey was not indicated in the dataset provided, anonymized **ethnographic information or preferences by region** may be available through other datasets to explore how it may encourage greater coupon acceptance.  
   * For example, a driver known to reside in an area with a high Muslim population (or potentially self-identifies as Muslim) would be inlikely to accept a coupon to a bar.