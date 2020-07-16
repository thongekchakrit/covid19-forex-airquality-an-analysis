# The Impact of the Novel Coronavirus Disease 2019 on the ASEAN Foreign Exchange Rate and Air Quality: Jan 2020 to April 2020.
By Chakrit Thong Ek, Master Of Analytics, Massey University School of Business (Singapore)

## Abstract 

The global outbreak of the COVID-19 had caused countries to lose millions as businesses, tourism, and supply chains were disrupted. These effects can be seen as the global stock market plunged and during this time of crisis, many have sought a silver lining, and countries from around the world have reported obvious improvement in air quality. However, the effect on every country is different. 

In this study, the impact of COVID-19 pandemic on ASEAN foreign exchange rate and air quality were examined. Our result showed that due to the pandemic, there was a depreciation in Singapore, Indonesia, Malaysia, and Thailand's currencies against the US dollars, while Philippines peso appreciated against the later as investors shifted to governmental bonds. Singapore and Malaysia saw no improvement in air quality, while Thailand and the Philippines saw an improvement in their air quality starting in April 2020. However, the improvement in Thailand's air quality was most likely unlinked to the pandemic while the Philippines was. Indonesia amongst the other country may see a worsening effect on their air quality as she enters her 'fire season' unless actions are taken against the burning of crops.

## 1. Introduction

The outbreak of a novel coronavirus infection (COVID-19) on 31st December 2019 in the city of Wuhan China had caused a global pandemic to date. In an attempt to curb the spread of this novel virus, the governmental bodies around the world are imposing a strict nationwide quarantine or are reviewing various lockdown measures (Lippi, Henry, & Sanchis-Gomar; The, 2020). These measures have led to the closure of many factories, schools, non-essential services, hotels and the implementation of travel restrictions worldwide.

The COVID-19 had disrupted global trade, supply chains and depressed asset prices (Ayittey, Ayittey, Chiwero, Kamasah, & Dzuvor, 2020). This will most likely cause an economic shock that will ripple throughout the globe for many months to come. 
Being one of the first few countries to be hit with the pandemic, countries in the Association of Southeast Asian Nations (ASEAN) may be hit hard by the economic downturn. What then in ASEAN had been affected? Did this economic meltdown lead to a loss of confidence in the ASEAN market?  

In this study, the impact of COVID-19 on ASEAN foreign exchange were analyzed. In addition, due to the closure of factories, we looked at the impact of COVID-19 on air quality. To do so, the questions below will be answered.

### Exploratory Data Analysis (EDA) Questions

The goal of EDA questions is to help us understand our data, here we will set the initial questions for us to answer in order to gain more knowledge on the data.

1. The COVID-19 Pandemic January to April 2020 
    - Which ASEAN member had the highest number of confirmed case of COVID-19?
2. The exchange rate of ASEAN members
    - What were the exchange rates before COVID-19 Pandemic?
3. Air quality in ASEAN countries
    - How was the air quality before COVID-19 Pandemic?
    
### Research Question

1. What was the impact of COVID-19 on ASEAN foreign exchange rate and air quality?

__Terms__

ASEAN: The association of Southeast Asian Nation is a regional grouping that consists of Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar (Burma), the Philippines, Singapore, Thailand, and Vietnam.

### Exploratory Data Analysis (EDA) Questions

The goal of EDA questions is to help us understand our data, here we will set the initial questions for us to answer in order to gain more knowledge on the data.

1. The COVID-19 Pandemic January to April 2020 
    * Which ASEAN member had the highest number of confirmed case of COVID-19?
2. The exchange rate of ASEAN members
    * What were the exchange rates before COVID-19 Pandemic?
3. Air quality in ASEAN countries
    * How was the air quality before COVID-19 Pandemic?
    
### Research Question

1. What was the impact of COVID-19 on ASEAN foreign exchange rate and air quality?

__Terms__

ASEAN: The association of Southeast Asian Nation is a regional grouping that consists of Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar (Burma), the Philippines, Singapore, Thailand, and Vietnam.

## 2. Methodology and EDA 

**2.1. Data Sources**

The datasets used in this study has been gathered from many sources. There are 3 main datasets used, (i) The COVID-19 dataset, (ii) the foreign exchange dataset, and (iii) air quality dataset. The breakdown of sources and methods of extraction are listed below.

COVID-19 Dataset. Data extraction method: Data imported using API
 - [COVID-19 Dataset]( https://pkgstore.datahub.io/core/covid-19/time-series-19-covid-combined_json/data/875416425fff342abbd7a1fc258e14f8/time-series-19-covid-combined_json.json) (January 22, 2020 to April 13, 2020)
 
 
Foreign Exchange Rates Dataset (USD / ASEAS countries). Data extraction method: Webscrapping of data from website
 - [Brunei]( https://finance.yahoo.com/quote/BND%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Cambodia]( https://finance.yahoo.com/quote/KHR%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Indonesia]( https://finance.yahoo.com/quote/IDR%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Laos]( https://finance.yahoo.com/quote/USDLAK%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Malaysia]( https://finance.yahoo.com/quote/MYR%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Myanmar]( https://finance.yahoo.com/quote/MMK%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Philippines]( https://finance.yahoo.com/quote/PHP%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Singapore]( https://finance.yahoo.com/quote/SGD%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Thailand]( https://finance.yahoo.com/quote/THB%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)
 - [Vietnam]( https://finance.yahoo.com/quote/VND%3DX/history?period1=1549065600&period2=1586736000&interval=1d&filter=history&frequency=1d) (Feb 2nd, 2019 to April 13, 2020)


Air Quality Dataset. Data extraction method: Import data from CSV file
 - [Air Quality Open Data Platform]( https://aqicn.org/data-platform/covid19/) (December 30, 2020 to April 13, 2020)
 
In response to the questions above, data wrangling and exploratory data analysis was performed in an attempt to analyze the datasets. The following modules was throughout this study: Pandas, numpy, seaborn, matplotlib, matplotlib.pyplot, folium, json, plotly express, request, prettyprint and beautifulsoup.
 
```
The steps taken for data wrangling has been left out. 

The full process can be found using the link at the end of essay.
```

**2.1.1. Data Acquisition and Data Wrangling**

Firstly, the COVID-19 dataset mentioned in section 2.1. was imported using an API. Next, dataframe was generated from JSON and irrelevant data was removed and columns were renamed and rearranged. Then, the data containing ASEAN countries and changed 'Date' into datatime format.

Next, the Foreign Exchange Rate was scrapped from Yahoo Finance. To do so, we began by defining a function to scrape through yahoo currency of interest. After the creation of currency_extractor function, a list was created to contain the URLs to all ASEAN currencies. Lastly, 2 loops were created to loop the through the URLs and the currencies was converted into a dataframe.

Following the data acquisition from Yahoo finance, the air quality dataset was imported from the CSV file. Next the countries of interest were selected and the variables were formatted to suit the data structure.

**2.2. Exploratory Data Analysis**

In order for us to gain insights to the impact of COVID-19 on ASEAN foreign exchange rate and air quality, we will start off by answering a few research questions in the exploratory analysis section. During the exploratory data analysis, we will create more questions to aid us in analyzing the datasets.

Here an attempt to explore the data was made, we started off by answering the initial questions mentioned in section 1 (Exploratory Analysis Questions).

**2.2.1. Covid-19 Pandemic January to April 2020**

In this section, we aimed to find the country with the highest number of COVID cases. This question was meant to help us gather more information on the dataset before deeper analysis could be performed.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig1_p2.png">

**The highest and lowest number of confirmed cases**

Looking at the graph above, we can see that the highest confirmed cases belonged to Philippines , followed by Malaysia, Indonesia, Singapore and Thailand. Vietnam, Brunei, Cambodia, Burma and Laos had relatively lower number compared to the former group. Laos had 19 confirmed cases by the end of April 13th, this was much lower in comparison to Philippines , Malaysia, Indonesia, Singapore and Thailand. There was a contrast between the upper and lower half of the countries, the number of confirmed cases of the lower and upper quantile (Thailand and Vietnam) were approximately 10 times the size.

This graph does not, however, tell us which countries were the first to detect the virus.The question we can ask next was which country was the first to detect the virus on their shore. To best represent this, I think an animated bar graph would best satisfy the condition.

<p align="center">
  <img width="798" height="336" src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig2_p2.gif">
</p>

**The first Country to detect the virus on her shore**

The first ASEAN member that detected COVID-19 was Thailand, following that on 23rd of January, Singapore and Vietnam had their confirmed cases. By the end of January, six ASEAN members in total had confirmed cases of COVID-19. These six members were Cambodia, Malaysia, Philippines, Singapore, Thailand and Vietnam, with Thailand having the most number confirmed cases by the end of January. This finding was supported by World Health Organization (2020),who stated that Thailand was amongst the first three nations to report confirmed cases of COVID-19 outside of mainland China.

By the end of April 13th, however,Thailand was not the country with the most number of confirmed cases, this implied that other members of ASEAN had a higher growth rate compared to Thailand.

Thailand, Singapore, Indonesia, Malaysia and Philippines had a significantly large number of confirmed cases compared to Vietnam, Brunei, Cambodia, Burma (Myanmar) and Laos. To help us understand the effect of COVID-19 on the foreign exchange and air quality, the former group were selected for further analysis.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig3_p2.png">

**The growth rate of confirmed, recovered and death cases of Thailand, Singapore, Indonesia, Malaysia and the Philippines**

Looking at the trend of confirmed cases Figure 3(A), by 13th April, Thailand's growth rate seemed to be slowing down. Thailand was ahead of Singapore on confirmed cases count, however, by the 12th of April Singapore overtook Thailand. Between 3rd and 13th April, Singapore's rate of change increased by a great amount, resulting in the detection of more cases compared to Thailand. Both Singapore and Thailand have the lowest death cases amongst these 5 nations and their numbers were 9 and 40 respectively.

Malaysia, on the other hand, had a consistent growth rate, albeit, it was high. By 13th April Malaysia had 4817 confirmed cases, 2276 recovered cases and 77 death.Malaysia had the highest number of recovery rate and the 3rd lowest deaths by COVID-19 (Figure 3A and 3B). The trend of death cases in Malaysia was moderate and her recovered cases were growing exponentially.  

Figure 3 showed that both the Philippines and Indonesia had similar trend. Both these countries started with low number of confirmed cases, however, by 13th April, their numbers were close to 5000 cases. The Philippines and Indonesia’s confirmed cases seems to be growing exponentially starting 17th March. By April 13th, the Philippines and Indonesia had 4932 and 4557 confirmed cases, 242 and 380 recovered cases, and 315 and 399 death cases respectively. Amongst these 5 ASEAN members, the Philippines and Indonesia were the only two countries that had a higher death to recovered ration. The rate of change in death cases in these countries were much higher compared to their recovered cases. 

Looking at the graph above, it suggests that Thailand, Malaysia, and Singapore were efficient in diagnosing COVID-19 infections, which explains why they initially had high number of confirmed cases. The early detection of COVID-19 infection allowed these countries to provide proper medical care to their patient, hence, there were higher recovery cases and lower death rates in those countries. Early detection also allowed these countries to isolate the patient, thereby not allowing the disease to spread further.

Thailand, Malaysia, Singapore, Indonesia, and the Philippines were the ASEAN members that were affected the most by the Pandemic, hence, my focus will be directed to these countries. Next we analyzed the ratio of active, recovered and death cases caused by the pandemic.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig4_p2.png">

**The ratio of active, recovered and death cases per country**

By April 13, Singapore had an estimated 20 percent recovery rate, while Thailand and Malaysia had more than 47 percent. Indonesia and Philipines, had an estimate of 8 and 5 percent respectively. The active cases in Indonesia and the Philippines were the highest with at 83 percent and 88 percent respectively, Singapore had around 79 percent active cases, while Malaysia and Thailand had roughly 51  and 48 percent respectively.

The percentage of deaths caused by COVID-19 pandemic in Singapore was less than 1%, Thailand and Malaysia had an estimate of 2 percent, the Philippines had around 6.5 percent while Indonesia had 9 percent. The Philippines and Indonesia had fatality ratios which were much higher compared to the crude fatality rate, 3.67 percent  (Verity et al.), of COVID-19.

Following the EDA of COVID-19 dataset, we worked shift our focus to the forex exchange.

**... To be continue**
















## Code

* [Link to code](https://github.com/thongekchakrit/life-expectancy-SG/blob/master/notebook/The_Effect_of_Rising_Life_Expectancy.ipynb)
