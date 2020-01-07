# Social Media Analytics: Detect Food Trends from Facebook Posts

Download: [Data](https://drive.google.com/file/d/1xlWqW9I9qnxXmnjiwnTpE9Qk92JCkLua/view?usp=sharing) | [Handout](https://github.com/chriskhanhtran/facebook-detect-food-trends/blob/master/handout.pdf)

<img src="https://raw.githubusercontent.com/chriskhanhtran/chriskhanhtran.github.io/master/images/fb-food-trends.png"/>

In order to detect emerging trends of food consumption from social media data, I employ two simple methods:

- In the first method, I creat **word counts** of each ingredient mentioned in Facebook posts from 01-2015 to 12-2015. For each month, I look at the most mentioned ingredients, then I plot the trend of these ingredients being mentioned over time to detect abrupt changes in the time series. However, with this method, I can only identify the trend of a single ingredient and cannot tell what ingredient it is being mentioned with. For example, I can only see the trend of **cauliflower**, however this trend has a lot of noise because **cauliflower** can be used with any other ingredients, making it hard to detect the rise of **cauliflower rice**.


- In the second method, to handle the limits of the first method, I contruct **co-occurence matrices** of ingredients and calculate **Lift** and **PPMI**. Then, I observe the top 20 ingredient combinations in each month to identify emerging food trends and then plot time-series data to validate these findings. After validating this method on **pumpkin pie**, **cauliflower rice** and **vegetable noodle**, I find it show a fast and accurate detection of food trends.
