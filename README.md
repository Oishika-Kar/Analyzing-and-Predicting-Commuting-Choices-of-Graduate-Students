**Analyzing-and-Predicting-Commuting-Choices-of-Graduate-Students**

# Objective
We are analyzing the commuting preferences of graduate students during the winter seasonwhen only driving or taking the bus are feasible options due to severe weather conditions.This study will assist the university in optimizing parking and bus transportation needsduring the winter months. 

Additionally, we are investigating the commuting choices of graduate students in the spring,when biking and walking become viable alternatives. This research will support theuniversity in planning for car parking, bike rack availability, and bus transportation during thespring season. Moreover, the university is considering adjustments to bus routes and aimsto understand how these changes may influence students' commuting decisions.

# Data:
The analysis utilizes two datasets, both derived from simulated data on the commutingchoices of 1,000 graduate students who commute to campus from distances greater thanone mile. These datasets can be found [here](https://github.com/Oishika-Kar/Analyzing-and-Predicting-Commuting-Choices-of-Graduate-Students/blob/3652e98d42cb97087f1ec622f69a43ee31ff9546/commute_datasets.zip.zip)
Detailed descriptions of the variables in each dataset are available in the"commute_descriptions.txt" file.

**commute_binary.csv:** This dataset contains information on students' commutingchoices during the winter season, when only two options are feasible due to severeweather conditions: driving a car or taking a bus. This dataset will help the universityplan for parking and bus transportation needs during the winter months.

**commute_multinomial.csv:** This dataset includes data on commuting choices duringthe spring season, when weather conditions allow for additional options. Students canchoose from four commuting modes: driving a car, taking a bus, biking, or walking. Thisdataset will aid the university in planning for car parking, bike rack availability, and bustransportation during the spring. Additionally, the university is considering adjustmentsto bus routes and seeks to understand how these changes might influence students'commuting decisions.

# Methodology:

The methodology employed in this project encompasses a variety of modeling approaches to predict commuting choices for graduate students, thereby providing valuable insights into the factors influencing commuting behavior. By utilizing multiple estimation techniques, the project aims to offer a comprehensive understanding of commuting behavior and demonstrate the application of different methodologies in data science.

**1. Linear Probability Model (LPM):**
   - **Objective:** Predict commuting choices during winter (driving or taking the bus).
   - **Method:** Utilizes linear regression to estimate the probability of each mode of transport based on cost and time. This approach provides a straightforward interpretation of the relationship between predictor variables and the probability of choosing a particular mode of transportation.

**2. Binary Logit Model (BLM):**
   - **Objective:** Explore predictors' relationship with the probability of driving during winter.
   - **Method:** Implements logistic regression to model the binary outcome (driving or taking the bus), offering more precise probability estimates compared to the linear probability model. By modeling the probability of choosing driving versus taking the bus, this approach allows for the examination of the impact of various predictors on the likelihood of driving during winter.

**3. Multinomial Logit Model (MLM):**
   - **Objective:** Analyze commuting choices in spring (biking, walking, driving, or taking the bus).
   - **Method:** Applies multinomial logistic regression to estimate probabilities for each commuting mode simultaneously. This model allows for the assessment of the influence of predictor variables on the likelihood of choosing different commuting modes in spring, providing insights into the relative preferences for biking, walking, driving, and taking the bus.

**4. Maximum Likelihood Estimation (MLE):**
   - **Objective:** Estimate multinomial logit model parameters for deeper understanding.
   - **Method:** Constructs the likelihood function and maximizes it to estimate parameters, illustrating the theoretical foundations of MLE. By estimating parameters using MLE, this approach provides a rigorous statistical framework for understanding the relationship between predictor variables and commuting mode choices.

**5. Generalized Method of Moments (GMM):**
   - **Objective:** Estimate binary choice model parameters (driving or taking the bus) using GMM.
   - **Method:** Utilizes moment conditions from the data to estimate parameters, offering a robust estimation approach for potential endogeneity. GMM provides a flexible method for estimating parameters in binary choice models, allowing for the incorporation of instrumental variables to address endogeneity concerns and improve the accuracy of parameter estimates.

By employing these diverse modeling techniques, the project aims to provide comprehensive insights into commuting behavior and demonstrate the versatility of different estimation methods in analyzing transportation choices. Each approach offers unique advantages and insights, contributing to a comprehensive understanding of the factors influencing commuting decisions among graduate students.

# Interpretation of the models:

1. **Linear Probability Model (LPM):** The LPM estimates the probability of commuting choices during winter, specifically between driving and taking the bus. The coefficients represent the change in the probability of choosing driving over taking the bus for a one-unit change in the respective predictor variables. For instance, the constant coefficient indicates the base probability of choosing driving over taking the bus when all other predictors are zero. The coefficient for the cost of driving reflects the impact of an increase in driving cost on the likelihood of driving, while the coefficient for driving time indicates how changes in driving time affect the probability of driving.

2. **Binary Logit Model (BLM):** The BLM explores the relationship between predictors and the probability of driving during winter. Coefficients in the BLM represent the log odds ratio of choosing driving over taking the bus. For example, a positive coefficient for the cost of driving suggests that higher costs are associated with a higher likelihood of driving, while a negative coefficient for driving time indicates that longer driving times decrease the odds of choosing driving.

3. **Multinomial Logit Model (MLM):** The MLM analyzes commuting choices in spring across multiple modes, including biking, walking, driving, and taking the bus. Coefficients in the MLM represent the log odds ratios of choosing each mode relative to a reference category (often the bus). For instance, a positive coefficient for biking indicates a higher likelihood of choosing biking over taking the bus, while a negative coefficient for driving suggests a lower likelihood of driving compared to taking the bus.

4. **Maximum Likelihood Estimation (MLE):** MLE estimates parameters for the multinomial logit model, providing deeper insights into the relationship between predictor variables and commuting mode choices. The coefficients represent the log odds ratios of choosing each mode relative to a reference category, similar to the MLM. MLE offers a rigorous statistical framework for estimating parameters, allowing for precise interpretation of the impact of predictor variables on commuting choices.

5. **Generalized Method of Moments (GMM):** GMM estimates parameters for the binary choice model (driving or taking the bus) using moment conditions from the data. Coefficients in the GMM model represent the change in the odds of choosing driving over taking the bus for a one-unit change in the respective predictor variables. GMM provides a robust estimation approach, particularly useful for addressing potential endogeneity issues in the data.

 # Limitations:

It is essential to acknowledge the limitations of this analysis. The reliance on a specific dataset may introduce bias and limit the generalizability of findings to broader populations or geographic regions. Furthermore, the modeling techniques employed assume certain functional forms and may not capture all relevant factors influencing commuting decisions. Endogeneity and omitted variable bias could also affect the robustness of the results, particularly in models where unobserved factors influence commuting choices. Additionally, the analysis primarily focuses on commuting behavior among graduate students, potentially overlooking differences in commuting patterns among other demographic groups. Addressing these limitations would require additional data sources, more sophisticated modeling approaches, and careful consideration of potential biases.

# Use Cases:

Despite these limitations, the insights gained from this project have several practical applications. Transportation planners and policymakers can leverage the findings to design more effective transportation policies and infrastructure investments tailored to the needs of different demographic groups. For instance, understanding the impact of cost, time, and socio-economic factors on commuting mode choices can inform decisions regarding public transit subsidies, road pricing mechanisms, and bike lane infrastructure. Employers and educational institutions can also utilize this knowledge to implement transportation-related incentives or benefits that promote sustainable commuting options and improve employee/student satisfaction. Moreover, urban planners and developers can incorporate these insights into community design to create more walkable, bike-friendly environments that encourage active transportation and reduce reliance on single-occupancy vehicles. Overall, the findings from this project offer actionable guidance for various stakeholders involved in transportation planning and decision-making.

# Conclusion:

This project employs a diverse set of modeling techniques to analyze commuting choices among graduate students, providing valuable insights into the factors influencing transportation mode selection. The Linear Probability Model (LPM), Binary Logit Model (BLM), Multinomial Logit Model (MLM), Maximum Likelihood Estimation (MLE), and Generalized Method of Moments (GMM) offer distinct perspectives on commuting behavior, each contributing to a deeper understanding of the decision-making process. Through these models, we have identified significant predictors such as cost, time, and socio-economic factors that influence commuting mode choices. Furthermore, the interpretation of model coefficients reveals nuanced relationships between these predictors and commuting behavior, shedding light on the trade-offs individuals make when selecting transportation modes. Overall, the findings from this project contribute to the existing literature on transportation modeling and provide actionable insights for transportation planners, policymakers, and stakeholders.
