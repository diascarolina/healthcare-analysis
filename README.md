# Brazilian Public Healthcare Data Analysis
[<img src="https://img.shields.io/badge/author-Carolina%20Dias-ff69b4?style=flat-square"/>](https://github.com/diascarolina) [![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat-square&logo=Jupyter)](https://jupyter.org/try) [![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg?style=flat-square)](https://github.com/diascarolina/healthcare-analysis/blob/main/LICENSE)

![](https://raw.githubusercontent.com/diascarolina/healthcare-analysis/main/other/banner.png?token=AH6WME6YO5QSXJPZKTOZKWDAXL5HG)

# Table of Contents

- [Introduction](#intro)
- [Data](#dt)
- [Methodology](#method)
- [Technologies Used](#tech)
- [Conclusion](#concl)
- [Acknowledgments](#ack)
- [References](#refs)
- [Contact](#contac)

<a name="intro"></a>
# Introduction

Brazil's publicly funded healthcare system, SUS (Sistema Único de Saúde), is the largest nondiscriminatory government-run public health care system in the world. The system is entirely free of any cost at the point of service for any person, including foreigners.[[1]](https://en.wikipedia.org/wiki/Sistema_%C3%9Anico_de_Sa%C3%BAde)

With this in mind, we'll take a look and analyze some datasets from the brazilian public healthcare system, using a "top-down" approach, meaning that we´ll look first in the aspects of the entire country and move on to analyze a specific region (the Northeastern one) and finally change our focus to only one state, the State of Ceará.

> The main notebook with the full analysis and code can be found [here](https://github.com/diascarolina/healthcare-analysis/blob/main/notebooks/healthcare-analysis.ipynb) (in Portuguese).

> A PDF summary of the analysis can be found [here](https://github.com/diascarolina/healthcare-analysis/blob/main/other/analise_sus.pdf) (also in Portuguese). This contains all the text and charts from the main notebook, but none of the code and data cleaning steps, as I felt the code for these parts was becoming too extensive for a quick view.

<a name="dt"></a>
# Data
The data used in this analysis was directly obtained from the official website [DATASUS](https://datasus.saude.gov.br/) on the week of May 22 to May 29 of 2021.
The raw datasets can be found [here](https://github.com/diascarolina/healthcare-analysis/tree/main/data). Please note that the data is constatly being updated, that's why is importante to keep the versions used for the analysis.

The datasets chosen were as follows:
- Number of Hospital Admissions
  - From the whole country
  - Focused only in the State of Ceará
- Total Spending in Hospital Admissions
  - From the whole country
  - From the State of Ceará
- Average Price per Hospital Admission
  - From the whole country
  - From the State of Ceará

All this data ranges from January 2008 to March 2021.

A detailed description of each dataset and its meaning is also provided in the official DATASUS website at [Notas Técnicas (Technical Notes)](http://tabnet.datasus.gov.br/cgi/sih/Proced_hosp_loc_int_2008.pdf)

<a name="method"></a>
# Methodology
We'll proceed in a top-down approach, meaning we will start at the highest level, the country level, and go down focusing on the Northeastern region of Brazil and then on the State of Ceará, comparing its main city and capital, Fortaleza, with the sum of all the other 183 municipalities. Exactly like in the image below:

<p align="center">
  <img width="700" src="https://github.com/diascarolina/healthcare-analysis/blob/main/other/map.png">
</p>

The data was first loaded, then cleaned in order to be analyzed graphically using various charts, giving us a better view of what we have in the datasets.

With this, we were able to obtain many statistics about the relevant variables observed.

<a name="tech"></a>
# Technologies Used

<p align="center">
  <img src="https://github.com/diascarolina/healthcare-analysis/blob/main/other/gif.gif">
</p>

The main .ipynb notebook was produced in Jupyter Lab using Python 3.8.5, mainly for its flexibility and number of features.
The libraries used were:
- Pandas, the backbone of data analysis in Python, used to manipulate datasets;
- Numpy, for manipulation of numpoy arrays;
- Matplotlib, for the plotting of the charts;
- Locale, this was used to change the locale to portuguese in order to use the datetime library correctly;
- Datetime, to convert the dates.

<a name="concl"></a>
# Conclusion
After the analysis, we have arrived at the following conclusions:

**Looking at the number of hospital admissions in Brazil:**
- The State of Ceará is the 9th highest in the number of hospital admissions in Brazil from January 2008 to March 2021, accounting for 4.25% of the country's total admissions, with 6 322 342 total hospital admissions in this period of time;
- The Northeastern Region accounts for 27.29% of the total hospital admissions in Brazil from January 2008 to March 2021;
- Considering only the Northeastern Region, the State of Ceará comes in third in the number of hospital admissions in this period, accounting for 15.57%;
- As observed, the number of hospital admissions has a seasonal variation, with the highs in the months of March to June of every year, and the lows in the months of October to January of each year.

**Looking at the number of total admissions only in the State of Ceará, considering the place of admission:**
- Ceará's capital city, Fortaleza, accounts for 41.62% of all admissions from January 2008 to March 2021;
- The other 183 municipalities in the State account for the other 58.28% in the same period.

**Looking at the number of total admissions only in the State of Ceará, considering the place of residence:**
- 29.12% of all hospital admissions in the State of Ceará are from people living in Fortaleza;
- The other 70,88% are from people living in any of the other 183 municipalities.

Comparing with the total population we have:
- 29.60% of residents of the State of Ceará live in Fortaleza;
- 70.40% of residents of the State of Ceará live in the other 283 municipalities.

With this, we can clearly see the the number of total hospital admissions in the State of Ceará are in accordance with the population.

**Looking at the total spending in hospital admissions in Brazil:**
- The State of Ceará ranks at 10th place in Brazil considering the total spent with hospital admissions from January 2008 to March 2021, and this accounts for 3.88% of the total, or 6 573 100 152.04 BRL;
- The Northeastern Region accounts for 23.46% of the total spent with hospital admissions in Brazil from January 2008 to March 2021;
- Considering only the Northeastern Region, the State of Ceará comes in third in the total spent with hospital admissions in this period, accounting for 16.55%;

**Looking at the total spending in hospital admissions only in the State of Ceará:**
- The total spending with hospital admissions in Ceará's capital, Fortaleza, accounts for 61.77% of the total in the years analyzes;
- All the other 183 municipalities account for the rest 28.23%.

This show the disparity between the cities. Even though Fortaleza has less hospital admissions that the other 183 municipalities combined, it still has the highest total spending in this area.

**Average Price per Hospital Admission in Brazil:**
- The average price per hospital admission is pretty leveled in all the 5 regions.
- The State of Ceará is the 12th highest in the average price per hospital admission from January 2008 to March 2021;
- The Northeastern Region is in 4th place from all 5 regions in Brazil;
- Considering only the Northeastern Region, Ceará comes in at 3rd place.

**Average Price per Hospital Admission only in the State of Ceará:**

Here we can really grasp the diverging amount of money spent in Fortaleza against the other municipalities.
- The average price per hospital admission in Fortaleza is 1 537.72 BRL;
- The average price per hospital admission in the other 183 municipalities is 380.28 BRL.

<a name="ack"></a>
# Acknowledgments
This project was proposed as a first project in the Alura's Data Science Bootcamp, acting as an introduction to the world of Python to obtain insights from data.

<a name="refs"></a>
# References
- [[1] Sistema Único de Saúde](https://en.wikipedia.org/wiki/Sistema_%C3%9Anico_de_Sa%C3%BAde)
- [DATASUS](https://datasus.saude.gov.br/)
- [TABNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02)
- [Alura](https://www.alura.com.br/)
- [Applied Data Science Bootcamp](https://www.alura.com.br/bootcamp/data-science-aplicada/matriculas-abertas)
- [Storytelling with Data](https://www.storytellingwithdata.com/)
- [Storytelling with Data in Python](https://github.com/empathy87/storytelling-with-data#:~:text=storytelling%2Dwith%2Ddata%20(Python%20%2B%20matplotlib),-http%3A%2F%2Fwww&text=The%20book%20storytelling%20with%20data,pivotal%20point%20in%20your%20story.)
- [Numpy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- Banner photo by [Martha Dominguez de Gouveia](https://unsplash.com/@mdominguezfoto?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/photos/nMyM7fxpokE)
  

<a name="contac"></a>
# Contact

Any tips or suggestions? Feel free to contact me!

[<img src="https://img.shields.io/badge/carodias-0A66C2?style=flat-square&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/carodias/) [<img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=Gmail&logoColor=white" />](mailto:carolinadiasw@gmail.com)


