# Texas-Prison-Gerrymandering
Data and analysis for the story <a href=https://www.dallasnews.com/news/investigations/2021/12/15/prison-gerrymandering-how-inmates-are-helping-the-texas-gop-maintain-its-power/">"‘Prison gerrymandering:’ How inmates are helping the Texas GOP maintain its power"</a> published by The Dallas Morning News on December 15, 2021.

## Methodology
To conduct this analysis, The News began with three data files: one from the Texas Department of Criminal Justice with each incarcerated persons’ name, county of charge and the facility where they were housed on March 31, 2020; another from TDCJ showing the location of each prison and a third from the Census Bureau containing the population of every county in 2020. These three files were joined together for analysis.

To conduct the reallocation analysis, The News wrote a script in the Python programming language to loop through every row of the combined data, adding one person to the county where the prisoner was charged and subtracting one person from the county where they were incarcerated, to generate final adjusted populations for every county in Texas.

The News joined a fourth data table showing county election results for 2020, obtained from the Texas Secretary of State’s office, to the combined data.

The first map of prison population was generated by joining a count of all incarcerated adults in every 2020 Census Tract to a Census geospatial file of these tracts in QGIS. This was then exported as a combined shapefile and styled in Tableau.

To conduct the analysis on excluding inmates, The News reduced each district’s population by its total population of incarcerated adults, as counted by the Census Bureau and then adjusted the ideal district size by the total statewide incarcerated population. The News then calculated which districts, by population size, would fall outside of the 10% maximum-minimum population threshold.

To conduct the demographic analysis, The News used the March TDCJ data and 2020 Census Bureau data for adult correctional facilities (group quarters, institutionalized population). This was compared to the 2020 Census Bureau racial demographic data for Anderson County.

The News used the March TDCJ data to determine sentencing and projected release data for Anderson County prisons in state-run facilities. Texas counties with the highest incarceration rates were determined using the 2020 Census Bureau data for adult correctional facilities.

TDCJ provided The News with data of the number of incarcerated people who reported living in specific zip codes prior to incarceration. TDCJ warned this data was incomplete and self-reported. This data was used solely to determine, to the best of The News’ ability, which zip code sent the most people to state-run jails and prisons.
