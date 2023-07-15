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

[Describe your analysis methods and include any visualizations or graphics that you used to present your findings. Explain the insights that you gained from your analysis and how they relate to your research question or problem statement.]

## Results

[Provide a summary of your findings and conclusions, including any recommendations or implications for future research. Be sure to explain how your results address your research question or problem statement.]

## Contributors

Yare Ramirez Garrido - Research, coding and writing
Erick Armando Navarrete Segovia - Research, coding and writing


## Acknowledgments

Professor Torrent (Chung-pei Pien) for his teching in R coding.

## References

Berens, S. (2017). “Taxing Higher Incomes: What Makes the High-Income Earners Consent to More
Progressive Taxation in Latin America?” Political. Behavior 39, 3: 703–29.
Carnes, E. (2013). “Measuring the Individual-Level Determinants of Social Insurance Preferences: Survey
Evidence from the 2008 Argentine Pension Nationalization”. Latin American Research Review 48,
3: 10
Cortina, J. & Gelman, A. (2006). “Income and vote choice in the 2000 Mexican presidential election”.
Social Science Research Network (SSRN).
Feierherd, G. (2021). “Courting Informal Workers: Exclusion, Forbearance, and the Left. American Journal
of Political Science”, December 24. https://onlinelibrary.wiley.com/doi/10.1111/ajps.12576.
Jusidman, C. (2009). “Desigualdad y política social en México. Nueva Sociedad”. Retrieved 25 of June

2023. Source: https://nuso.org/articulo/desigualdad-y-politica-social-en-
mexico/#:~:text=M%C3%A9xico%20sufre%20una%20alta%20desigualdad,%C3%ADndices%2

0de%20desigualdad%20muy%20altos.
Lipset, M. (1960). Political Man: The Social Bases of Politics. Garden City: Doubleday
Lugo Neria, B. (2021). Elecciones de ayuntamientos en Hidalgo (2008-2020): determinantes de la
participación electoral City Council Elections in the State of Hidalgo 2008-2020: The Determinants
of Electoral Participation (Vol. 65).
National Council for the Evaluation of Social Development Policy (Coneval), (2023). “Statistics on

Municipal poverty 2010 – 2020”. Source: https://www.coneval.org.mx/Medicion/Paginas/Pobreza-
municipio-2010-2020.aspx.

National Institute of Statistics and Geography (INEGI). (2023). “Census 2020”. Source:
https://www.inegi.org.mx/programas/ccpv/2020/.
National Electoral Institute (INE). (2023). “Official Sites of the Electoral Local Public Organizations
(OPLEs)”. Source: https://portal.ine.mx/voto-y-elecciones/opl/oples-estados/.
Soto, I. & Cortez, W. (2014). “Determinantes de la participación electoral en México”. Estudios
Sociológicos, 32 (95), 323-353.
Sura-Fonseca, R. (2019). “El vínculo entre la pobreza y la desigualdad con la participación electoral
ciudadana: las elecciones presidenciales de 2006 y 2014 en Costa Rica”. Revista Mexicana de
Ciencias Políticas y Sociales, 64 (235), 189-220.
Vargas, E. (2012). Vulnerabilidad_social_y_comportamiento electoral. Un análisis por secciones
electorales. Universidad Autónoma del Estado de México.
Verba, S. & Nie, H. (1972). Participation in America. Nueva York: Harper and Row.
