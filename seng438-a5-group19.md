**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group 19 |
|-----------------|
|       Liam Brennan          | 
|        Ethan Bensler         | 
|           Andrew Duong      |   
|          Joseph Duong     |  

# Introduction:

NEEDS TO BE DONE

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

NEEDS TO BE DONE

# A discussion on the advantages and disadvantages of RDC:

RDC facilitates efficient analysis of a system's reliability in terms of both time and cost. As outlined in the slides, it's important to note that RDC cannot precisely quantify the reliability of the system under test (SUT). Instead, it serves as a suggestion or indication regarding the acceptability of the SUT's reliability.

# Comparison of Results from Part 1:

NEEDS TO BE DONE

# Discussion on Similarity and Differences of the Two Techniques:

NEEDS TO BE EDITED

Both Reliability Growth Testing (RGT) and Reliability Demonstration Chart (RDC) Testing aim to evaluate the reliability of a system through the analysis of failure data over time, utilizing statistical tools to make informed decisions regarding the system's reliability and its potential risks. However, while RGT primarily focuses on assessing the improvement in reliability over time during the development phase, RDC Testing is typically conducted towards the end of the development process to demonstrate that the system meets reliability requirements before deployment or release. This distinction highlights the timing and context in which each method is employed, despite their shared goals and methodologies.

# How the team work/effort was divided and managed:

The Reliability Growth Testing segment of the assignment was undertaken by Andrew and Liam, while Ethan and Joseph took charge of the Reliability Demonstration Chart component in the lab. Although we primarily worked in pairs, we maintained open communication throughout the process, assisting each other with any challenges encountered along the way.

# Difficulties encountered, challenges overcome, and lessons learned:

**Failure Data:**

Converting the failure data into the appropriate format required for reliability testing tools proved to be a challenging endeavor. The dataset utilized for C-SFRAT analysis is sourced from the CDS.DAT file. Despite our thorough search, we were unable to locate any pertinent information regarding the covariates E (execution time measured in hours), F (failure identification work measured in person hours), and C (computer time failure identification measured in hours) within the provided failure data. Consequently, we opted to solely incorporate "None" as a covariate for assessing the models' performance. 

**Reliability Growth Testing:**

The reliability growth testing posed challenges, particularly when we were given the option to utilize either SRTAT or C-SFRAT for comparing the predictiveness of the models. Despite exploring SRTAT, we found it lacking in providing meaningful insights for comparing the models effectively. Consequently, we opted for C-SFRAT. However, another obstacle arose when determining which specific plots were required based on the assignment description. This presented a significant challenge, as the assignment description seemed to require more types of plots than C-SFRAT could accommodate. After consideration, we ultimately concluded that the two plots effectively captured the predictability of the failure data.

**Reliability Demonstration Chart:**

ADD SOMETHING HERE JOSEPH

# Comments/feedback on the lab itself:

This lab proved to be exceptionally challenging due to the lack of explanation regarding the functionality of the tools and how they could be effectively utilized. The primary hurdle was encountered during the process of converting the failure data into the correct format. Moreover, the other failure data files provided seemed to have no discernible correlation, making it impossible to augment our selected failure data by referencing them. It appears that this lab, like many other components of the course, is in need of updating. The creation dates and last modified dates of several files indicate that they are approximately 20 years old or even older. This outdated content does not accurately reflect the current state of reliability testing practices, putting students at a disadvantage. Additionally, many of the tools featured in this lab lacked adequate documentation and were challenging to navigate. We believe that a comprehensive update or overhaul of these tools would greatly enhance the lab's comprehensibility and our overall learning experience.
