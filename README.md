# Socioeconomic Vulnerabilities and Political Preferences in Mexican Municipalities

## Project Description (Abstract)

This study focuses on identifying the elements involved in the political
preferences in the Mexican municipalities during the Major elections of 2018 and 2021
to detect if exists a relationship between socioeconomic vulnerabilities and the preference
for some parties as many people argue each election. The methodology used is
quantitative with a data panel that structures the electoral preference of each municipality
as a dependent variable with the created variables “winner_2018” and “winner_2021”,
taking as independent variables the vulnerability index proposed by the National Council
for the Evaluation of Social Development Policy (Coneval). With multiple linear
regression, we found that for 2018 the access to health services and the percentage of
people in extreme poverty have statistical significance, and for 2021 only the first one

has statistical significance. This demonstrates that the arguments created around socio-
economic vulnerabilities and the relationship with voting preferences could be a stigma 
created to underestimate the capacity of people living with vulnerabilities to decide their
political preferences.

Keywords: vulnerabilities, Mexico, political parties, municipalities, poverty, political
preferences.

## Getting Started

For this project it was used the R studio Program, and it was reuiqered to have installed the packages of dplyr, raster, GISTools and Readxl

## File Structure - Introduction

Inequality and “classism” are one of manly the socioeconomic challenges of Mexican society.
México is one of the most unequal countries, not only in the region but in the world (Jusidman,
2009), and even if the official data may show little advances in some economic sectors like the
remittances and rural activities diversification, the situation of far from being resolved, and this
has caused that other related problems to appear in different arenas, like the political, as the
inequality has historical roots and with the past of time it has found a way to be expressed in a
multifactorial form.
In the political arena we can find that it exists a discourse of discrimination that seeks to
humiliate somehow or to decrease the value of the opinion of the poorest sector of the population
in its political preferences, making derogatory – and indeed with no evidence – on the political
preferences. In the last years has become quite regular to listen to or read accusations on how the
more vulnerable people tend to vote for one or another party, but there is always as background
the need of the people to be themselves in a privileged position against the otherness, where if you
vote for a determined party, then you are poor, and hence, worse than the others.
The current situation of inequality in Mexico has reached nowadays point after several
decades of economic, social, and political processes, nevertheless, analysis of this is not the aim
of the current essay; in the other hand, the discussion on the national level on the impact that has
de economic level of the individuals on their electoral preferences is relatively new, as during a
major part of the XX century, the political power in the country was concentrated in the same
political party, the National Revolutionary Party (PNR) since 1928 held the control of the Congress
and Executive power, a tendency that continue with its successor (same party but refunded) the
today alive Institutional Revolutionary Party (PRI).
This party kept the Federal Presidency of Mexico until the year 2000 when the National
Action Party (PAN) won the Presidency of the country, giving an end to 72 years of un-interrupted
PRI government, starting officially an alternate and somehow giving space to a different spectrum
of possibilities for pluralism in the country. Here is needed to have in consideration, that in Mexico
four main parties hold a national presence (and are officially recognized), the already mentioned
PRI and PAN, the Democratic Revolution Party (PRD), and the recently created National
Regeneration Movement (Morena). From these parties, we can draw a political location of ideals,
as the PAN is considered a right-wing party, the PRI a Center party, the PRD a left party, and Morena a left-wing party (considered a far-left wing party due to its positions of support to other
far left-wing regimes in the international arena).
Despite the 2000’s alternate mentioned above, in 2012, the historical party, PRI returned to
power, but in 2018 the most recent political force, Morena, managed to win the presidential spot
having as a major slogan the phrase “The poor people first”. With the more and more common
changes of political force in the power, different approaches to analysis started to appear claiming
the possibility of a correlation between the political preferences that related the poorest to vote for
a specific party, but no evidence supports the existence of such correlation.
And at the same time that academic studies started to appear, in social media (mainly
Twitter and Facebook) the spread of aggressive messages on the vision that different sector has on
the electoral basis of different parties, accusing the more educated sector of the population, and
the one with less social and economic vulnerabilities supports one or another specific political
force, but again, in this exchange of declarations, there is a lack of information or data that give
further back-up to the arguments.
Hence, there is where this line wants to give a response to the question: Do socioeconomic
vulnerabilities impact the political preferences at the municipality level in Mexico? For giving an
answer to this and trying to break with the tendency of trying to measure the political preferences
in the federalism arena, we will consider the electoral preference in the elections of Mayors in the
municipalities of the whole country. We aim to analyze the dynamics between socioeconomic
vulnerabilities and political preferences at the municipal level in Mexico, resulting in a better
understanding of the underlying factors that influence electoral behavior having into consideration
socioeconomic challenges, this is a first step towards the identification of correlations between the
needs and aspirations of vulnerable communities and their electoral preference.

With this research, students of social sciences, policymakers, consultancy firms, and NGOs
that work with political participation and social vulnerability, can have a more reliable back-up on
the idea of the impact that social vulnerabilities have on the political preference of the Mexican
voters. Our hypothesis lies on the premise that socioeconomic vulnerabilities have a significant
impact on political preferences at the municipality level in Mexico, with higher levels of
vulnerability correlating with certain political ideologies and voting patterns. Nevertheless, as a
null hypothesis, we have the opposite core idea, where the social vulnerabilities won’t have any
sort of correlation, or at least not any significance.
To demonstrate which hypothesis is achieved, it will be used a multiple correlation model,
where we will consider the political preference of each city as the dependent variable with the
created variable for each period studied: “winner_2018” and “winner_2021”, and as independent
variables different indicators of vulnerability in the same level, like the presence of poverty,
extreme poverty, educational backwardness, lack of access to services of health and social security,
and the lack of quality in the household materials and services, this taken from the index proposed
by the National Council for the Evaluation of Social Development Policy (Coneval).

## Data and Methodology

For this project it was used three main sources, all official from the Mexican government. For the
data on social vulnerabilities, we extract the data from the National Council for the Evaluation of
Social Development Policy (Coneval), in its studies on Poverty at the municipality level from 2015
and 2020. The second source was the National Institute of Statistics and Geography (INEGI), from
this we extract the total population of each city in Mexico, and we obtained the SHP filetype that
allowed us to make the plotting of the political results and levels of poverty all over the country.
And thirdly, we use the official results of the elections for mayor in 2018 and 2021 from the 32
Electoral Local Public Organizations (OPLEs).
For the methodology, the first step was the construction of the indicator through the census
statistics, to have the total population of each city (2015, 2018, 2021) in 25 of 32 states. The
methodology used for the analysis is geospatial analysis to correlate each municipality’s
vulnerability rate with the electoral results. Also, it was used a multiple linear regression analysis
to identify how strong the relationship between the variables that we are considering. The
dependent variable is Victories in local elections to Major positions for this it was created the

indicator for each election period “Winner_2018” and “Winner_2021”. The independent variables:
the set of indicators of social vulnerability proposed by Coneval and that is described in the formula
below.
Then, the downloading and cleaning of the database of social vulnerabilities was made and
merged using the dplyr package in R. The major challenge came with the tracking and
downloading of all the datasets of electoral results, as each OPLE has its landing webpage, and the
accessibility was not always friendly (difficulty finding the results in the web ecosystem). Once
all the electoral results were, we used a loop code in R to merge all the results into one single data
frame for the results of 2018 and 2021.
Once we get those three data frames (social vulnerability, and electoral results from 2018,
and 2021), we merged them using the CVEGEO code of each city. Once we had built the final data
frame, we ran two models of multiple linear regression analysis to identify how strong the
relationship between the variables that we are considering is. The two equations model are the
following: For 2018 =
Winner party ~ population 2015 + percentage of poverty in 2015
+ percentage of extreme poverty in 2015
+ percentage of population with at least one social lack in 2015
+ percentage of population with educational backwards in 2015
+ percentage of population that is vulnerable by its income in 2015
+ percentage of population that is not poor or vulnerable in 2015
+ percentage of population with lack of social security in 2015
+ percentage of population with lack of health services in 2015
+ percentage of population with lack of quality and spaces in their household in 2015
+ percentage of population with income below the line of poverty in 2015.
• For 2021 =

Winner party ~ population in 2021 + percentage of poverty in 2021
+ percentage of extreme poverty in 2021
+ percentage of population with at least one social lack in 2021
+ percentage of population with educational backwards in 2021
+ percentage of population that is vulnerable by its income in 2021
+ percentage of population that is not poor or vulnerable in 2021
+ percentage of population with lack of social security in 2021
+ percentage of population with lack of health services in 2021
+ percentage of population with lack of quality and spaces in their household in 2021
+ percentage of population with income below the line of poverty in 2021.
Besides the core analysis, it was used the SHP file of the country to geo-represent the
presence of poverty and the electoral results of each of the years of interest using GIStool, Ggplot2,
and raster packages in R.

## Analysis

The analysis revealed a significant positive correlation between some of the socioeconomic vulnerabilities and the preference for political parties advocating for social welfare policies and income redistribution. Municipalities with higher poverty rates, and limited access to health showed a stronger inclination toward supporting candidates who prioritize poverty alleviation programs and social development initiatives. That could be the ruling party because it has more resources to invest in those proposals and publicity. 
Figure 1. Municipality Party’s Victories 2018  
 ![image](https://github.com/ErickNavarrete29/Socioeconomic-Vulnerabilities-and-Political-Preferences-in-Mexican-Municipalities/assets/139622375/1547a030-ca5c-41ee-a535-2139ec7f0af0) ![image](https://github.com/ErickNavarrete29/Socioeconomic-Vulnerabilities-and-Political-Preferences-in-Mexican-Municipalities/assets/139622375/6cd28fe8-d40f-4ae5-b350-b29a5ce5cc99)


Own elaboration with data from National Electoral Institute 2018

Figure 2. Population in extreme poverty by Municipality in 2018
![image](https://github.com/ErickNavarrete29/Socioeconomic-Vulnerabilities-and-Political-Preferences-in-Mexican-Municipalities/assets/139622375/d4cee282-732d-438d-9465-069596865108)
 
Own elaboration with data from CONEVAL 2018

With figures 1 and 2 we can compare the winning parties in each municipality in Mexico and also the population in extreme poverty, as we can see in the South and Center part of Mexico are the localities with more population in extreme poverty and also those that voted for the left-wing party (Morena), but we can release also that on the North part of Mexico, in municipalities located in Sinaloa and Baja California,  that has the fever level of poverty the winner party was the same. So, it seems to exist correlation if we only consider these two factors but not in all the cases, moreover, when we make the multiple linear regression all these assumptions change. 

Figure 3. Changes in State governments from 2018 to 2021
 ![image](https://github.com/ErickNavarrete29/Socioeconomic-Vulnerabilities-and-Political-Preferences-in-Mexican-Municipalities/assets/139622375/6902864e-2245-4d50-95f6-15127f5eba72)

Own elaboration with data from National Electoral Institute 2021

Also in Figure 3, we can see how the left-wing party acquired more electors that voted for it during the 2021 elections for State governor that shows that not only in some parts of Mexico started to vote for that party, but in all the country, another fact that could demonstrate that the assumption established on the hypothesis could be refuted because not only poor people or non-educated voted for Morena. This was also because the party won the last elections with more than 10 percent of the advantage. It also would address whether vulnerable communities are adequately represented in the political system and whether policies and political platforms align with the needs and concerns of these communities.
The regression analysis results are presented for the models corresponding to the 2018 and 2021 elections in separate tables. For 2018, the regression coefficients, standard errors, t-values, and associated p-values for the independent variables are displayed in Table 1. The intercept term was found to be statistically significant (p < 0.001), suggesting that there is a non-zero intercept when all independent variables are zero. 
Among the independent variables "Porcentaje_de_pobreza_extrema_2015" (people in extreme poverty) was also statistically significant (p < 0.001), suggesting that higher levels of extreme poverty are associated with specific voting patterns. However, none of the other independent variables reached statistical significance (p > 0.05), implying that there is insufficient evidence to establish a significant relationship between those variables and electoral preferences in the 2018 elections.

Table 1. Model 2018
Residuals:
    Min      1Q  Median      3Q     Max 
-2.1392 -0.7316 -0.2556  1.0254  2.2339 

Coefficients:
                                                                                       Estimate Std. Error
(Intercept)                                                                           2.529e+00  2.614e-01
Población2015                                                                         4.579e-07  1.798e-07
Porcentaje_de_pobreza_2015                                                           -1.033e+01  1.392e+01
Porcentaje_de_pobreza_extrema_2015                                                    1.942e-02  4.936e-03
Porcentaje_de_Población_con_al_menos_una_carencia_social_2015                         5.810e-03  5.458e-03
Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2015                        3.769e-03  4.072e-03
Porcentaje_de_personas_con_rezago_educativo_2015                                     -2.578e-02  4.524e-03
Porcentaje_de_personas_vulnerables_por_ingreso_2015                                  -1.032e+01  1.392e+01
Porcentaje_de_personas_no_pobres_y_no_vulnerables_2015                               -2.699e-03  5.493e-03
Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2015             3.304e-03  3.993e-03
Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2015          1.151e-02  3.736e-03
Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2015       -2.068e-03  4.198e-03
Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2015  1.032e+01  1.392e+01
                                                                                     t value Pr(>|t|)    
(Intercept)                                                                            9.675  < 2e-16 ***
Población2015                                                                          2.547  0.01095 *  
Porcentaje_de_pobreza_2015                                                            -0.742  0.45802    
Porcentaje_de_pobreza_extrema_2015                                                     3.934 8.63e-05 ***
Porcentaje_de_Población_con_al_menos_una_carencia_social_2015                          1.064  0.28724    
Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2015                         0.926  0.35476    
Porcentaje_de_personas_con_rezago_educativo_2015                                      -5.699 1.38e-08 ***
Porcentaje_de_personas_vulnerables_por_ingreso_2015                                   -0.742  0.45843    
Porcentaje_de_personas_no_pobres_y_no_vulnerables_2015                                -0.491  0.62323    
Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2015              0.827  0.40806    
Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2015           3.082  0.00209 ** 
Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2015        -0.493  0.62233    
Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2015   0.741  0.45856    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 1.078 on 2007 degrees of freedom
  (450 observations deleted due to missingness)
Multiple R-squared:  0.04507,	Adjusted R-squared:  0.03936 
F-statistic: 7.894 on 12 and 2007 DF,  p-value: 1.418e-14

For 2021, the regression coefficients, standard errors, t-values, and p-values for the independent variables in the 2021 model are presented in Table 2. Like the 2018 model, the intercept term was found to be statistically significant (p = 0.00058), indicating a non-zero intercept.  "Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2020" (population with lack of health services in 2020) stood out as highly statistically significant (p < 0.001), suggesting a strong relationship between the percentage of people lacking access to healthcare services in 2020 and electoral preferences in the 2021 elections. However, none of the other independent variables reached statistical significance (p > 0.05), implying that there is insufficient evidence to support a significant relationship between those variables and electoral preferences in the 2021 elections.

Table 2. Model 2021
Residuals:
    Min      1Q  Median      3Q     Max 
-2.2723 -0.8997 -0.2142  1.1531  2.0185 

Coefficients:
                                                                                       Estimate Std. Error
(Intercept)                                                                           4.000e+00  1.161e+00
Población2020                                                                         3.061e-07  1.885e-07
Porcentaje_de_pobreza_2020                                                            1.230e+02  2.491e+02
Porcentaje_de_pobreza_extrema_2020                                                    5.385e-03  6.900e-03
Porcentaje_de_Población_con_al_menos_una_carencia_social_2020                        -1.910e-02  1.281e-02
Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2020                        4.815e-04  4.602e-03
Porcentaje_de_personas_con_rezago_educativo_2020                                     -5.613e-03  4.536e-03
Porcentaje_de_personas_vulnerables_por_ingreso_2020                                   1.230e+02  2.491e+02
Porcentaje_de_personas_no_pobres_y_no_vulnerables_2020                               -1.702e-02  1.270e-02
Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2020            -5.794e-03  4.775e-03
Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2020          1.671e-02  2.649e-03
Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2020        3.024e-03  5.046e-03
Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2020 -1.230e+02  2.491e+02
                                                                                     t value Pr(>|t|)    
(Intercept)                                                                            3.446  0.00058 ***
Población2020                                                                          1.624  0.10462    
Porcentaje_de_pobreza_2020                                                             0.494  0.62158    
Porcentaje_de_pobreza_extrema_2020                                                     0.780  0.43520    
Porcentaje_de_Población_con_al_menos_una_carencia_social_2020                         -1.491  0.13612    
Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2020                         0.105  0.91670    
Porcentaje_de_personas_con_rezago_educativo_2020                                      -1.237  0.21608    
Porcentaje_de_personas_vulnerables_por_ingreso_2020                                    0.494  0.62167    
Porcentaje_de_personas_no_pobres_y_no_vulnerables_2020                                -1.340  0.18042    
Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2020             -1.213  0.22518    
Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2020           6.309 3.46e-10 ***
Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2020         0.599  0.54902    
Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2020  -0.494  0.62161    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 1.161 on 1974 degrees of freedom
  (483 observations deleted due to missingness)
Multiple R-squared:  0.05752,	Adjusted R-squared:  0.05179 
F-statistic: 10.04 on 12 and 1974 DF,  p-value: < 2.2e-16
Overall, the multiple R-squared values for both models were relatively low, indicating that the included independent variables explain only a small portion of the variation in electoral preferences. This suggests that other factors beyond the variables included in the models may also play a significant role in determining electoral outcomes in Mexican municipalities.

## Results

For the year 2018, it was found that extreme poverty indeed played a significant role in the voters’ preferences towards a leftwing party. Other elements that were relevant in this were the educational backwardness and the lack of access to health services. Nevertheless, in 2021 it was found that only the lack of access to health services was a significative variable in the determination of the political preference in the cities of Mexico.
This means that there is only consistency in the lack of access to health services in the determination of the people into supporting a left-wing party, nevertheless, this is only applicable in the consideration of a recent period. The weakness of the current study is the lack of contrastable evidence on more elections due to the lack of time for further research due to the inaccessibility of the information online on the electoral results. And yet, this does not mean that there is any support for the classist argument that argues that the poorest people have a particular preference, but the fact that the lack of access to health services had, but having this vulnerability does not mean that the other exist, including the income-related one.
Hence, the null hypothesis has a major approach to the results, as most of the vulnerability indicators did not have consistency and significance in the electoral preferences of the people, being access to health the only exception, ad not for that support on the core hypothesis to be tested, that was that more vulnerable people had a major tendency to support left-wing parties in Mexico. 
As a further step to the future, the research should be focused on matching the vulnerability-independent variables with further statistics elements within the socioeconomic spectrum, such as unemployment, outbreaks of violence and insecurity, GDP per capita, rule of law and human development, and to see if the lack of access to health services remains to have a strong bond to the electoral preferences of the Mexican voters.
Our study has some limitations we need to be careful in generalizing our findings beyond the Mexican case. Our results and robustness tests suggested an apparent disconnect between socioeconomic vulnerabilities and political preferences among elections during the 2018 and 2021 Major elections period. Future studies should further investigate the conditions under which social policy offerings became politicized and the extent to which political identities may filter public preferences for policies that are perceived to be aligned with partisan platforms and agendas. The analysis is based on cross-sectional data, which restricts our ability to establish causality and fully capture the dynamics of electoral preferences over time. Additionally, the models explained only a small portion of the variation in electoral preferences, suggesting the presence of unaccounted factors that influence voting behavior. 


## Contributors

Yare Ramirez Garrido - Research, coding and writing
Erick Armando Navarrete Segovia - Research, coding and writing


## Acknowledgments

Professor Torrent (Chung-pei Pien) for his teching in R coding.

## References

Berens, S. (2017). “Taxing Higher Incomes: What Makes the High-Income Earners Consent to More Progressive Taxation in Latin America?” Political. Behavior 39, 3: 703–29.
Carnes, E. (2013). “Measuring the Individual-Level Determinants of Social Insurance Preferences: Survey Evidence from the 2008 Argentine Pension Nationalization”. Latin American Research Review 48, 3: 10
Cortina, J. & Gelman, A. (2006). “Income and vote choice in the 2000 Mexican presidential election”. Social Science Research Network (SSRN).
Feierherd, G. (2021). “Courting Informal Workers: Exclusion, Forbearance, and the Left. American Journal of Political Science”, December 24. https://onlinelibrary.wiley.com/doi/10.1111/ajps.12576. 
Jusidman, C. (2009). “Desigualdad y política social en México. Nueva Sociedad”. Retrieved 25 of June 2023. Source: https://nuso.org/articulo/desigualdad-y-politica-social-en-mexico/#:~:text=M%C3%A9xico%20sufre%20una%20alta%20desigualdad,%C3%ADndices%20de%20desigualdad%20muy%20altos. 
Lipset, M. (1960). Political Man: The Social Bases of Politics. Garden City: Doubleday
Lugo Neria, B. (2021). Elecciones de ayuntamientos en Hidalgo (2008-2020): determinantes de la participación electoral City Council Elections in the State of Hidalgo 2008-2020: The Determinants of Electoral Participation (Vol. 65).
National Council for the Evaluation of Social Development Policy (Coneval), (2023). “Statistics on Municipal poverty 2010 – 2020”. Source: https://www.coneval.org.mx/Medicion/Paginas/Pobreza-municipio-2010-2020.aspx. 
National Institute of Statistics and Geography (INEGI). (2023). “Census 2020”. Source: https://www.inegi.org.mx/programas/ccpv/2020/. 
National Electoral Institute (INE). (2023). “Official Sites of the Electoral Local Public Organizations (OPLEs)”. Source: https://portal.ine.mx/voto-y-elecciones/opl/oples-estados/. 
Soto, I. & Cortez, W. (2014). “Determinantes de la participación electoral en México”. Estudios Sociológicos, 32 (95), 323-353.
Sura-Fonseca, R. (2019). “El vínculo entre la pobreza y la desigualdad con la participación electoral ciudadana: las elecciones presidenciales de 2006 y 2014 en Costa Rica”. Revista Mexicana de Ciencias Políticas y Sociales, 64 (235), 189-220.
Vargas, E. (2012). Vulnerabilidad_social_y_comportamiento electoral. Un análisis por secciones electorales. Universidad Autónoma del Estado de México.
Verba, S.  & Nie, H. (1972). Participation in America. Nueva York: Harper and Row.


## Annex - Full code used for the project 
poverty <- read_xlsx("Concentrado_indicadores_de_pobreza_2020/Concentrado_indicadores_de_pobreza_2020.xlsx")

poverty_15_20 <- poverty %>%
  select(Entidad_federativa, CVEGEO, Municipio, Población2015,Población2020, Porcentaje_de_pobreza_2015,
         Porcentaje_de_pobreza_2020, Porcentaje_de_pobreza_extrema_2015, Porcentaje_de_pobreza_extrema_2020,
         Porcentaje_de_Población_con_al_menos_una_carencia_social_2015, Porcentaje_de_Población_con_al_menos_una_carencia_social_2020, Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2015,
         Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2020, Porcentaje_de_personas_con_rezago_educativo_2015,
         Porcentaje_de_personas_con_rezago_educativo_2020, Porcentaje_de_personas_vulnerables_por_ingreso_2015, Porcentaje_de_personas_vulnerables_por_ingreso_2020,
         Porcentaje_de_personas_no_pobres_y_no_vulnerables_2015, Porcentaje_de_personas_no_pobres_y_no_vulnerables_2020,
         Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2015, Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2020,
         Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2015, Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2020,
         Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2015,Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2020,
         Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2015, Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2020, Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_extrema_por_ingresos_2020)

map1 <- merge(map, poverty_15_20, by = "CVEGEO")

map3 <- merge(map, poverty, by = "CVEGEO")

data_map <- as.data.frame(map3)

#Map of poverty 

ggplot() +
  annotation_spatial(map3) +
  layer_spatial(map3, aes(fill = Porcentaje_de_pobreza_extrema_2020)) +
  scale_fill_gradient(low = "#D1DDFF", high = "#113AAA", 
                      space = "Lab", na.value = "grey50",
                      guide = "colourbar") + 
  theme(panel.background = element_rect(fill = "white"))


##################
##################
##################RESULTS OF 2018

results_2018_list <- list.files("2018")
results_2018_list

results_2018 <- data.frame()
for (i in 1:length(results_2018_list)) {
  temp<-read.csv(paste0("2018/",results_2018_list[i]))
  temp <- temp %>%
    select(ID_ESTADO,ESTADO, ID_MUNICIPIO, MUNICIPIO, PAN, PRD, PRI, MORENA)
  results_2018 <- rbind(results_2018, temp)
}


unique(results_2018$PAN)

results_2018 <- results_2018 %>%
  mutate(PAN = ifelse(PAN %in% c("PRI", "N/R", "Sin Dato", "ILEGIBLE", "Ilegible", "ilegible", "sin dato", "SIN DATO", "Sin dato", "PAN", "", " "), 0, PAN))

results_2018 <- results_2018 %>%
  mutate(PAN = as.numeric(sub(",", "", PAN)))

unique(results_2018$PAN)

unique(results_2018$PRD)

results_2018 <- results_2018 %>%
  mutate(PRD = ifelse(PRD %in% c("Sin dato", "N/R", "Sin Dato", "ilegible", "sin dato", "ILEGIBLE", "SIN DATO", "Ilegible", "Sin Dato", "", " "), 0, PRD))

results_2018 <- results_2018 %>%
  mutate(PRD = as.numeric(sub(",", "", PRD)))

unique(results_2018$PRD)

unique(results_2018$PRI)

results_2018 <- results_2018 %>%
  mutate(PRI = ifelse(PRI %in% c("Sin dato", "N/R", "Sin Dato", "ilegible", "sin dato", "ILEGIBLE", "SIN DATO", "Ilegible", "Sin Dato", "", " "), 0, PRI))

results_2018 <- results_2018 %>%
  mutate(PRI = as.numeric(sub(",", "", PRI)))

unique(results_2018$PRI)

unique(results_2018$MORENA)

results_2018 <- results_2018 %>%
  mutate(MORENA = ifelse(MORENA %in% c("MORENA", "Sin dato", "N/R", "Sin Dato", "ilegible", "sin dato", "ILEGIBLE", "SIN DATO", "Ilegible", "Sin Dato", "", " "), 0, MORENA))

results_2018 <- results_2018 %>%
  mutate(MORENA = as.numeric(sub(",", "", MORENA)))

unique(results_2018$MORENA)


#This is to create the CVEGEO that will allow us to merge with he map database
results_2018$CVEGEO <- paste0(str_pad(results_2018$ID_ESTADO, 2, pad = "0"), str_pad(results_2018$ID_MUNICIPIO, 3, pad = "0"))


res_2018_clean <- results_2018 %>%
  group_by(CVEGEO) %>%
  summarise(PAN_18 = sum(PAN),
            PRD_18 = sum(PRD),
            PRI_18 = sum(PRI),
            MORENA_18 = sum(MORENA))

res_2018_clean <- res_2018_clean %>%
  mutate(more_votes_18 = if_else(PAN_18 > PRD_18 & PAN_18 > PRI_18 & PAN_18 > MORENA_18, "PAN",
                              if_else(PRD_18 > PAN_18 & PRD_18 > PRI_18 & PRD_18 > MORENA_18, "PRD",
                                      if_else(PRI_18 > PAN_18 & PRI_18 > PRD_18 & PRI_18 > MORENA_18, "PRI", "MORENA"))))

res_2018_clean$CVEGEO[20] <- "03008"
res_2018_clean$CVEGEO[21] <- "03009"

#This data test gatther the information of the SHP file of the mexican municipalities, the information about different variables of interest of social vulnerability and the control variables like people that is no poor and no vulnerable. It also has the voting results per individual party where are considered the main 4 national parties.
datatest1 <- merge(poverty_15_20, res_2018_clean, by = "CVEGEO", all = TRUE)

map <- shapefile("MG_INTEGRADO_2020/conjunto_de_datos/00mun.shp") 

map1 <- merge(map, res_2018_clean, by = "CVEGEO")

data_map1 <- as.data.frame(map1)


#THIS IS THE MAP OF THE RESULTS IN 2018
ggplot() +
  annotation_spatial(map1) +
  layer_spatial(map1, aes(fill = more_votes)) +
  scale_fill_manual(values = c("PAN" = "blue", "PRD" = "yellow", "PRI" = "red", "MORENA" = "brown")) +
  theme_minimal()

##################
##################
##################RESULTS OF 2021

results_2021_list <- list.files("2021")
results_2021_list

results_2021 <- data.frame()
for (i in 1:length(results_2021_list)) {
  temp<-read.csv(paste0("2021/",results_2021_list[i]))
  temp <- temp %>%
    select(ID_ESTADO,ESTADO, ID_MUNICIPIO, MUNICIPIO, PAN, PRD, PRI, MORENA)
  results_2021 <- rbind(results_2021, temp)
}

unique(results_2021$PAN)

results_2021 <- results_2021 %>%
  mutate(PAN = ifelse(PAN %in% c("Sin acta", "No identificada", "SIN ACTA", " ", "PRI", "PAN", "N/R", "Ilegible", "Sin dato", "ILEGIBLE", "SIN DATO", "-", "ilegible", "sin dato", ""), 0, PAN))

results_2021 <- results_2021 %>%
  mutate(PAN = as.numeric(sub(",", "", PAN)))

results_2021[is.na(results_2021)] <- 0

unique(results_2021$PAN)

unique(results_2021$PRD)

results_2021 <- results_2021 %>%
  mutate(PRD = ifelse(PRD %in% c("SIN ACTA", "No identificada", "Sin acta", "Sin Dato", "Ilegible", "Sin dato", "-", "PRD", "ILEGIBLE", "SIN DATO", "ilegible", "sin dato", "N/R", "", " "), 0, PRD))

results_2021 <- results_2021 %>%
  mutate(PRD = as.numeric(sub(",", "", PRD)))

unique(results_2021$PRD)

unique(results_2021$PRI)

results_2021 <- results_2021 %>%
  mutate(PRI = ifelse(PRI %in% c("SIN ACTA", "No identificada", "Sin acta", "PRI", "Sin Dato", "Ilegible", "Sin Acta", "ILEGIBLE", "SIN DATO", "-", "sin dato", "ilegible","", " "), 0, PRI))

results_2021 <- results_2021 %>%
  mutate(PRI = as.numeric(sub(",", "", PRI)))

unique(results_2021$PRI)

unique(results_2021$MORENA)

results_2021 <- results_2021 %>%
  mutate(MORENA = ifelse(MORENA %in% c("SIN ACTA", "Sin acta", "No identificada", "N/R", "Sin Dato", "Ilegible", "MORENA", "Sin Acta", "Sin dato", "Sin Acta", "SIN DATO", "ILEGIBLE", "-", "ilegible", "sin dato", ""), 0, MORENA))

results_2021 <- results_2021 %>%
  mutate(MORENA = as.numeric(sub(",", "", MORENA)))

unique(results_2021$MORENA)

#This is to create the CVEGEO that will allow us to merge with he map database
results_2021$CVEGEO <- paste0(str_pad(results_2021$ID_ESTADO, 2, pad = "0"), str_pad(results_2021$ID_MUNICIPIO, 3, pad = "0"))

res_2021_clean <- results_2021 %>%
  group_by(CVEGEO) %>%
  summarise(PAN_21 = sum(PAN),
            PRD_21 = sum(PRD),
            PRI_21 = sum(PRI),
            MORENA_21 = sum(MORENA))

res_2021_clean <- res_2021_clean %>%
  mutate(more_votes_21 = if_else(PAN_21 > PRD_21 & PAN_21 > PRI_21 & PAN_21 > MORENA_21, "PAN",
                              if_else(PRD_21 > PAN_21 & PRD_21 > PRI_21 & PRD_21 > MORENA_21, "PRD",
                                      if_else(PRI_21 > PAN_21 & PRI_21 > PRD_21 & PRI_21 > MORENA_21, "PRI", "MORENA"))))

res_2021_clean <- slice(res_2021_clean, -1)
res_2021_clean$CVEGEO[21] <- "03008"


#This data test gatther the information of the SHP file of the mexican municipalities, the information about different variables of interest of social vulnerability and the control variables like people that is no poor and no vulnerable. It also has the voting results per individual party where are considered the main 4 national parties.
datatest_2 <- merge(poverty_15_20, res_2021_clean, by = "CVEGEO", all = TRUE)

final_database <- merge(datatest1, res_2021_clean, by = "CVEGEO", all = TRUE)

final_database_1 <- final_database %>%
  mutate(winner_18 = ifelse(more_votes_18 == "PAN", 1,
                         ifelse(more_votes_18 == "PRI", 2,
                                ifelse(more_votes_18 == "PRD", 3,
                                       ifelse(more_votes_18 == "MORENA", 4, NA)))),
         winner_21 = ifelse(more_votes_21 == "PAN", 1,
                                   ifelse(more_votes_21 == "PRI", 2,
                                          ifelse(more_votes_21 == "PRD", 3,
                                                 ifelse(more_votes_21 == "MORENA", 4, NA))))
         )

model_2018 <- lm(winner_18 ~ Población2015 + Porcentaje_de_pobreza_2015 + Porcentaje_de_pobreza_extrema_2015 + Porcentaje_de_Población_con_al_menos_una_carencia_social_2015 +
                   Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2015 + Porcentaje_de_personas_con_rezago_educativo_2015 + Porcentaje_de_personas_vulnerables_por_ingreso_2015 +
                   Porcentaje_de_personas_no_pobres_y_no_vulnerables_2015 + Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2015 + Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2015 +
                   Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2015 + Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2015, data = final_database_1)
summary(model_2018)

model_2021 <- lm(winner_21 ~ Población2020 + Porcentaje_de_pobreza_2020 + Porcentaje_de_pobreza_extrema_2020 + Porcentaje_de_Población_con_al_menos_una_carencia_social_2020 +
                   Porcentaje_de_Población_con_tres_o_más_carencias_sociales_2020 + Porcentaje_de_personas_con_rezago_educativo_2020 + Porcentaje_de_personas_vulnerables_por_ingreso_2020 +
                   Porcentaje_de_personas_no_pobres_y_no_vulnerables_2020 + Porcentaje_de_personas_con_Carencia_por_acceso_a_la_seguridad_social_2020 + Porcentaje_de_personas_con_Carencia_por_acceso_a_los_servicios_de_salud_2020 +
                   Porcentaje_de_personas_con_Carencia_por_calidad_y_espacios_de_la_vivienda_2020 + Porcentaje_de_Población_con_ingreso_inferior_a_la_línea_de_pobreza_por_ingresos_2020, data = final_database_1) 
summary(model_2021)

path <- "C:/Users/erick/OneDrive/Escritorio/FINAL_PROJECT/final_database.xlsx"

write_xlsx(final_database, path = path)
