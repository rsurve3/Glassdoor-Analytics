# Glassdoor-Analytics
 
**Introduction:**

As a direct response to the present status of the global economy, the vast majority of companies have reached their absolute lowest level of hiring ever recorded. The recruiting process is difficult for everyone, but in today's economy, it is particularly difficult for recent grads who are looking for their first employment.
When someone is searching for their first job, the employment websites they use aren't always as useful and versatile as they may be. When we check for a certain employment position on these websites, we find that not all the job needs and specifications for that role are the same, despite the fact that the roles may have the same name. As a direct consequence of this, the students get confused. In addition to that, this will create an issue all the way through the interviewing process.
Because there are such vast differences in the wages given by various companies, people often feel confused when discussing their pay, particularly if it is their first work. This is especially true for those who are looking for their first employment. Within the scope of our project, we will prioritize addressing issues of this kind.
We will be working on one such job listing website – Glassdoor, as part of our project. It is a website where companies may publish their job opportunities along with the essential information, users can offer their thoughts on a specific position or firm, and workers can look at evaluations and make job searches on the platform. With the use of this data, we will be able to determine which companies are advertising which job titles, the pay rates that relate to those job titles, and the overall geographic distribution of needs throughout the country.

**Research Questions:**

The following areas are researched as part of our project to help us understand the diversity of jobs and corresponding variables and details:
1.	Annual Salary based on Job Title
2.	Sentiment Analysis on Reviews
3.	Salary Distribution across different states
4.	Variation of job salaries based on different factors (company rating, seniority, skills required, etc.)
5.	Word cloud on job description

**Data Analysis:**

**Feature Extraction:**

Using Beautiful Soup, we extracted data from the Glassdoor Website. We used libraries like plotly, Seaborn, NumPy, pandas, spacy, request, time, and re. The extracted data required extensive data cleansing after that. As was expected, not every business abides by the rules and posts all the data. Sometimes the city or even the state was not mentioned in the location of the company. Most companies disclose their pay in one of four ways: annual salary ($52K), annual salary in the range ($52K - $73K), hourly compensation ($25), or hourly salary in the range ($25 - $35). After data processing, all the aforementioned parameters were enforced for consistency. Extracted data contained job listings from various companies like Accenture, American-Express, Apple, Barclays, Cisco-Systems, Citi, Deloitte, EY, Goldman-Sachs, Google, IBM, Morgan-Stanley, etc.

![image](https://user-images.githubusercontent.com/122759737/214108974-eee30f90-e3f5-4799-aa0e-49ab647ad0db.png)

 
**Exploratory Data Analysis**



**Average salaries distribution throughout US states**
 
![image](https://user-images.githubusercontent.com/122759737/214109222-6cea4f5c-f1da-46ee-a853-2b83c116c711.png)

Virginia state has the highest average annual salary. The states with the lowest average annual salaries are Tennessee and North Carolina. 

**Annual Salaries of the top 10 job**s 
 
![image](https://user-images.githubusercontent.com/122759737/214109262-53795507-ead4-4837-99d9-2454034ba22e.png)

The above figure shows the annual salaries of employees with respect to their job descriptions. The job title Senior Blockchain Data Analyst has the highest annual salary of more than $275k based Washington D.C.

**Annual Salaries of the bottom 10 jobs**
 
![image](https://user-images.githubusercontent.com/122759737/214109381-a8b91471-d798-439a-a19e-ef3e2fd59638.png)
 
This graph depicts 10 job titles having the least annual salaries. Here, we can see that Finance Analyst has the lowest salary below $10k.

**Job availability throughout different cities of US states**

![image](https://user-images.githubusercontent.com/122759737/214109433-f844ea95-a370-4a56-b348-08753c577770.png)

This plot depicts cities which have highest paying job titles. We can conclude that Washington D.C. has highest paying Analyst job titles.

**Annual Salary Distribution**

![image](https://user-images.githubusercontent.com/122759737/214109526-a7ed2775-85d2-463b-9365-26af1b417bbd.png)

By looking at this figure we can see that most of the salaries are distributed between $50k and $100k and just one salary above $250k.

**Annual salaries with respect to US states**
![image](https://user-images.githubusercontent.com/122759737/214109574-cb119d5f-ce97-410c-b505-f8b6cb28df45.png)
 
This histogram shows the job availability along with the salary distribution with respect to the 17 states of United States.

**Word Cloud**
![image](https://user-images.githubusercontent.com/122759737/214109623-925d6b6b-e0c5-41be-bae7-c6e7eefb44ba.png)

 
Word Cloud shows the highest frequency of word occurrence. We can determine that words like Business, Data and Technical have the highest frequency of searches.

**Pie Chart**
![image](https://user-images.githubusercontent.com/122759737/214109758-101c6159-8f04-4ddd-90ce-39fe133ccb90.png)
 
After Web scraping the availability of jobs on glass door throughout 17 states of United States, we can determine the highest and the lowest availability of jobs in each state in the pie chart.

**Polarity Plot**
 
![image](https://user-images.githubusercontent.com/122759737/214110788-d615ec2a-b896-432e-84be-607aae307c86.png)


From the polarity plot, we can determine that most of the reviews are positive.

**Subjectivity Plot**
 
![image](https://user-images.githubusercontent.com/122759737/214110815-8e8447e3-6492-4567-8899-5d2a1b045ad2.png)
 
From the subjectivity plot, we can determine that majority of the reviews are fairly subjective.

**Model Selection:**

Data is used in predictive analytics to foretell future trends and occurrences. Salary Prediction falls under the category of predictive analytics since it makes use of past data to foresee prospective situations that may aid in the direction of strategic choices. We have employed the linear regression, lasso regression, and random forest regressor algorithms, which are some of the finest ones for predictive analytics.

1.	Lasso Regressor: A kind of linear regression that makes advantage of shrinkage is called lasso regression. When data values shrink toward a middle value, such as the mean, this is called shrinkage. Simple, sparse models are encouraged by the lasso approach (i.e. models with fewer parameters). 

2.	Linear Regressor:  A variable's value can be predicted using linear regression analysis based on the value of another variable. The dependent variable is the one you want to be able to forecast. The independent variable is the one you're using to make a prediction about the value of the other variable.


3.	Random Forest Regressor: Multiple decision trees can be used in Random Forest, an ensemble approach, to complete both classification and regression problems. This method's fundamental principle is to integrate several decision trees to get the final result rather than depending just on one decision tree. 

**Model Comparison:**
We have used 3 different models for Salary Prediction. 
1.	Lasso Regressor
2.	Linear Regressor
3.	Random Forest Regressor

The term "regression" refers to challenges in predictive modelling that include making a prediction about a numerical value. It is not the same as classification, which includes making a guess on the label for a class. In contrast to classification, we are unable to utilize the accuracy of classification to assess the accuracy of predictions provided by a regression model.  Instead, we need to make use of error metrics that have been purpose-built for the evaluation of predictions produced based on regression issues.
Common error metrics used to evaluate and report the performance of a regression model is:
Root Mean Squared Error (RMSE).
The Root Mean Square Error (RMSE) is another name for the Root Mean Square Deviation. It considers the deviations from the real value and calculates the average size of the mistakes that have occurred. A RMSE score of 0 shows that the model provides an accurate representation of the data. The model and its predictions are of higher quality when the RMSE is smaller. If the RMSE value is high, it suggests that there is a significant gap between the residual and the ground truth. The root mean square error (RMSE) is a metric that may be used with a variety of features since it assists in determining whether the feature is contributing to an improvement in the model's prediction.
Values of RMSE that fall between the range of 0.2 and 0.5 are indicative of a model's ability to reasonably predict the data.
Accuracy of a regressor model can also be computed by calculating product of 1.96 and RMSE value for that model.
After analyzing the RMSE values for the three models, we can infer that Random Forest Regressor has the highest accuracy among the three.

**Result Analysis:**
1. Sentimental Analysis
 
![image](https://user-images.githubusercontent.com/122759737/214110884-8a5c5f96-6470-420a-8730-be384e14cc3b.png)
 
 
This histogram depicts comparison between polarity of two companies, Apple and American Express. (Blue – American Express, Red – Apple). Positive polarity of reviews of Apple is higher than that of American Express. Thus, we can say that Apple has better reviews than American Express from the employee perspective.
 
![image](https://user-images.githubusercontent.com/122759737/214110942-5ecb62a2-623c-40b3-b94f-6dd2f39cfdf8.png)
 
 
With the successful implementation of our model, we can now conclude which companies have the most satisfied employees and good work environment Moreover, we can also determine companies with the least satisfied employees Out of all the companies, Apple has the highest sentiment with 0.33. Thus, we can say that Apple employees are most satisfied with their companies. Now, EY has the lowest sentiment with 0.23. This means, EY employees are least satisfied with their companies.

2. Salary Prediction

![image](https://user-images.githubusercontent.com/122759737/214110968-27456e42-7978-426b-9d2f-1c3f755e123a.png)
 

As seen in the code above, all the user has to do is input their job requirements in the highlighted part,
1.	Which Industry they want to work in?
2.	How should the company be owned? (Public, Private, NGO, Government, etc.)
3.	What job title they want?
4.	Level of seniority of the job
5.	The skills and tools they want to work with as a part of the job

Once the user has specified their requirements, our model shows the annual salary the user should expect by comparing data of all the job listings which we have extracted and trained the model with,

![image](https://user-images.githubusercontent.com/122759737/214110997-a2221f35-17fa-497a-a894-544bd47087ed.png)


As seen in the code above, our model gives the estimated salary in the highlighted part.
We might be able to see a job's salary on the standard Glassdoor website. But what our model accomplished was it enhanced the system so that the user could estimate their expected wage based on several input criteria.
Recent graduates often worry during interviews about their inadequate understanding of the expected income. They might be paid insufficiently in some circumstances because of their inexperience. They will benefit from our model in these circumstances.

**Limitations:**
In our project, we have trained our model in such a way that it should be beneficial for the user before going to an interview. The inputs like skills required is totally dependent on the user. The user can decide whatever the skills they” want to work on. However, we haven’t included a scenario where we checked if the user would actually be able to work for the skills they have searched for. 
For example, if the user searched for python as a skill requirement in their job search, we haven’t cross checked whether they are comfortable working in python or not. To include that, we need to work on the user’s resume as well.
Additionally, the Glassdoor website is always being updated and improved. It is challenging to extract data in real time since the classes change so frequently. It is inconvenient to have to check all the classes on the website before executing the code each time data needs to be extracted.

**Future Work:**
Our next action will be to remove the limitation we mentioned before. To do this, we'll begin by gathering resume datasets. After each resume has been cleaned and processed, we will compare it again with the job description. With the addition of this functionality to our model, we would also be able to advise the user on the skills they should utilize in their job search to increase their chances of landing a position.


