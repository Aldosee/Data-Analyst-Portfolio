**📊 COVID-19 in the Philippines 🌏**

## 🌐 Objective
The COVID-19 project in the Philippines is to comprehensively analyze and present the regional distribution of confirmed cases, prevalent symptoms, and age groups affected. Through this exploration, it aims to contribute valuable insights for targeted public health interventions and regional strategies in mitigating the impact of the virus.

### 🤔💭 Questions for this analysis using SQL queries:

1. What region has the highest covid cases?
2. What age group infected the most?
3. Identify what category of covid cases recorded by DOH.

## 🛠️ Tools
- SQL: For analysis and query database to answer the questions.
 - SQL Server Management Studio (SSMS): Integrated environment for managing any SQL infrastructure.
 - Git & GitHub: SQL scripts and analysis. Project tracking of updates.
 - PowerBi: Visualization and to give a comprehensive insight of the data analysis.


 ## 🔎 Analysis

 1. What region has the highest covid cases? 
 
    The table showed that regions with higher populations, like the NATIONAL CAPITAL REGION (NCR), tend to have higher COVID-19 case counts due to the higher density of people and greater likelihood of virus transmission. Conversely, regions with lower populations, such as the AUTONOMOUS REGION IN MUSLIM MINDANAO (ARMM), might report fewer cases due to fewer people and potentially less frequent interactions.


    | Region                                              | Covid Case  |
    |-----------------------------------------------------|-------------|
    | NATIONAL CAPITAL REGION (NCR)                       | 1,423,227   |
    | REGION IV-A (CALABARZON)                            | 397,797     |
    | CORDILLERA ADMINISTRATIVE REGION (CAR)              | 156,255     |
    | AUTONOMOUS REGION IN MUSLIM MINDANAO (ARMM)         | 51,774      |
    | REGION VII (CENTRAL VISAYAS)                        | 242,409     |
    | REGION IX (ZAMBOANGA PENINSULA)                     | 143,686     |
    | REGION XI (DAVAO REGION)                            | 259,370     |
    | REGION III (CENTRAL LUZON)                          | 562,673     |
    | REGION II (CAGAYAN VALLEY)                          | 296,128     |
    | REGION X (NORTHERN MINDANAO)                        | 171,844     |
    | REGION VIII (EASTERN VISAYAS)                       | 90,138      |
    | REGION V (BICOL REGION)                             | 101,823     |
    | REGION XII (SOCCSKSARGEN)                           | 118,573     |
    | REGION I (ILOCOS REGION)                            | 224,231     |
    | BARMM                                               | 30,874      |
    | REGION IV-B (MIMAROPA)                              | 78,261      |
    | REGION XIII (CARAGA)                                | 118,759     |
    | REGION VI (WESTERN VISAYAS)                         | 294,885     |



    ### A visual presentation of covid cases per region in the Philippines. 

    ![Age Group Infection](<assets/Heat_Map_Covid.png>)


2. What age group infected the most?

    The age group 25 to 29 has the most infections for both males and females. This is evident from the longer bars in this age range compared to other age groups.
    
    ### Reasons for High Infection Rates in 25 to 29 Age Group:

    -**High Mobility:** Individuals in this age group are typically more mobile, often commuting for work, education, and social activities, increasing their exposure to the virus.
    
    **-Social Interaction:** This age group tends to have a higher level of social interaction, both professionally and personally, which can lead to more opportunities for transmission.

    **-Workforce Participation:** Many individuals in this age group are active in the workforce, which may require them to be in environments where physical distancing is challenging.

    ### Age Group with the Least Infections:

    The age group 80+ has the fewest infections for both males and females. This is shown by the shortest bars in this age range.

    Reasons for Low Infection Rates in 80+ Age Group:

    **-Lower Mobility:** Older adults tend to have lower levels of mobility, reducing their chances of exposure to the virus.

    **-Higher Caution:** This age group may be more cautious and adhere more strictly to public health guidelines due to their higher risk of severe illness from COVID-19.

    **-Protective Measures:** There may be more protective measures in place for this vulnerable age group, such as priority vaccination, dedicated shopping hours, and restricted visitation in care facilities. 

    ![Age Group Infection](<assets/Age_Group_Infection.png>)

3. Identify what category of covid cases recorded by DOH.


    The National Capital Region (NCR) leads in confirmed COVID-19 cases due to its high population density, economic activity, and better healthcare access. In contrast, the Autonomous Region in Muslim Mindanao (ARMM) has lower cases due to lower population density, geographical isolation, and limited healthcare infrastructure. These factors contribute to varying infection rates across regions.

    | Region                                            | Total Confirmed_ Asymptomatic | Total Confirmed_Critical | Total Confirmed_Mild | Total Confirmed_Moderate | Total Confirmed_Severe |
    |---------------------------------------------------|-------------------------------|--------------------------|----------------------|--------------------------|------------------------|
    | NATIONAL CAPITAL REGION (NCR)                     | 137,830                       | 142,499                  | 368,210              | 493,358                  | 281,330                |
    | REGION IV-A (CALABARZON)                          | 27,145                        | 25,953                   | 130,566              | 148,342                  | 65,791                 |
    | CORDILLERA ADMINISTRATIVE REGION (CAR)            | 8,886                         | 8,401                    | 53,022               | 43,221                   | 42,725                 |
    | AUTONOMOUS REGION IN MUSLIM MINDANAO (ARMM)       | 22,935                        | 652                      | 15,729               | 10,213                   | 2,245                  |
    | REGION VII (CENTRAL VISAYAS)                      | 21,721                        | 13,756                   | 75,046               | 89,077                   | 42,809                 |
    | REGION IX (ZAMBOANGA PENINSULA)                   | 4,618                         | 5,722                    | 34,804               | 66,424                   | 32,118                 |
    | REGION XI (DAVAO REGION)                          | 45,307                        | 7,928                    | 89,779               | 72,582                   | 43,774                 |
    | REGION III (CENTRAL LUZON)                        | 44,396                        | 24,666                   | 195,939              | 217,508                  | 80,164                 |
    | REGION II (CAGAYAN VALLEY)                        | 34,175                        | 10,462                   | 141,065              | 81,568                   | 28,858                 |
    | REGION X (NORTHERN MINDANAO)                      | 14,359                        | 3,793                    | 69,090               | 55,664                   | 28,938                 |
    | REGION VIII (EASTERN VISAYAS)                     | 11,475                        | 1,692                    | 43,383               | 27,312                   | 6,276                  |
    | REGION V (BICOL REGION)                           | 11,298                        | 3,077                    | 33,020               | 36,111                   | 18,317                 |
    | REGION XII (SOCCSKSARGEN)                         | 9,217                         | 5,354                    | 50,545               | 42,691                   | 10,766                 |
    | REGION I (ILOCOS REGION)                          | 23,620                        | 8,970                    | 110,361              | 54,959                   | 26,321                 |
    | BARMM                                             | 4,001                         | 1,115                    | 7,231                | 10,562                   | 7,965                  |
    | REGION IV-B (MIMAROPA)                            | 5,164                         | 2,797                    | 33,618               | 24,030                   | 12,652                 |
    | REGION XIII (CARAGA)                              | 15,216                        | 4,255                    | 48,767               | 40,727                   | 9,794                  |
    | REGION VI (WESTERN VISAYAS)                       | 26,961                        | 11,013                   | 102,152              | 110,743                  | 44,016                 |





 ##  🔗 Sources
📖 Dataset: https://doh.gov.ph/covid19tracker

⚙️ Script: [SQL](https://github.com/Aldosee/Data-Analyst-Portfolio/blob/main/Covid_19_Philippines/SSMS_PhCovid(11.03.24).sql)

📈 Dashboard: [PowerBI](https://github.com/Aldosee/Data-Analyst-Portfolio/blob/main/Covid_19_Philippines/PhCovid(Dashboard_PowerBI).pdf)
