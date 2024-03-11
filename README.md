# GLOBAL UNEMPLOYMENT DATA ANALYTICS

### Problem Statement

Unemployment remains a pressing economic and social issue worldwide, with implications for individuals, communities, and governments. Thus, gaining insights into the subject is important for informed policy-making, resource allocation, and economic planning, and will help to improve the percentage of individuals that are gainfully employed. 

The objective of this project is to prepare, analyse, and visualise a global unemployment dataset to identify trends, regional disparities, and demographic patterns. It will be done entirely with Microsoft Excel, and the focus will be on the following key areas:

- Trend analysis of global unemployment rates over the past decade.
- Regional analysis to explore variations in unemployment rates across different countries or regions.
- Demographic analysis to investigate disparities in unemployment rates by sex and age group.

### The Data

The dataset for this project was collected from [Kaggle](https://www.kaggle.com/datasets/sazidthe1/global-unemployment-data/data). It comprises 1,135 rows and 16 columns containing the following information:

1. Country name
2. Indicator name
3. Sex
4. Age group
5. Age category
6. 11 columns for the years 2014 to 2024, displaying the annual unemployment rate for each respective year.

### Data Preparation

After downloading and opening the data in Excel, several steps were taken to ensure it was ready for analysis. Firstly, a new version of the data was created to preserve the original dataset. Then, the following actions were carried out:

- **Data type check**: The columns were reviewed to ensure they were assigned the appropriate data types. Where necessary, columns were converted to text or numbers.
- **Duplicate check**: No duplicate rows were found in the dataset.
- **Missing values**: Unemployment rates for Ukraine in the 2022, 2023, and 2024 columns were missing, as well as values for the Palestinian Territories in 2023 and 2024. These blanks were filled using the mean rate of the preceding years.
- **Categorical variables**: All categorical variables were inspected for spelling errors or unexpected values. No issues were found.
- **Outliers**: No outliers were detected in the dataset.
- **Column removal**: The 'indicator_name' column, which contained a singular value ("Unemployment rate by sex and age"), was removed as it was redundant.
- **Age category column**: The 'age_category' column contained three values (Youth, Adults, and Children). Given that the Children category consists of individuals below the age of 15, who are not typically part of the labour force, these rows were deleted from the dataset to correct any classification errors.
- **Regions**: A new worksheet containing countries and their respective continent/regions was imported into the workbook. A new 'Regions' column was created, and using ***VLOOKUP*** and ***MATCH*** functions, each country was assigned to its specific region. The region of each country was fact-checked, facilitated using filters, and where there was unavailable or incorrect information, they were corrected manually.

### Exploratory Data Analysis

Once preparation was done, it was time for exploration and analysis. It was important to know the average global population and the average youth population for the time under consideration so that was first calculated. Then, the analysis was broken down into two contexts: examining the global and regional patterns, and exploring the demographic dynamics.

#### Global and Regional Analysis
The analysis began by exploring the global trend in unemployment rates over the past decade. This involved calculating the average unemployment rates across all countries for each year and then representing the aggregated data in a pivot table to visualise the trend. 

Once the global trend was examined, attention turned to assessing the performance of each region over the years. Another pivot table was created, with each year listed in the values field and continent in the columns field. This allowed for a clear comparison of how unemployment rates had changed over time for each region.

After reviewing the regional trends, the analysis continued with the calculation of the average unemployment rate for each region. This helped to identify regions with the highest and lowest average rates of unemployment over the past decade. Once again, a pivot table was used to organise and present this information effectively.

Finally, the analysis sought to identify the countries with the lowest and highest unemployment rates. In both cases, the top 5 countries were retrieved. 

#### Demographic Analysis 
With the completion of the global patterns analysis, the focus shifted to understanding age and gender dynamics to discern which demographic groups faced the highest unemployment rates. The first step involved examining the trend of unemployment rates by gender. This allowed us to observe how unemployment rates fluctuated over the years for both males and females.

Next, the analysis investigated the trend of unemployment rates by age category, providing insights into how unemployment rates changed for both the youth and adult populations.

Moving forward, attention turned to exploring gender distribution across regions. This involved determining the percentage of unemployed males and females in each of the six regions and identifying regions with significant gender disparities. 

Furthermore, the distribution of age categories across regions was explored to assess whether there were more unemployed adults than youths in any region, and if so, by what margin.

Finally, the average unemployment rates for males and females were extracted from the dataset to complete the demographic analysis.

To enhance the dashboard's interactivity, the following slicers were created:

- An age category slicer that allows users to filter information specific to either adults or youths.

- A gender slicer that enables users to view the gender distribution of all generated insights.

### Insights
#### Global and Regional Patterns

1. **Global Trend**: The global unemployment rate experienced a steady decline until 2020, when it surged to a peak of 16%. This was most likely due to the COVID-19 pandemic that led to a loss of jobs for millions of people. There, however, was a rapid fall between 2020 and 2022 and then a more steady decrease leading up to 2024.

   ![Global trend](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/b2064d1f-beb2-4390-abba-f11e7b78d439)

3. **Trend Per Region**: Europe had the highest unemployment rate in 2014 (17.24%), but has since seen a steady decline, with the rate reaching 10.52% in 2024. South America recorded the highest rate in 2020 (16.25%). Presently, Africa has the highest unemployment rate at 13.23%, while Oceania, with 9.58%, has the lowest rate.

   ![Region trend](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/2ad74207-2b64-45f0-939a-4e7833053cee)

5. **Average Rate Per Region**: Africa (13.39%) has the highest average unemployment rate, while Oceania (9.98%) has the lowest average rate.

   ![Region averages](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/88536f37-1f08-4e7b-8249-c9f4fb0a2a72)

4. **Country Data**: Cambodia, Niger, Qatar, Chad, and the Solomon Islands have the lowest unemployment rates, with Cambodia averaging only 0.46%. Conversely, Djibouti, the Palestinian Territories, Libya, South Africa, and Eswatini face the highest rates, with Djibouti averaging 49.09%.

   ![Top countries](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/da91dc2a-942c-42ed-809f-faf3b2e470a9)
   ![Botttom countries](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/46c1fa59-a383-40b2-8c7c-4cf3ace61e61)

#### Age and Gender Dynamics 
1. **Gender Trend**: Throughout the past decade, more females have been unemployed than males, with a general decrease observed in both genders, except for 2020.

    ![Rate trend per gender](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/d7723adc-063d-4cba-9902-efb67a102c80)

2. **Age Category Trend**: Youths have consistently faced higher unemployment rates than adults over the past decade, with a steady decrease observed in both categories, although with a gentler trend observed for adults.

    ![Rate trend per age category](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/cabff93d-33fd-4e18-87fb-fd8ca363bdca)


3. **Gender Distribution Per Region**: Asia has the highest disparity in unemployed males to females, with a difference of 3.73%, while Europe has the lowest disparity with only 0.1%.

    ![Average rate per gender](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/b7142636-3f70-490f-96ce-7109f9d60826)

4. **Age Distribution Per Region**: North America has a higher proportion of unemployed youths compared to adults than any other region, while South America has the lowest disparity in adult and youth unemployment rates.

    ![Average rate per age category](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/dd9be1c9-61d6-4c83-906d-45f12bb2d099)

5. Over the past decade, the average unemployment rate for males, females, and youths was found to be 10.9%, 13.53%, and 17.99%, respectively. The average global unemployment rate over the same period is 12%. 

### Dashboards
#### Global and Regional Patterns
![Global Unemployment Dashboard1](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/2417c209-5c4a-4860-a51d-5e1211a0193f)

#### Age and Gender Dynamics 
![Global Unemployment Dashboard2](https://github.com/Idorenyin-Udoh/Unemployment-Analytics-Project/assets/162564901/f1138da5-7849-47e5-b9ac-f50e716d98ee)

### Recommendations

Following a comprehensive analysis of the data, the following recommendations are proposed to reduce the rate of unemployment globally: 

1. Targeted employment programs should be developed in high unemployment regions, such as Africa and North America, focusing on vulnerable groups such as youth and females. Collaboration should be initiated with local governments, NGOs, and businesses to provide training, mentorship, and job placement assistance, aiming to improve employability and reduce unemployment rates.
2. Education and skills development programs should be improved to equip individuals with the necessary competencies for emerging job markets. Focus should be placed on STEM (Science, Technology, Engineering, and Mathematics) education, digital literacy, and vocational training to meet the demands of evolving industries.
3. Policies to promote gender equality in the workforce and reduce disparities in unemployment rates between males and females should be implemented. Support for work-life balance, including affordable childcare and parental leave policies, must be provided. Women's participation in non-traditional sectors and leadership roles should be promoted through mentorship and networking programs.
4. Encouragement for investment in economic diversification is important for the creation of new jobs and the reduction of sector dependency. Support for startups and small businesses, particularly in regions with limited job opportunities and high unemployment rates, is vital for the fostering of entrepreneurship and innovation.
5. Youth employment must be prioritised by creating accessible education, training, and job programs. Partnerships between government, education, and private sectors for youth employment and entrepreneurship, including subsidised schemes and startup support should be encouraged.
6. A robust monitoring and evaluation framework should be established to track intervention effectiveness and measure progress in reducing unemployment rates. Stakeholders should be engaged in ongoing dialogue and feedback loops to ensure accountability, transparency, and continuous learning in the pursuit of reducing global unemployment.








