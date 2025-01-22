# Introduction
Employee departure is a natural part of the workforce lifecycle. While some are involuntary due to terminations and layoffs, many employees also quit on their own accord. This is a concern to a company because recruiting, hiring and training employees take money, time and effort. As highlighted in studies on employee retention, several factors contribute to why employees leave, including financial incentives, career development opportunities, and supportive work environments.

In our project, we want to explore why an employee might leave the company and focus on using quantifiable predictor variables to predict whether an employee will leave the company. These findings might be able to reduce workload on HR and keep employees longer in the company by ensuring their satisfaction with their job and the company.

# Method
We will begin by splitting the data into training and testing sets. The training set is used to train our model and testing set will be used as an evaluation metric for the model we built. Feature selection with the backward selection algorithm will be implemented to optimize our model. Based on our results, we will be able to build our model with the condensed variables.

We will be building a logistic regression model with our training set. Logistic Regression is appropriate as it is designed for modelling binary outcomes and specifically, we are trying to predict our target variable, LeaveOrNot, which is a binary categorical variable. Hence, by using logistic regression, we are able to model the probability of LeaveOrNot as a function of our predictor variables.
