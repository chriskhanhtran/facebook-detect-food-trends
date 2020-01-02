# Social Media Analytics: Detect Food Trends from Facebook Posts

Download: [Data](https://drive.google.com/file/d/1xlWqW9I9qnxXmnjiwnTpE9Qk92JCkLua/view?usp=sharing) | [Handout](https://github.com/chriskhanhtran/facebook-detect-food-trends/blob/master/handout.pdf)

<img src="https://raw.githubusercontent.com/chriskhanhtran/chriskhanhtran.github.io/master/images/fb-food-trends.png"/>

In order to detect emerging trends of food consumption from social media data, I employed two simple methods:

- In the first method, I creat **word counts** of each ingredient mentioned in Facebook posts from 01-2015 to 12-2015. For each month, I look at the top mentioned ingredients, then I plot the trend of these ingredients being mentioned over time to detect abrupt changes in the time series. However, with this method, I can only identify the trend of a single ingredient and cannot tell what ingredient it is being mentioned with. For example, I can only see the trend of "Cauliflower," however this trend has a lot of noise because "Cauliflower" can be used with many other ingredients in different recipe, making it hard to detect the rise of "Cauliflower Rice."


- From the limit of single-word-count method mentioned above, in the 2nd method, I built a **co-occurence matrix** of ingredients for each month and observed the top 50 ingredient combination. After that, I calculated **Lift** and **PPMI**. If I identify any interesting ingredient combination emerging from this analysis, I will plot time-series data of this ingredient combination to see whether it could be an emerging food trend. After validating this method on *pumpkin pie*, *cauliflower rice* and *vegetable noodle*, I found this method showed a fast and accurate detection of food trends.
