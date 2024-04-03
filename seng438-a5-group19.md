**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group 19 |
|-----------------|
|       Liam Brennan          | 
|        Ethan Bensler         | 
|           Andrew Duong      |   
|          Joseph Duong     |  

# Introduction:

# Reliability Growth Testing:

# Result of model comparison (two top models):

![model-results-graph](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/95046408/8ac5b245-95a8-4f0d-9b68-7a8560aab430)

![model-comparison-logs](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/95046408/1aa5b230-adea-4166-ab8e-b538929c9e63)

The graph and table above clearly demonstrate that the Truncated Logistic (TL) and IFR Generalized Salvia & Bollinger (IFRSGB) reliability models outperform others in fitting the failure data, thereby offering more accurate predictions for variables such as time to release and remaining failures. Moreover, their Log-Likelihood scores, notably -137.074 for the TL model and -137.030 for the IFRSGB model, exceed those of alternative models, providing further evidence of their effectiveness.

The dataset utilized for C-SFRAT analysis is sourced from the CDS.DAT file. Despite our thorough search, we were unable to locate any pertinent information regarding the covariates E (execution time measured in hours), F (failure identification work measured in person hours), and C (computer time failure identification measured in hours) within the provided failure data. Consequently, we have opted to solely incorporate "None" as a covariate for assessing the models' performance.


# Result of range analysis (an explanation of which part of data is good for proceeding with the analysis):

![plot-no-lines](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/95046408/38275339-7b97-44cf-a8b2-c3a9a19a95d5)

The plot above reveals a downward trend in the number of failures within the system as time progresses. Although there is a slight uptick in failures at time = 35, subsequent observations suggest a diminishing likelihood of future failures. This trend indicates a decreasing risk of system failures as time advances.

# Plots for failure rate and reliability of the SUT for the test data provided:

![plot](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/95046408/f5aeffa5-dc6d-4a5b-b5b0-346e165cf969)

# A discussion on decision making given a target failure rate:

When making decisions based on a target failure rate, it's important to carefully assess the reliability and performance of the system or product under consideration. The target failure rate serves as a benchmark against which the observed failure rate is compared. If the observed failure rate falls within the acceptable range defined by the target failure rate, it indicates that the system is performing as expected and meets the reliability requirements. However, if the observed failure rate exceeds the target, it suggests potential issues that need to be addressed. By analyzing failure data and comparing it to the target rate, we can identify areas for improvement, through design modifications, enhanced quality control measures, or predictive maintenance strategies. Understanding the relationship between failure rates and associated costs enables informed decision-making, weighing the trade-offs between reducing failure rates and the investment required.

# Reliability Demonstration Chart Testing:

# 3 plots for MTTFmin, twice and half of it for your test data:

MTTFmin = 

RDC for MTTFmin * 2: 

RDC for MTTFmin * 0.5: 

RDC for MTTFmin: 

# Explain your evaluation and justification of how you decided on MTTFmin:

# A discussion on the advantages and disadvantages of RDC:

# Comparison of Results from Part 1:

# Discussion on Similarity and Differences of the Two Techniques:

# How the team work/effort was divided and managed:

# Difficulties encountered, challenges overcome, and lessons learned:

# Comments/feedback on the lab itself:
