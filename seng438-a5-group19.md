**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group 19 |
|-----------------|
|       Liam Brennan          | 
|        Ethan Bensler         | 
|           Andrew Duong      |   
|          Joseph Duong     |  

# Introduction:

This lab aims to assess software reliability through the use of external testing tools. The two main methods of assessing software reliability is through the use of Reliability Growth Testing and Reliability Demonstration Charts. The tools we used were C-FSRAT and RDC-11.

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

# A discussion on the advantages and disadvantages of reliability growth analysis

Advantages:
- Graphs produced through reliability growth analysis are able to show any time-dependent trends. This allows for data driven decision making to take place as reliability growth curves are able to make predictions about the future of data based on its current values.
- By having a model be able to predict how data should change over time, it also allows for identification of changes that made significant altercations. The reliability growth curve predicts how the data should behave, and so when data deviates from that, reliablity growth curves make it easy to identify the change that took place to cause that unexpected altercation of the data.
- In the development of a product or system, reliability growth analysis can allow for early detection of bugs or weaknesses in the system. In the long run this early detection system can prevent expensive failure later on.

Disadvantages 

 - Real world data tends to be very complex, and mathematical models aren't always able to accurately model that complexity.
 - The accuracy of the reliability growth curve is very highly dependent on the accuracy of the failure data that the model is given. If the failure data is incomplete, inaccurate, or generally of poor quality, the reliability growth curve may produce misleading results.
 - Reliablity growth analysis is trained off of current failure data, however systems may be able to fail in other ways later on as the system progresses. Reliablity growth analysis can't anticipate these changes particularly well due to limitations of the data it's trained on. 

# Reliability Demonstration Chart Testing:

# 3 plots for MTTFmin, twice and half of it for your test data:

MTTFmin = 1.45

RDC for MTTFmin * 2: ![doubleMTTF](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/113631518/9ff49680-9508-41d5-8bfe-efa85ed1f905)

RDC for MTTFmin * 0.5: ![halfMTTF](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/113631518/45d3ca13-5dab-41be-9691-f1cdada2bd9c)

RDC for MTTFmin: ![MTTF](https://github.com/seng438-winter-2024/seng438-a5-Ruvaakaan/assets/113631518/95ae0859-ac6b-415f-b801-225645ede51a)

# Explain your evaluation and justification of how you decided on MTTFmin:

To get the MTTFmin, we first calculated the MTTF of the data we used, doing so resulted in 16/11 = 1.45. This then became our anchor point and we tested different MTTF's on either side of this number and seeing the acceptability of the failure points overall. In the end we decided to keep the MTTFmin at 1.45 as it generally acceptable although some testing is needed. Additionally, from the chart above, we see that the data points generally line up between the acceptable and need testing region. The main reason for our choice is that although we can achieve a more acceptable SUT if we lower the MTTFmin, it does not mean the overall system is better. From seeing the MTTFmin that has been set to half, we see that all the points are within the acceptable range, however, by setting the MTTF to about 0.725, it means we are expecting the system to have atleast 1 failure per week (the measurement for this dataset) which may not be acceptable. This is the tradeoff when dealing with the MTTF as we should pick a value that correctly identifies the reliability of the system while also keeping the expectations realistic.

# A discussion on the advantages and disadvantages of RDC:

RDC facilitates efficient analysis of a system's reliability in terms of both time and cost. As outlined in the slides, it's important to note that RDC cannot precisely quantify the reliability of the system under test (SUT). Instead, it serves as a suggestion or indication regarding the acceptability of the SUT's reliability.

# Comparison of Results from Part 1:

Reliability Growth Testing is done to analyze the current reliability of a system. By having a model that can predict future data trends, it can aid in the development of a system as measured values deviate from the expected data trends. Measuring progress in this way allows for resources to be directed to achieve reliability goals in an efficient manner. Should failures occur, it can be detected through this method and resources can be allocated to fix the problem.

A Reliability Demonstration Chart is typically completed towards the end of the Reliability Growth Testing period. By taking collected failure data and plotting the observed failure rate of a system over time, developers can assess whether a system is on track to meet its reliability goals, and what actions should be taken based off of the current percieved reliability. During times when reliability demonstration charts are made, software updates are typically limited to critical updates or minor bug fixes, while large changes that can introduce new failure modes are discouraged at this point in the development stage.

# Discussion on Similarity and Differences of the Two Techniques:

Both Reliability Growth Testing (RGT) and Reliability Demonstration Chart (RDC) Testing aim to evaluate the reliability of a system through the analysis of failure data over time, utilizing statistical tools to make informed decisions regarding the system's reliability and its potential risks. However, while RGT primarily focuses on assessing the improvement in reliability over time during the development phase, RDC Testing is typically conducted towards the end of the development process to demonstrate that the system meets reliability requirements before deployment or release. This distinction highlights the timing and context in which each method is employed, despite their shared goals and methodologies.

# How the team work/effort was divided and managed:

The Reliability Growth Testing segment of the assignment was undertaken by Andrew and Liam, while Ethan and Joseph took charge of the Reliability Demonstration Chart component in the lab. Although we primarily worked in pairs, we maintained open communication throughout the process, assisting each other with any challenges encountered along the way.

# Difficulties encountered, challenges overcome, and lessons learned:

**Failure Data:**

Converting the failure data into the appropriate format required for reliability testing tools proved to be a challenging endeavor. The dataset utilized for C-SFRAT analysis is sourced from the CDS.DAT file. Despite our thorough search, we were unable to locate any pertinent information regarding the covariates E (execution time measured in hours), F (failure identification work measured in person hours), and C (computer time failure identification measured in hours) within the provided failure data. Consequently, we opted to solely incorporate "None" as a covariate for assessing the models' performance. 

**Reliability Growth Testing:**

The reliability growth testing posed challenges, particularly when we were given the option to utilize either SRTAT or C-SFRAT for comparing the predictiveness of the models. Despite exploring SRTAT, we found it lacking in providing meaningful insights for comparing the models effectively. Consequently, we opted for C-SFRAT. However, another obstacle arose when determining which specific plots were required based on the assignment description. This presented a significant challenge, as the assignment description seemed to require more types of plots than C-SFRAT could accommodate. After consideration, we ultimately concluded that the two plots effectively captured the predictability of the failure data.

**Reliability Demonstration Chart:**

For this assignment, we used the RDC-11 EXCEL worksheet. Initially we planned to use the SRTAT to create the RDC but we opted to use RDC-11 instead as SRTAT seemed to lack the function to create charts with different MTTF's. Using RDC-11 was challenging as there are a lot of things that are unclear or confusing even after reading the documentation. Additionally it was found to be extremely challenging to modify the limits of the boundaries as it caused a lot of errors and did not work as expected, which is further worsened by the lack of proper explanation of the software. As it appeared impossible to scale the chart properly, we opted to instead minimize our points of data and were more selective with the dataset we used to avoid extending past the bounds. Doing so still provides the correct information about the data and is still a good sample of the overall failure data.

# Comments/feedback on the lab itself:

This lab proved to be exceptionally challenging due to the lack of explanation regarding the functionality of the tools and how they could be effectively utilized. The primary hurdle was encountered during the process of converting the failure data into the correct format. Moreover, the other failure data files provided seemed to have no discernible correlation, making it impossible to augment our selected failure data by referencing them. It appears that this lab, like many other components of the course, is in need of updating. Additionally, many of the tools featured in this lab lacked adequate documentation and were challenging to navigate. We believe that a comprehensive update or overhaul of these tools would greatly enhance the lab's comprehensibility and our overall learning experience.
