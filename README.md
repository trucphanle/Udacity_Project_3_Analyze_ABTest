# Udacity_Project_3_Analyze_ABTest

This is my repository for the project and files for the third project in the Udacity Data Analyst Nanodegree program.

## Project Overview
A/B tests are very commonly performed by data analysts and data scientists. For this project, I will be working to understand the results of an A/B test run by an e-commerce website. The company has developed a new web page in order to try and increase the number of users who "convert," meaning the number of users who decide to pay for the company's product. My goal is to work through this notebook to help the company understand if they should implement this new page, keep the old page, or perhaps run the experiment longer to make their decision.

## Conclusions

For this project, our goal was to help the e-commerce company understand if they should implement the new website or keep the old page by using three different methods as follows.

1. Probability based approach
2. A/B test
3. Regression approach

##### 1. Probability based approach:

* We found that an individual received the new page with a probability of 50%, which means that there is an equal chance that an individual received the old page at the same time.
* Moreover, there is not sufficient evidence to conclude that the new treatment page results in more conversions. In fact, it is quite the opposite with a conversion rate of 12.04% for the old page and 11.88% for the new page.

##### 2. A/B test:

* In this part, we set up our hypothesis to test if new page results in better conversion or not (one-tailed test).
* We simulated our user groups with respect to conversions, computed the p_value of 0.9061 and thus, failed to reject null hypothesis. 
* By using the built-in stats.proportions_ztest we computed z-score and p-value which confirmed our earlier p-value and failure to reject null hypothesis.
* Therefore, similar to the probability based approach, we can not be confident with a 95% confidence level that the converted rate of the new_page is larger than the old_page.

##### 3. Regression Approach:

* We changed our hypothesis to test whether conversion rate of the old page is different to the conversion rate of the new page (two-tailed test).
* With logistic regression results, we computed same z-score and the p-value of 0.190.
* Then we added geographic location of the users to find if any specific country had an effect on conversion.
* The result gave a similar outlook and suggested that neither the countries nor the interations between country and landing page influenced on the conversion rate.

##### Consideration and Recommendation:

* Due to Change aversion effect, a group of users may give an unfair advantage to the older page.
* Similarly, due to Novelty effect, users may give an unfair advantage to the newer page.

* Even the duration of this experiment is only 22 days, which is quite short for the A/B testing, the sample size is very large. In my opinion, prolonging the experiment on tesing the new_page is likely not necessary. 
* Instead, I recommend this e-commerce company to focus on the development of another new landing page with more productive features.
