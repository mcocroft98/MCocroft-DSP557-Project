# MCocroft-DSP557-Project
Capstone project for URI's Data Science Graduate Certificate

# **Energy Consumption in the Steel Industry**

![Steel Picture](https://i.imgur.com/HLXFacj.jpg)

Mason Cocroft
Prof. Robert Coyne
DSP 557
8 February, 2022


## **Introduction & Aims**

Steel production and recycling is a very labor-intensive process. Steel products all start as ore or scrap, which is then chemically refined into usable material, and is finally shaped into the various products that today’s markets demand. The fast paced, on-demand nature of today’s markets adds another layer of intensity and variability to the steel making process. Naturally, this complex and highly in demand industry requires a significant amount of energy to meet market needs. With data from an anonymous Korean steel firm supplied by the Korean Electric Power Corporation, this project aims to most accurately predict a steel firm’s energy output for any given 15-minute interval in the year 2018. 

## **Methods**

The primary method to be used in this project is a regression algorithm. The primary packages to be used in Python will be sci-kit learn and pandas. The *train_test_split* function from sci-kit learn will be used to split the samples into training and test sets. The training set will contain 80% of the data, and the test set will contain 20% of the data. The target variable for this project is total kWh used for each sample. Each sample is a 15-minute time period during the year 2018, labelled by the time and date column. The variables from the original data set being used to predict kWh usage include: day of the week, whether weekend or week day, size of the load of steel, CO2 emissions, number of seconds since midnight, and leading and lagging current measurements. In addition, variables to be used in the prediction will be added for whether or not it’s the rainy season, which of the four seasons it is (spring, summer, winter, fall), whether it is a Korean holiday (no holiday, minor holiday, or major holiday) and what shift of the workday it is (first, second, or third). The regression may be run multiple times featuring only specific sets of variables, for instance removing the lagging and leading current data to see what change in accuracy there is, or removing all but the date-related variables 

## **Outcomes**

The primary outcome of this project would be the prediction accuracy on total kWh usage. The secondary outcomes will be the prediction accuracy on total kWh usage given certain combinations of features. When determining which regression model is most appropriate for this project, model accuracy will be measured using score from metrics in sci-kit learn. The selected model’s performance will be further evaluated using mean absolute error, mean squared error, and root mean squared error, each calculated with functions from metrics in sci-kit learn.

## **Implications**

The price of steel is constantly fluctuating due to various market circumstances. For the company I will be working for price quotes are regularly honored for only a 24-hour period before a new quote would need to be created for a potential customer. This fluctuating price is brought on by many factors, including things like tariffs, freight obstruction, changes to the labor market, and many other things. One more variable that would need to be accounted for in overhead costs would be total energy consumption and cost. Being able to accurately predict how much energy the company will be using when given a certain set of variables will help in creating a strategic pricing plan that accounts for the cost of energy. Cost of energy itself is not present in this data, but being able to predict total kWh usage is equally as good a measurement, as total usage and cost go hand in hand. The more accurately the price reflects the energy consumed in creating the steel products, the less of an effect any overhead costs would have on the company.

In terms of ethical implications, there are no implications for using this specific data as it is made publicly available through Kaggle. Trying to apply any of the findings or models of this project to another company, whether Korean or American, could cause some ethical issues. Firstly, the Korean steel industry will have some innate differences with the American steel industry, largely due to cultural differences. Differences in work hours, work culture, how the steel is acquired and shipped, how the consumed energy is created (hydroelectric, natural gas, coal, oil), etc. all play a part in making the two industries unique from each other, and those types of non-quantifiable or unavailable variables must be taken into consideration when attempting to cross any findings of this project over. Secondly this data is pre-COVID. Applying it now three years into the COVID pandemic is likely unwise due to significant changes in the global economy, massive disruptions to the workforce, as well as the different handlings of the pandemic by the two different countries. This data was the most recent data readily available online, but there is a chance it is already outdated, which would only be known by comparing it to more modern data which is currently not available. This should be kept in mind as long as additional data remains unavailable.
