# Introduction
Employee departure is a natural part of the workforce lifecycle. While some are involuntary due to terminations and layoffs, many employees also quit on their own accord. This is a concern to a company because recruiting, hiring and training employees take money, time and effort. As highlighted in studies on employee retention, several factors contribute to why employees leave, including financial incentives, career development opportunities, and supportive work environments.

In our project, we want to explore why an employee might leave the company and focus on using quantifiable predictor variables to predict whether an employee will leave the company. These findings might be able to reduce workload on HR and keep employees longer in the company by ensuring their satisfaction with their job and the company.

# Method
We will begin by splitting the data into training and testing sets. The training set is used to train our model and testing set will be used as an evaluation metric for the model we built. Feature selection with the backward selection algorithm will be implemented to optimize our model. Based on our results, we will be able to build our model with the condensed variables.

We will be building a logistic regression model with our training set. Logistic Regression is appropriate as it is designed for modelling binary outcomes and specifically, we are trying to predict our target variable, LeaveOrNot, which is a binary categorical variable. Hence, by using logistic regression, we are able to model the probability of LeaveOrNot as a function of our predictor variables.

# Discussion
Summary of Findings and Implications
The analysis explored factors associated with employee retention using logistic regression. Significant predictors for whether an employee leaves or stays with the company included Education, Joining Year, City, Payment Tier, Age, Gender, and Ever Benched status. Key observations include:

Age: Younger employees (20-30 years) are more likely to leave, suggesting that career growth or other opportunities might be attractive for this demographic, or just a current trend in youngsters to switch between companies.

City: Employees in Pune had a higher likelihood of staying, possibly reflecting regional differences in work culture or job availability.

Gender: Female employees demonstrated slightly higher retention rates, potentially reflecting satisfaction with workplace policies.

Payment Tier: Employees in payment tier 2 have a higher retatention rate ,while employees in payment tier 3 surprisingly were the most likely to leave. This suggests that individuals in higher-paying roles might be more attractive to the industry, offering them greater career mobility and options due to their expertise and salary levels.

Education: Employees with a Master's degree were more likely to stay with the company, while those holding a PhD were more inclined to leave. This trend appears to be connected to payment tiers, as individuals with higher levels of education, such as PhDs, might expect greater compensation or career opportunities elsewhere, potenially leading to a higher rate of turnover. On the other hand, Master's degree holders may find their current positions more aligned with their expectations and career goals, contributing to better retention.

Joining Year: Employees who joined before 2018 had a higher likelihood of leaving, and those who joined in 2018 tend to stay with the company. This suggests a possible shift in company culture or policies improving retention in later years.

The final model achieved around 80% prediction accuracy, which underscores the model's robust ability to differentiate between employees likely to stay or leave. This strong performance was consistent across different variable selection methods (Cp, BIC and full model), indicating that the chosen predictors reliably influence retention.

These findings are crucial for tailoring retention strategies, such as focusing on younger employees for engagement programs, providing competitive pay, and addressing location-specific challenges.

Alignment with Expectations
The results were mostly aligned with expectations, but there was unexpected findings regarding payment tiers, city as well as gender and employee retention.

Payment Tier and Retention: Contrary to the intuitive notion that higher payment tiers correlate with higher retention, the analysis revealed that employees in payment tier 3 were more likely to leave. This was surprising, as a previous study (Sorn, Fienena, Ali, Rafay, & Fu, 2023) suggest that higher payment tiers are typically associated with increased job satisfaction and retention. This article highlights that competitive pay is a strong predictor of employee retention, with those in higher-paying roles often staying longer. However, the result in this analysis suggests that employees in higher payment tiers might be more sought after by the industry, having more opportunities elsewhere due to their experience and skillset, leading them to leave for better offers. This warrants further exploration to understand the dynamics better.

Regional Differences in Retention: The unexpected finding that employees in Pune had higher retention rates points to potential regional differences in workplace culture, job availability, or economic factors. Further investigation into these regional dynamics could shed light on how location impacts employee loyalty and retention.

Gender and Retention: The observation that female employees had slightly higher retention rates was also surprising, as it contrasts with broader industry trends, where gender retention gaps often favor male employees. This could indicate that the company's workplace policies may be more supportive of female employees, contributing to higher satisfaction and retention. Further analysis of company policies and practices would be helpful to understand this trend fully.

# Improvements
A potential improvement that can be made to our model is addressing the class imbalance by applying certain techniques to our dataset to either increase the minority class or decrease the majority class. As seen in our EDA, the Education variable faces class imbalance where there are much more Employees with a Bachelors education compared to Masters or PHD. This poses a challenge as our model might have become biased towards employees with the highest education level of Bachelors. Moreover, for employees with Masters and PHD, the model might have not learned meaningful patterns in the data due to lack of examples, hence underfitting of the model for employees with those education categories.

Another potential improvement that can be made to our model is including the interaction term of certain covariates in our dataset. Although our EDA is quite extensive, we did not cover all combinations. This limitation means that we might have overlooked cases where the effect of a variable is dependent on another variable. Being able to point out this dependency and include it as an interaction term may have improved our model.

## Future Questions
From our model, several future research questions for exploration arises, such as

Can the model accurately predict long-term turnover patterns in this company?
Will the model be able to generalize well to the entire population?
How do external factors like economic conditions or how well a company is performing can impact employee turnover?

## Citations
Elmetwally, T. (2020). Employee dataset [Data set]. Kaggle. https://www.kaggle.com/datasets/tawfikelmetwally/employee-dataset/data
Sorn, M.K., Fienena, A.R.L., Ali, Y., Rafay, M. and Fu, G.H. (2023) The Effectiveness of Compensation in Maintaining Employee Retention. Open Access Library Journal, 10, 1-14. doi: 10.4236/oalib.1110394.
