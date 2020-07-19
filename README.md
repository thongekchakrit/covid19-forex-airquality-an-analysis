# The Impact of the Novel Coronavirus Disease 2019 on the ASEAN Foreign Exchange Rate and Air Quality: Jan 2020 to April 2020.
Date: 29 April 2020

By Chakrit Thong Ek, Master Of Analytics, Massey University School of Business (Singapore)

```
My codes can be found in "notebook" folder
```

## Abstract 

The global outbreak of the COVID-19 had caused countries to lose millions as businesses, tourism, and supply chains were disrupted. These effects can be seen as the global stock market plunged and during this time of crisis, many have sought a silver lining, and countries from around the world have reported obvious improvement in air quality. However, the effect on every country is different. 

In this study, the impact of COVID-19 pandemic on ASEAN foreign exchange rate and air quality were examined. Our result shows that there was a depreciation in Singapore, Indonesia, Malaysia, and Thailand's currencies against the US dollars, while Philippines peso appreciated against the later as investors shifted to governmental bonds. Singapore and Malaysia saw no improvement in their air quality, while Thailand and the Philippines saw an improvement in early April. However, the improvement in Thailand's air quality was most likely unlinked to the pandemic while the Philippines was. The air quality in Indonesia on the other hand, may worsen as she enters her 'fire season' in April.

## 1. Introduction

The outbreak of a novel coronavirus infection (COVID-19) on 31st December 2019 in the city of Wuhan China had caused a global pandemic to date. In an attempt to curb the spread of this novel virus, the governmental bodies around the world are imposing a strict nationwide quarantine or are reviewing various lockdown measures (Lippi, Henry, & Sanchis-Gomar; The, 2020). These measures have led to the closure of many factories, schools, non-essential services, hotels and the implementation of travel restrictions worldwide.

The COVID-19 had disrupted global trade, supply chains and depressed asset prices (Ayittey, Ayittey, Chiwero, Kamasah, & Dzuvor, 2020). This will most likely cause an economic shock that will ripple throughout the globe for many months to come. 
Being one of the first few countries to be hit with the pandemic, countries in the Association of Southeast Asian Nations (ASEAN) may be hit hard by the economic downturn. What then in ASEAN had been affected? Did this economic meltdown lead to a loss of confidence in the ASEAN market?  

In this study, the impact of COVID-19 on ASEAN foreign exchange were analyzed. In addition, due to the closure of factories, we looked at the impact of COVID-19 on air quality. To do so, the questions below will be answered.

### Exploratory Data Analysis (EDA) Questions

The goal of EDA questions was to help us understand our data, below are the explorative questions.

1. The COVID-19 Pandemic January to April 2020 
    * Which ASEAN member had the highest number of confirmed case of COVID-19?
2. The exchange rate of ASEAN members
    * What were the exchange rates before COVID-19 Pandemic?
3. Air quality in ASEAN countries
    * How was the air quality before COVID-19 Pandemic?
    
### Research Question

1. What was the impact of COVID-19 on ASEAN foreign exchange rate and air quality?

__Term__

ASEAN: The association of Southeast Asian Nation is a regional grouping that consists of Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar (Burma), the Philippines, Singapore, Thailand, and Vietnam.

## 2. Methodology

**2.1. Data Sources**

The datasets used in this study had been gathered from many sources. There were 3 main datasets used, (i) The COVID-19 dataset, (ii) the foreign exchange dataset, and (iii) air quality dataset. The breakdown of sources and methods of extraction are listed below.

COVID-19 Dataset. Data extraction method: Data were imported using an API
 - [COVID-19 Dataset]( https://pkgstore.datahub.io/core/covid-19/time-series-19-covid-combined_json/data/875416425fff342abbd7a1fc258e14f8/time-series-19-covid-combined_json.json) (January 22, 2020 to April 13, 2020)
 
 
Foreign Exchange Rates Dataset (USD / ASEAS countries). Data extraction method: Webscrapping of data from yahoo finance
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
 
In response to the questions above, data wrangling and exploratory data analysis were performed in an attempt to analyze the datasets. The following modules were throughout this study: Pandas, numpy, seaborn, matplotlib, matplotlib.pyplot, folium, json, plotly express, request, prettyprint and beautifulsoup.
 
```
The steps taken for data wrangling had been left out. 

The full process can be found using the link at the end of essay.
```

**2.2. Data Acquisition and Data Wrangling**

Firstly, the COVID-19 dataset mentioned in section 2.1. was imported using an API. Next, dataframe was generated from JSON and irrelevant data was removed and columns were renamed and rearranged. Then, the data containing ASEAN countries and changed 'Date' into datatime format.

Next, the Foreign Exchange Rate was scrapped from Yahoo Finance. To do so, we began by defining a function to scrape through yahoo currency of interest. After the creation of currency_extractor function, a list was created to contain the URLs to all ASEAN currencies. Lastly, 2 loops were created to loop the through the URLs and the currencies was converted into a dataframe.

Following the data acquisition from Yahoo finance, the air quality dataset was imported from the CSV file. Next the countries of interest were selected and the variables were formatted to suit the data structure.

## 3. Exploratory Data Analysis and Results

In order for us to gain insight to the impact of COVID-19 on ASEAN foreign exchange rate and air quality, we will start off by answering a few research questions in the exploratory analysis section. During the exploratory data analysis, we will create more questions to aid us in analyzing the datasets.

Here an attempt to explore the data was made, we started off by answering the initial questions mentioned in section 1 (Exploratory Analysis Questions).

**3.1. Covid-19 Pandemic January to April 2020**

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

The percentage of deaths caused by COVID-19 pandemic in Singapore was less than 1 percent, Thailand and Malaysia had an estimate of 2 percent, the Philippines had around 6.5 percent while Indonesia had 9 percent. The Philippines and Indonesia had fatality ratios which were much higher compared to the crude fatality rate, 3.67 percent  (Verity et al.), of COVID-19.

Following the EDA of COVID-19 dataset, we worked shift our focus to the forex exchange.

**3.2. The exchange rates of Indonesia, Malaysia, Philippines, Singapore and Thailand**

In this section, we started off by looking at how these ASEAN currencies were doing prior to the COVID-19 pandemic. This question was meant to help us gather more information on the dataset before deeper analysis can be performed.

The period before any ASEAN member having a death case caused by COVID-19 will be defined as the period before the pandemic. The first recorded death due to COVID-19 was recorded by the Philippine on 2nd February 2020, thus, the period before that will be considered as the period before the pandemic. 

To gain a better insight into the foreign currencies during COVID-19 pandemic, we evaluated the foreign currencies of Malaysian ringgit,Philippines peso, Singapore dollar, Indonesian rupiah and Thai baht with a period of 6 months prior to 31st January 2020 (1st and 2nd February Market closes).

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig5_1_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig5_2_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig5_3_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig5_4_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig5_5_p2.png">

**Trend of exchange rates prior to the COVID-19 Pandemic**

Except for the Singapore dollar and Thai Baht, the foreign exchange rates of United States Dollar to Indonesian Rupiah, Philippine Peso, and Malaysia Ringgit have a downward trend.

From 2nd August 2019 to 1st January 2020, the trend of USD/SGD and USD/THB was a downward trend. During this period, the Singapore dollar and the Thai baht was getting stronger compared to the United States dollar. In this period, the USD/SGD decreased from \$1.38 to \$1.33 and USD/THB decreased from 30.9300฿ to 29.6800฿, which was a huge decrease for both currencies. 

After 1st Jan 2020, however, we witnessed an exponential growth in USD/SGD and USD/THB. In 1 month, respectively, the USD/SGD and USD/THB raised from \$1.33 to \$1.36 and 29.68฿ to 31.12฿.

Malaysia ringgit, Indonesian rupiah, and Philippines peso, on the other hand, grew stronger against the USD over the entire period of 2nd August 2019 to 31st January. 

During this period the USD/IDR, USD/PHP, and USD/MYR decreased from 14,329 to 13,643, 51.30 to 50.84, and 4.14 to 4.08 respectively. The percentage of decrease for each currency exchange against was 4.87 percent IDR, 0.9 percent PHP, and 1.36 percent MYR. 

Analyzing the trend within this time frame, we see a possibility of reversal for Indonesia Rupiah and Malaysian ringgit after mid-January onwards. Although the Philippines had an overall downward trend from 2nd August 2020 to 31st January 2020, however, the Philippines has been having a gradual increase in trend starting in early November 2019.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig6_1_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig6_2_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig6_3_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig6_4_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig6_5_p2.png">

**The trend of the currencies amid the COVID-19 Pandemic**

The market was closed from 1st to 2nd February (weekend)

In Figure 6, we saw an overall increase in trends of USD/IDR, USD/MYR, USD/SGD, and USD/THB which was an increase of 15.9, 5.18, 3.67, and 4.86 percent respectively. It seemed that the pandemic has depreciated the foreign exchange currency. Although it has been documented that USD was not considered a safe haven currency by many researchers  (Jäggi, Schlegel, & Zanetti, 2019; Ranaldo & Söderlind, 2009), in times of global pandemic, US dollar seemed to be stronger compared to the rupiah, Singapore dollar, baht, and ringgit. 

Considering the trend of USD/PHP, it was largely consistent throughout this period. However, the peso faced a sudden upward spike on 3rd March, which was then followed by an unstable market and finally a decline over approximately half a month, resulting in an overall depreciation value of the US dollar by 0.5 percent.

Across these 5 currencies, except for Philippine peso, we can see a distinct depreciation in their currency against the US dollar. 

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig7_p2.png">

**The distinct trend caused by the pandemic**

Looking at Figure 7, it was clear that on average there was an increasing trend towards the first quarter of 2020. Out of the five currencies, four currencies, namely Singapore dollars, Indonesian rupiah, Thai baht, and Malaysia ringgit depreciated against the US dollars. Similarly, for the Philippine peso, there was a depreciation in mid to late March 2020 before increasing again.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig8_p2.png">

Furthermore, Figure 8 showed a strong change in Singapore dollars, Indonesian rupiah, Thai baht, and Malaysia ringgit. The strong change could be seen from the outliers of these currencies. 

This effect was most evident with rupiah and ringgit as both these currencies have lower quartile values, which meant that they were considered stable before the onset of the COVID-19 pandemic. And after the onset of the pandemic, their currency depreciated greatly against US dollars, hence causing a large spike in value, which was reflected by the outliers. Similarly, this could be seen by the Singapore dollar and Thai baht, albeit, Singapore dollars and Thai baht have slightly higher upper quartile mean. 

The Philippines have a higher standard deviation and a bigger margin between the upper and lower quartile. This suggested that the currency of the Philippines was the most volatile against the other currencies.

No actions will be taken against these outliers as removal or changing them would lead to inaccurate analysis. This was likely caused by an external event, which could be presumably be linked to the COVID-19 pandemic.

**3.3. Air quality in SEA**

Before we drive deeper into the relationship between the forex exchange and COVID-19 pandemic, we looked at how the COVID-19 affected air quality in these ASEAN countries as countries around Asia decreased operations of factory, airports, traffic and commercial activities (Leika, 2020). We will also evaluate the air quality of China, as China was the first to suspend her factory operations due to the pandemic.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig9_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig10_p2.PNG">

Image Source: https://aqicn.org/scale/

**Figure 10. Air Quality Index Scale and Color Legend**

Figure 9 suggested that China had a low distribution of particle matter 2.5 and 10 while a high distribution in AQI. 

The mean PM2.5, PM10 and AQI for China from 30th December 2019 to 13th April 2020 were roughly around 105μg/m3, 50μg/m3 and 97 μg/m3 respectively.

Considering the air quality index scale, China on average had an unhealthy level of PM2.5, moderate level of PM10 and AQI.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig11_p2.PNG">

**The trend of air quality index in China and Malaysia from 31st December 2019 to 13th April 2020**

AQI concentrations were only available for China and Malaysia. The visualization in Figure 11 showed a downward trend in the AQI level in China. Starting from late January leading up to early April, we can see that majority of the readings were below 200 μg/m3, which was an improvement in China's air quality index, albeit the level was still in the unhealthy range. 

On 16th February, China saw the lowest recorded concentration of AQI at 25.25μg/m3. As the date increases, we saw a reduction in the concentration of AQI in China, there was a negative correlation between AQI level and recorded time. The improvement in air quality was most likely due to the suspension of the factories during the Chinese new year period and COVID-19 pandemic. 

Malaysia, on the other hand, had a constant AQI trend throughout the period, which was roughly around 45μg/m3 at a healthy level. Malaysia on the 18th of March 2020 (Tashy, 2020) had suspended non-essential operations such as the operation of small businesses and factories. Looking at Figure 11, the trend after 18th March remained the same at a healthy level.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig12_p2.PNG">

PM10 is an inhalable particulate matter which is less than 10 micrometers in diameter and it has a known association with various diseases such as lung cancer and respiratory impairment (Hoek et al., 2012). The result of our study showed no obvious trend in PM10 distribution in Indonesia, Singapore, and the Philippines. In these countries, the trend of PM10 concentration was consistent throughout the recorded period. Thailand and China, on the other hand, have a weak downward trend as we move towards the right of the graph. We could see a drop in PM10 concentration after 28th February in Thailand and January 25th for China.

Singapore, Indonesia, and the Philippines had a desirable PM10 concentration while Thailand and China had a moderate level.

It was interesting to see Thailand air quality improving at the beginning of March. Next, we analyzed Thailand's maximum, minimum and median air quality in different state using the moving average of the indicator.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig13_1_p2.png">

PM10 is an inhalable particulate matter which is less than 10 micrometers in diameter and it has a known association with various diseases such as lung cancer and respiratory impairment (Hoek et al., 2012). The result of our study showed no obvious trend in PM10 distribution in Indonesia, Singapore, and the Philippines. In these countries, the trend of PM10 concentration was consistent throughout the recorded period. Thailand and China, on the other hand, have a weak downward trend as we move towards the right of the graph. We could see a drop in PM10 concentration after 28th February in Thailand and January 25th for China.

Singapore, Indonesia, and the Philippines had a desirable PM10 concentration while Thailand and China had a moderate level.

It was interesting to see Thailand air quality improving at the beginning of March. Next, we analyzed Thailand's maximum, minimum and median air quality in different state using the moving average of the indicator.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig13_2_p2.png">

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig13_3_p2.png">

Air pollution has been a constant problem in Thailand, especially when after harvesting season. The spike seen above are mostly caused by forest fires, wild fires and the burning off of crops after harvesting season. The air pollution in Chiang Mai started to worsen at the start of February. While Bangkok air pollution worsen in April as PM10 concentration raised.

The highest PM10 and PM2.5 concentrations recorded during this period was 630μg/m³ and 675μg/m³, both belonged to Chiang Mai.

Looking at Figure 13 A, B and C, it was evident that the air quality in Thailand were heavily influence by burning of crops after harvesting season, wild fire and forest fire. Perhaps the improvement in air quality shown in Figure 12 were due to the actions of the local authorities in combating the fires instead of COVID-19 pandemic.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig14_p2.PNG">

PM2.5 has been revealed by scientists having a significant correlation to respiratory morbidity and mortality(Brunekreef & Holgate, 2002). In the European Union, it was found that PM2.5 decreased the average life of those affected by 8.6 months(Orru et al., 2011; Xing, Xu, Shi, & Lian, 2016). Hence, it is important to access the concentration of PM2.5. 

The result of this study revealed a negative correlation of PM2.5 against time in China, while Thailand has a decrease in PM2.5 value after 1st March. Thailand, Indonesia, and China have a similar distribution of PM2.5 concentrations at an unhealthy for sensitive people. Singapore, on the other hand, had a good to moderate concentration of PM2.5.

**Trends of air PM2.5, PM10, and AQI during the COVID-19 pandemic**

Most ASEAN countries did not have an obvious reduction in air pollutants. Singapore, Indonesia, and the Philippines have a constant pattern to the distribution of pollutant concentrations. Singapore, Indonesia, and the Philippines until 13th April were under partial lockdown, with the Philippines having a third of their operations shut (Straitstimes, 2020), however, despite the lockdown, the pollutant concentrations did not decrease. 

Thailand was in partial lock-down since 26th March 2020 (Rogovin, 2020), however, their factories and essential services were still in operation. The reduction of air pollution in Thailand was unlikely linked to the operation of factories. Looking at Figure 13A, B and C, we can see that the cause of air pollution in Thailand was due to burning of crops after harvesting season, wild fire and forest fire. The improvement in air quality were unlikely linked to the cause of COVID-19 pandemic.

In China, it was clear that the pandemic had caused a reduction in air pollution. In Figure 11, after the 25th of January,  the concentration thereafter of AQI dropped below 200μg/m3. In addition, after the 2nd of February, the highest PM2.5 concentrations China saw was below 120μg/m3. China also saw a reduction in PM10 concentration during the period.

**3.4. The impact of COVID-19 on ASEAN foreign exchange rate and air quality**

Here, the relationship between the COVID-19 pandemic, ASEAN foreign exchange, and air quality was performed.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig15_p2.png">

**3.4.1. Analysis, Results, and Discussion**
- There was a strong positive correlation between Indonesia COVID-19 confirmed cases and Indonesia rupiah depreciation. 
- There was a moderate positive correlation between Singapore COVID-19 confirmed cases and Singapore dollar depreciation. 
- There was a strong positive correlation between Thailand COVID-19 confirmed cases and Thai baht depreciation.
- There was a strong positive correlation between Malaysia COVID-19 confirmed cases and Malaysian ringgit depreciation.
- There was no correlation between Philippine's confirmed cases and the Philippines peso depreciation.
- There was a moderate positive correlation between Philippines peso and the other ASEAN currencies.
- Figure 14 shows a strong positive correlation between Singapore, Thailand, Malaysia, Indonesia, and the Philippines confirmed cases.

The positive correlation between the increase of confirmed cases between these 5 nations was strong, this can be seen in Figure 3, and looking at the geological mapping of these countries, these countries are located around the Malay Peninsula. Looking at Figure 7, we would expect to see a negative correlation between Philippines peso and confirmed cases of COVID-19, however, it was interesting to note that there was no correlation between them. 

Looking at other countries it suggested that there was indeed a strong positive correlation between their currency depreciation and COVID-19 confirmed cases. The depreciation in the currency, maybe due to a loss in confidence of the Asian Market as the Pandemic sweep across its continent or that due to the market dependency on China. The reason why market dependence on China could aggravate the currency depreciation may be due to China being the longest impacted by COVID-19 and China had only recently resumed production. Perhaps amid the pandemic, investors have shifted to the greenback as they feared the ASEAN country might ease their monetary policy to get back on track.

Investors seeking safe havens are moving from stocks to government securities and Philippine government bonds offer relatively higher yields, said BDO Unibank chief investment strategist Jonas Ravelas.

According to Ong (2020) Philippine peso was defying the global rout due to investors were moving from stocks to government securities. Also, the bonds offered by the Philippine government have high yield, hence, investors were more likely to invest in government securities. 

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig16_p2.png">

**The relationship between the number of confirmed cases and PM10 pollutant**

- There was no correlation between China, Indonesia and Singapore PM10 concentration to the number of confirmed cases of COVID-19 infection. 
- There was a moderate degree of negative correlation of Philipines PM10 to her number of confirmed cases of COVID-19 infections.
- There was a moderate degree of negative correlation of Thailand PM10 to her number of confirmed cases of COVID-19 infections.
- China have a weak negative correlation between her PM10 concentration and confirmed number of COVID-19 cases.
- A moderate degree of negative correlation between Philippines PM10 concentration and the confirmed cases of COVID-19 can be seen.

<img class="ui fluid image"  src="https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/images/fig17_p2.png">

**The relationship between the number of confirmed cases and AQI and PM2.5**

- There was no correlation between Malaysia AQI concentration and Malaysia number of confirmed COVID-19 cases.
- There was a strong positive correlation between China AQI concentration and PM2.5 concentration.
- There was a high moderate degree of negative correlation between China AQI concentration and China number of confirmed COVID-19 cases.
- There was a high moderate degree of negative correlation between China PM2.5 concentration and China number of confirmed COVID-19 cases.
- No correlation can be seen with Singapore PM2.5 and Singapore number of confirmed COVID-19 cases.
- A weak positive correlation can be seen between Indonesian PM2.5 concentration and Indonesia number of confirmed COVID-19 cases.
- There was a moderate degree of negative correlation between Thailand PM2.5 concentration and Thailand number of confirmed COVID-19 cases

Figure 17 suggested that the suspension of factories and commercial operations in China had an lead to a decrease of PM10 levels in China. The PM10 similarly to PM2.5 are known to be caused by industrial facilities, automobiles, biomass burning, and fossil fuels used in homes and factories for heating (Rohde & Muller, 2015). As her factory ceased to operate country wide, leading to lesser biomass burning and lesser fossil fuel burning, hence, there was a reduction to PM10. In addition to PM10 concentration, the PM2.5 and AQI concentration had a strong and moderate degree of negative correlation against the number of COVID-19 confirmed cases which supported the notion that China's reduction in pollution was significantly correlated with suspension of the factories.

ASEAN country on the otherhand had gone into partial lockdown, where all services expect essential services ceased to operate. During which, some factories were still operational. Malaysia ceased factory that produce non-essential products on 18th March under the movement control order(MCO). Singapore implemented a stringent implementation and enforcement called the Circuit Breaker Measure on 7th April to combat the pandemic, most non-essential services ceased operations, however, factory production lines are considered essential services, hence, there were no closure of production line. Similarly to Singapore and Malaysia, Indonesia saw no improvement in air pollution as shown in Figure 14. 

In addition to no improvement in air quality, Indonesia concentration of PM2.5 had a weak positive correlation with confirmed cases of COVID-19. The raise in air pollution in Indonesia causing a coincidental correlation with COVID-19 number may be due to Indonesia's 'fire season' which was reported to start in April (Kuo, 2020).

Similarly to Singapore, Thailand factories remained operational, hence, the reduction in pollution was most likely due to actions of Thailand local authorities in combating brunt off of crops, wild fire and forest fire. 

Philippines on the other hand saw an improvement in air pollution, similarly to China, was likely due to the closures of factories and businesses as Philippines enter lockdown. 

## 3. CONCLUSION

Key findings:
1. The top 5 countries with the highest confirmed cases of COVID-19 was Indonesia, Philippines, Malaysia, Singapore, and Thailand
2. Indonesia had an active, recovered and death estimated percentages at 83, 8, and 9 percent respectively.
3. The Philippines had an active, recovered and death estimated percentages at 88.5, 5 and 6.55 percent respectively.
4. Singapore had an active, recovered and death estimated percentages at 73, 20, and 2 percent respectively.
5. Thailand had an active, recovered and death estimated percentages at 48, 50, and 2 percent respectively.
6. Malaysia had an active, recovered and death estimated percentages at 51, 47, and 2 percent respectively.
7. Overall amid the pandemic, Singapore, Thailand, Indonesia and Malaysia currencies depreciated against the US dollars.
8. The Philippines peso appreciated against the US dollars during the pandemic as investors shifted to invest in government bonds.
9. There was a clear trend in the depreciation of Singapore dollar, Thai baht, Indonesian rupiah, and Malaysian ringgit at around mid of January 2020 against the US dollar.
10. Singapore and Malaysia had no improvement in air quality.
11. No correlation between air quality in Singapore, Malaysia and their COVID-19 confirmed cases.
11. Philippines saw a reduction in air pollution after mid March.
12. A moderate degree of negative correlation can be seen between Philippine's PM10 concentration and confirmed cases of COVID-19.
2. Thailand saw a reduction in air pollution after mid March.
13. A moderate negative correlation can be seen between Thailand's PM10 and PM2.5 concentration with confirmed cases of COVID-19.
14. A weak positive correlation can be seen between Indonesia PM2.5 concentration and her confirmed cases of COVID-19. 

In summary, due to the COVID-19 pandemic, the prices of Singapore, Indonesia, Malaysia, and Thailand depreciated against the US dollar. This was likely caused by a loss of confidence in the Asian Market. The currency of the Philippines, on the other hand, appreciated against the US dollar as investors shifted from the stock exchange to governmental bonds due to their higher yield. Thailand and the Philippines like China saw an improvement in air quality in April. However, unlike China and the Philippines, the cause of improvement in air quality in Thailand was most likely linked to her authorities' actions on subduing wildfire, burning of crops and forest fire. Philippines and China both saw an improvement in air quality and the improvement is most likely linked to the suspension of factories, commercial services, and lockdown amid the pandemic. Unlike the rest of the country, Indonesia saw a positive correlation between air pollution and COVID-19 confirmed cases, and this might be due to Indonesia 'fire season' where locals use fire to clear land for agriculture.

## 4. REFERENCES

1. Ayittey, F., Ayittey, M., Chiwero, N., Kamasah, J., & Dzuvor, C. (2020). Economic Impacts of Wuhan 2019‐nCoV on China and the World. Journal of Medical Virology, 92. doi:10.1002/jmv.25706
2. Brunekreef, B., & Holgate, S. T. (2002). Air pollution and health. The Lancet, 360(9341), 1233-1242. Retrieved from https://doi.org/10.1016/S0140-6736(02)11274-8. doi:10.1016/S0140-6736(02)11274-8
3.	Hoek, G., Pattenden, S., Willers, S., Antova, T., Fabianova, E., Braun-Fahrländer, C., . . . Fletcher, T. (2012). PM<sub>10</sub>, and children's respiratory symptoms and lung function in the PATY study. European Respiratory Journal, 40(3), 538-547. Retrieved from https://erj.ersjournals.com/content/erj/40/3/538.full.pdf. doi:10.1183/09031936.00002611
4.	Kuo, F. (2020). Indonesia’s forests battered to a pulp. Asiatimes. Retrieved from https://asiatimes.com/2020/03/indonesias-forests-battered-to-a-pulp/
5.	Kyrkilis, G., Chaloulakou, A., & Kassomenos, P. A. (2007). Development of an aggregate Air Quality Index for an urban Mediterranean agglomeration: relation to potential health effects. Environment international, 33(5), 670-676. Retrieved from http://europepmc.org/abstract/MED/17328954
6.	https://doi.org/10.1016/j.envint.2007.01.010. doi:10.1016/j.envint.2007.01.010
7.	Leika, K. (2020). Here’s how coronavirus has affected Asia’s factories, Financial Journalism. World Economic Forum. Retrieved from https://www.weforum.org/agenda/2020/04/asias-factory-activity-coronavirus/
8.	Lippi, G., Henry, B. M., & Sanchis-Gomar, F. Physical inactivity and cardiovascular disease at the time of coronavirus disease 2019 (COVID-19). European Journal of Preventive Cardiology, 0(0), 2047487320916823. Retrieved from https://journals.sagepub.com/doi/abs/10.1177/2047487320916823. doi:10.1177/2047487320916823
9.	Liu, H., Li, Q., Yu, D., & Gu, Y. (2019). Air Quality Index and Air Pollutant Concentration Prediction Based on Machine Learning Algorithms. Applied Sciences, 9, 4069. doi:10.3390/app9194069
10.	Ong, M. (2020). Why the Philippine peso is defying global rout due to COVID 19. ABS-CBN News. Retrieved from https://news.abs-cbn.com/business/03/10/20/why-the-philippine-peso-is-defying-global-rout-due-to-covid-19
11.	Orru, H., Maasikmets, M., Lai, T., Tamm, T., Kaasik, M., Kimmel, V., . . . Forsberg, B. (2011). Health impacts of particulate matter in five major Estonian towns: main sources of exposure and local differences. Air Quality, Atmosphere & Health, 4(3), 247-258. Retrieved from https://doi.org/10.1007/s11869-010-0075-6. doi:10.1007/s11869-010-0075-6
12.	Rogovin, K. (2020). COVID-19 Impact on Migrant Workers in Thailand. The International Labor Rights Forum. Retrieved from https://laborrights.org/blog/202003/covid-19-impact-migrant-workers-thailand
13.	Rohde, R. A., & Muller, R. A. (2015). Air Pollution in China: Mapping of Concentrations and Sources. PLOS ONE, 10(8), e0135749. Retrieved from https://doi.org/10.1371/journal.pone.0135749. doi:10.1371/journal.pone.0135749
14.	Straitstimes. (2020). In Philippines, lockdown brings out the best, even from those with the least. The Straits Times. Retrieved from https://www.straitstimes.com/world/lockdown-brings-out-the-best-even-from-those-with-the-least
15.	The, L. (2020). COVID-19: too little, too late? The Lancet, 395(10226), 755. Retrieved from https://doi.org/10.1016/S0140-6736(20)30522-5. doi:10.1016/S0140-6736(20)30522-5
16.	Verity, R., Okell, L. C., Dorigatti, I., Winskill, P., Whittaker, C., Imai, N., . . . Ferguson, N. M. Estimates of the severity of coronavirus disease 2019: a model-based analysis. The Lancet Infectious Diseases. Retrieved from https://doi.org/10.1016/S1473-3099(20)30243-7. doi:10.1016/S1473-3099(20)30243-7
17.	World Health Organization. (2020). Novel Coronavirus (2019-nCov) Situation Report -1. Retrieved from https://www.who.int/docs/default-source/coronaviruse/situation-reports/20200121-sitrep-1-2019-ncov.pdf?sfvrsn=20a99c10_4
18.	Xing, Y.-F., Xu, Y.-H., Shi, M.-H., & Lian, Y.-X. (2016). The impact of PM2.5 on the human respiratory system. Journal of thoracic disease, 8(1), E69-E74. Retrieved from https://pubmed.ncbi.nlm.nih.gov/26904255
19.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4740125/. doi:10.3978/j.issn.2072-1439.2016.01.19

## Code

* [Link to code](https://github.com/thongekchakrit/covid19-forex-airquality-an-analysis/blob/master/notebook/Impact%20of%20COVID-19%20on%20Air%20Quality%20and%20foreign%20exchange%20rate%20in%20ASEAN%20countries.ipynb)
