# Evaluation of the Ebola data and statistics
## by Uchanma Adeola Igbokwe


This dataset is from the World Health Organization and contributions were made by HDX. The dataset contains information for 36 different indicators in 10 countries on the Ebola outbreak from August 2014 to March 2016. The 2014–2016 outbreak in West Africa was the largest Ebola outbreak since the virus was first discovered in 1976. The outbreak started in Guinea and then moved across land borders to Sierra Leone and Liberia. The list of affected countries in the dataset are Guinea, Liberia, Sierra Leone, Nigeria, Senegal, Mali, Spain, the USA, the United Kingdom and Italy. Information in the dataset was last updated on the 10th of November 2019.

There were originally 36 indicators in the dataset, however, 9 indicators were of interest in this analysis. The following are the list of indicators considered during the analysis:
- Total number of confirmed ebola cases: any suspected or probable case with a positive laboratory result.
- Total number of suspected ebola cases: any person, alive or dead, suffering or having suffered from sudden onset of high fever, and had contact with:
      a suspected, probable or confirmed case, or a dead or sick animal.
- Total number of probable ebola cases: any suspected case evaluated by a clinician.
- Total number of confirmed, probable, and suspected ebola cases
- Total number of confirmed ebola deaths
- Total number of suspected ebola deaths
- Total number of probable ebola deaths 
- Total number of confirmed, probable, and suspected ebola deaths
- Case fatality rates: a measure of disease severity and often used for prognosis(predicting disease course or outcome.) The lower the rate, the better.

The main variables of interest were total number of confirmed ebola deaths, case fatality rate of the disease in each country on the different days and the total probable ebola cases.

>> This dataset can be found in https://data.humdata.org/dataset/ebola-cases-2014  

#### Facts about Ebola or Ebola Virus Disease (EVD)
##### Description
The Centre for Disease Control and Prevention (CDC), 2021 describes Ebola virus disease (EVD) as a deadly disease with occasional outbreaks that occur mostly on the African continent. EVD most commonly affects people and nonhuman primates (such as monkeys, gorillas, and chimpanzees). It is caused by an infection with a group of viruses within the genus Ebolavirus.
The mean EVD case fatality rate is roughly 50%. In previous epidemics, case fatality rates ranged from 25 to 90 percent.

##### Transmission
The virus spreads among humans through human-to-human contact and is spread to people by wild animals. The virus first spreads to people through direct contact with the blood, body fluids and tissues of animals. Ebola virus then spreads to other people through direct contact with body fluids of a person who is sick with or has died from EVD.

##### Prevention
For outbreaks to be successfully controlled, community involvement is essential. A combination of actions, including case care, infection prevention and control procedures, surveillance and contact tracing, strong laboratory service, safe and respectable burials, and societal mobilisation, are necessary for effective outbreak control.

Ebola vaccines have been created and deployed to help contain the spread of epidemics of the disease in Guinea and the Democratic Republic of the Congo (DRC).

#### References
1. Centre for Disease Control and Prevention (27 April 2021). Ebola Virus Disease. https://www.cdc.gov/vhf/ebola/about.html

2. World Health Organization (WHO) (23 February 2021). Ebola Virus Disease. https://www.who.int/news-room/fact-sheets/detail/ebola-virus-disease
 


### Summary of data wrangling steps:

After the assessment of the dataset, the following steps were taken to clean it up before exploration was carries out:
1. The dataset was made tidy by making variables columns and observations as rows. That is long format was changed to the wide format.
2. Varibles (columns) of interest were selected and datatype changed to the appropriate one.
3. The entries that had Guinea 2 and Liberia 2 were made uniform with other entries for the countries. This was done by removing the '2' and trailing whitespaces.
4. A new column for case fatality rate was calculated using the number of deaths from the disease and the number of confirmed cases for each day.

### Summary of Findings

In the distribution of the variables, the number of confirmed cases, number of confirmed deaths, and the number of probable cases majority of the values were between 0-300. Other values were spread across a wide range as high as 8700 in the number of confirmed cases. 

When number of probable cases and number of confirmed cases were compared, there were incidents when the number of probable cases and number of confirmed cases had close values. An increase in the number of probable cases did not suggest there will be an increase in the number of confirmed cases. On the contrary, when probable case numbers were low, number of confirmed cases spiked and were found to be higher.

There was a generally upward trend in Ebola cases and deaths for the duration of the epidemic. 6 African countries, 1 North American country, and 3 European countries were affected by the epidemic.  
African countries: Nigeria, Liberia, Guinea, Sierra Leone, Senegal and Mali.
European Countries: The United Kingdom (UK), Italy and Spain.
North America: The United States of America (USA).

The top three worst hit countries were Sierra Leone, Guinea and Liberia. 
Even though Sierra Leone had the greatest number of confirmed deaths and cases, the severity of the epidemic was the highest in Guinea compared to the other countries. 

### Key Insights:

> There was a very strong positive correlation between the number of confirmed deaths and the number of confirmed cases. It was generally noted that as the number of cases increased, so did the number of deaths. 

> Sierra Leone had the highest number of confirmed cases and the highest number of confirmed deaths. And in second place was Guinea. These were the two worst hit countries. On the other hand, Italy had the least number of confirmed cases (141) and recorded zero deaths. Next was the United Kingdom with 221 confirmed Ebola cases and zero deaths.  Other countries that recorded zero deaths were Spain and Senegal. 

> It was interesting to find that Senegal was the only African country with zero deaths and the lowest number of confirmed cases (254).

> The average daily case fatality rate for the duration of the outbreak was 28.7%.

> When examining the overall case fatality rate for the period of the epidemic, compared to the other countries, Guinea was the most hit in the outbreak. Guinea's case fatality rate was as high as 61.5%. This might be an indication of the need for personnel and resource support. To prove or disprove this, data on the availability of health personnel, facilities and other necessary resources would have to be collected and analyzed. 
Despite having the highest number of cases and verified deaths, Sierra Leone's case fatality rate (39.1%) was lower than that of Guinea. 
The third highest case fatality rate would be expected to be in Liberia, yet this is not the case. The third-highest case fatality rate (36.9%) was in Nigeria.

N/B: Disease severity is gauged by the case fatality rate.
