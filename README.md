## Vaxequity

### Goal: **Enhance Health Equality**

Equality is eliminating the differences among groups of people. These groups can be defined based on their gender, economical, demographical, or geographical status. Health inequalities concern health factors and access to the resources required to improve and maintain health. They also involve a failure to avoid or overcome inequalities that infringe on fairness and human rights norms.

Enhancing health equities is vital because health is a basic human right. Some groups of people are more vulnerable than others when facing health issues. This vulnerability could be a result of some characteristics. Out of all, some common characteristics that increase the vulnerability of people against health issues are age, income, gender, and ethnicity. People who are vulnerable to some diseases (e.g., COVID19) are people ages 65 and greater. Also, children under 6 years old are socially vulnerable age groups so families with these children can be vulnerable to health issues. Low-income groups are more vulnerable than people who have high incomes and can stop working temporarily with less mental concern. Also, females and some ethnicities are among socially vulnerable groups whose health issues can compromise their life quality (e.g., loss of job). 

Considering COVID19 the rate of reported cases varies in different neighbourhoods. Some neighbourhoods have a significantly higher rate of cases than others. If a group of vulnerable people live in the same neighbourhood, the health risk will dramatically be higher compared with the same rate of COVID cases in a low vulnerable neighbourhood. The question is that how we can help to balance this risk (generated by the vulnerability of groups of people and the high rate of COVID cases).

Considering COVID19 the rate of reported cases varies in different neighbourhoods. Some neighbourhoods have a significantly higher rate of cases than others. If a group of vulnerable people live in the same neighbourhood, the health risk will dramatically be higher compared with the same rate of COVID cases in a low vulnerable neighbourhood. The question is that how we can help to balance this risk (generated by the vulnerability of groups of people and the high rate of COVID cases).
 
The solution goes beyond empowering these vulnerable groups through systemic changes, such as law reform or changes in economic or social relationships. Simultaneously, reducing the health issues among these groups of society can be as effective and valuable. One way to do so is to increase the access to maintain health (e.g., immunization clinics). By enhancing health equality that results from differences in facilities that help in maintaining health, we can offer vulnerable groups the opportunity to enjoy life and pursue one's life plans.

## Health Equality Map Calculation

The team proposes an Health Equality Map Index (HEMI), using geo-spatial map analysis task related to equality criteria and health issues (COVID19 as an ongoing example) data available in Toronto area. 
We organized and cured the Toronto census data including age, gender, income, ethnicity, count of covid cases, location of the immunization clinics, and neighbourhoods. The group of vulnerable people were identified through geospatial analysis (overlaying) of the four selected criteria for vulnerability (age, gender, income, ethnicity). The method for overlaying was on the multicriteria decision-making basis (MCDM), based on which all criteria were brought to an identical unit (percentage). It was through rescaling to percentage, normalization by the min-max method for the neighbourhoods. The below table describe the summary of Health Equaty Map criteria and calculation:


|     Data Layer    |      Original data      |  Low valunerable (0%) |  Highly valunerable (1000%)
|----------|-------------|------|------|
| Age |   Population of People > 6 and > 65  | Zero population with these criteria live in this neighbourhood |  Maximum population with this criterion lives in this neighbourhood (compared with other neighborhoods) 
| Gender |   Population of female living in the neighborhood | Zero population with these criteria live in this neighbourhood |	Maximum population with this criterion lives in this neighbourhood (compared with other neighborhoods)	| 
| Ethnicity |  Population of first nations | Zero population with these criteria live in this neighbourhood |	Maximum population with this criterion lives in this neighbourhood (compared with other neighborhoods)	| 
| Income |  Annual income of the neighbourhood | Highest income |Lowest Income
| Covid cases |  Count of cases per neighborhood | Zero cases of Covid were reported in the neighbourhood |Highest count of cases lives in this neighbourhood
| Vulnerability |  Age, gender, ethnicity, and income were overlaid to create this data set  | Low vulnerable people live in this neighbourhood |Highly vulnerable people live in this neighbourhood
| Risk |  Vulnerable people in vicinity of Covid cases |  Low risk (Covid cases and vulnerability is low)  |High risk (Covid cases and vulnerability is low)
| Immunization clinics (as health facility) |  Count of immunization clinics per population of neighborhood | Zero clinics in the neighbourhood |Maximum count of clinic in the neighbourhood (compared with others)
| Equity |  Comparison of Risk (vulnerable groups and covid cases in the neighbourhood) and Immunization clinics (count of clinics) | Maximum equality (risk is high but the number of clinics is low, OR, the risk is low but the number of clinics is high) |Maximum equality (risk and number of clinics are both high, OR, risk and number of clinics are low)


`All four selected criteria (Criteria 1: age, Criteria 2: income, Criteria 3: ethnicity, Criteria 4: gender, Criteria5: covid cases) were     normalized by applying the linear standardization between 0 and 100.`

`(NC)_(i,1)=(C_(i,1)-((C_(i,1)))_min)/(((C_(i,1))_max-((C_(i,1)))_min )`
 

 Where i is the neighbourhood number, NCi,1 is the normalized criteria at neighbourhood i, Ci,1 is the actual value of the Criteria1  at  neighbourhood i, and (C1)max is the maximum value of Criteria1 within the study area. 

`The mathematical model for vulnerability which incorporates the four selected criteria using the weighted sum method (Chung & Kim, 2014) is presented below:`

   `V_i=∑_(k=1)^4▒NC_(k,i)/4	`
   
`Where Vi is vulnerability rate at neighbourhood i, NCi,k is the normalized Criteria k at neighbourhood i.
The risk at each neighbourhood was calculated using the risk formula.`

   `R_i=V_i×(N)_(5,i)`
   
`Where Ri is risk rate at neighbourhood i, NCi,5 is the normalized covid cases at neighbourhood i.`


The following chart represent the workflow of criteria map combination and generating the Health Eqiality Map:

![image](https://user-images.githubusercontent.com/52434636/113494450-3ccda180-94b6-11eb-8635-1757392304a0.png)



## App Features Description

The designed app provide an analytical dashboard embeds Visual Analytics functionalities so that, firstly, the user can attain a comprehensive insight about the health equality status of the neighbourhood, as well as the key contributing factors. Secondly, by selecting the neighbourhood user can individually look at the statistics and health equality status in the neighbourhood. Thirdly, the user can find the clinics within a user-defined buffer and find the direction to the closest clinic. 

Visual analytics is "the science of analytical reasoning facilitated by interactive visual interfaces." Our team utilized this concept to create the dashboard allowing the users to get clear and holistic information about health equality in the Toronto neighbourhoods by considering the vulnerability of people in the society and the hazard of Covid cases surrounding them, and their access to health care facilities (e.g., immunization clinics). This platform introduces a concept beyond Covid health facilities. The ongoing health issue (Covid disease) and facilities (immunization clinics) can be any identical health issue and facility, respectively. The platform thus is also crucial to research communities studying medical and health data analysis.

 ### Decision Making Tools
    
 ### Map Momparison Tool

 ### Summary Report Tools

 ## Data Sources
|     Data     |      Source      |  Year |
|----------|-------------|------|
| Immunization Clinics |   [link](https://open.toronto.ca/dataset/covid-19-immunization-clinics/)  | 2021 |
| Population |   [link](https://open.toronto.ca/dataset/neighbourhood-profiles/) |2016  |
| Age |   [link](https://open.toronto.ca/dataset/neighbourhood-profiles/) |2016  |
| Gender |   [link](https://open.toronto.ca/dataset/neighbourhood-profiles/) |2016  |
| Ethnicity |   [link](https://open.toronto.ca/dataset/neighbourhood-profiles/) |2016  |
| Covid19 Cases |   [link]() |2021  |
| Boundary files |   [link](https://www12.statcan.gc.ca/census-recensement/2011/geo/bound-limit/bound-limit-2016-eng.cfm) |2016 |
| Icon (mask) |   [link](https://www.flaticon.com/license/icon/2878235) |2021  |
| Icon (person1) |   [link](https://www.flaticon.com/license/icon/1077114) |2021  |
| Icon(person2) |   [link](https://www.flaticon.com/license/icon/2522086) |2021  |
| Image-Vaccine |   [link](https://unsplash.com/@ivvndiaz?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) |2020  |
| Image-Equality |   [link](https://pixabay.com/photos/math-blackboard-education-classroom-1547018/) |2020 |



 ## Reference

Armenakis, C., Du, E., Natesan, S., Persad, R., & Zhang, Y. (2017). Flood Risk Assessment in Urban Areas Based on Spatial Analytics and Social Factors. Geosciences, 7(4), 123. https://doi.org/10.3390/geosciences7040123

Chung, E. S., & Kim, Y. (2014). Development of fuzzy multi-criteria approach to prioritize locations of treated wastewater use considering climate change scenarios. Journal of Environmental Management, 146, 505–516. https://doi.org/10.1016/j.jenvman.2014.08.013

