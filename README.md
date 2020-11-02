# ProjectMEDA2002

# A project summary

Unemployment, Hard broken and the loss of family members is the grief that no one wants it to happen. Sometimes a way for people to escape pain or suffering is suicide. Around 800 000 people commit suicide and there are a lot of people who attempt suicide every year. Our project has 4 objectives which are 1. Overall of each country in map and bar chart, 2. Top n countries of average suicide rate Vs year and suicide number Vs year of each country, 3. The total suicide number grouping by ages in each year and 4. The total suicide number grouping by sex in each year. 
The first objective,using the geovisualisation to represent the world map the scale of circle showing the number of average population, the color show number of average suicide and use the bar charts to show suicide number that compares by age in each country and sex. It could be useful to see overview of statistics. The second objective, using the multiple line chart to represent the top n countries of suicide rate. For example, the top 3 countries of suicide rate are Hungary, Lithuania and Russia. Moverover, having suicide number Vs year of each country.The third objective, using the scatterplot to shows the suicide number in each age and in each year. Moreover, using regression line to forecast the suicide future trend.The fourth objective, using the scatterplot to shows the suicide number in each sex and in each year. Moreovr, this visaulisation also has regression line for forecast the suicide future trend. 


# The data source (or a stable link to the data source, say to GitHub).

Source Data : https://github.com/pakcheera/ProjectMEDA/blob/main/who_suicide_statistics.csv
		Or  https://www.kaggle.com/szamil/who-suicide-statistics
		
Cleaning Data : https://github.com/pakcheera/ProjectMEDA/blob/main/cleandata_1.csv
		 ( it also can be generated from R file in the project) 

# Approach: what was selected and what was omitted.

<img width="452" alt="Picture 1" src="https://user-images.githubusercontent.com/73279529/97080505-0eee5200-1626-11eb-9ac3-8afa68317946.png">

We remove all row that have NULL value in Suicide No and Population.

# Contribution of each team member. 

Sasa Manasboonpermpoon 20302647: objective 2 and objective 4

Pakcheera Choppradit 20303349 : objective 1 and objective 3

Both of us helped each other to do Readme.md and slide.


# A clear description of how to execute/run the project and on which platform.

Firstly, we import data (who_suicide_statistics.csv) to R to clean it and save to name Cleandata_1.csv for use in Tableau.

Then we do each objective in following :

R (ggplot2 and plotly) : objective 3 and  objective 4

Tableau :  objective 1 and objective 2.

In R programimg
After we clean the data we import ggplot2 and plotly then we use aggregate function to create Sex table and Age table that sum number of suicide number and population grouping by Sex and Age, respectively. Then we use ggplot to plot graph and add trend line. Finally we use plotly to create the interactive graph. Finally, we export the graphs in html file.

In Tableau tools
Firstly we created calulation fileds which are average population (sum(population)/countd(year)), average suicide number (sum(suicide number)/countd(year)) and suicide rate(average suicide number/average population). Then, we created the treemap to show propotion of female and male, the bar chart that grouping by range of age and the map that show each country. In the map we use the scale of cricle depends on average population and the color depends on the average suicide number. addig the action that zoom the map when click and show the treemap and the bar chart of the clicking country. Then, we created the parameter of top n and the set of it to use in objective 2. We also create the list parameter of name's countries to choose to see it. Moreover we create the new calculate filed ( suicide no. with fill null value ) using to jiont the line garph when we have missing value.



# explain the graph of each objective. 

Objective 1 : Overall of each country in map and bar chart.
<img width="1440" alt="Screen Shot 2020-10-23 at 8 51 23 pm" src="https://i.imgur.com/u5YG5CT.png">

It can choose only one country that you want to see the over all by clicking the name of country in the map. For example, in the graph show suicide statistic that compares by sex and compares by a range of age in each Russia.
<img width="1440" alt="Screen Shot 2020-10-24 at 6 43 23 pm" src="https://i.imgur.com/KCbp2Yh.png">

It can also show the group of country that you want to see the over all by cover the name of countries in the map  like in the picture below.
<img width="1440" alt="Screen Shot 2020-10-24 at 6 44 37 pm" src="https://i.imgur.com/sEETNIz.png">


Object 2 : Top n countries of average suicide rate Vs year and suicide number Vs year of each country. 

In the first graph show the Top n country of suicide number VS year and second graph show the selected country Vs year. Both graphs also show the trend line. 
<img width="1438" alt="Screen Shot 2020-10-24 at 6 49 15 pm" src="https://i.imgur.com/LbFVED3.png">

In the first graph you can change the number of Top n like in the graph below I choose 5. In the second graph it can choose the counrty that you want to see in this case I choose thailand
<img width="1440" alt="Screen Shot 2020-10-24 at 6 49 24 pm" src="https://i.imgur.com/ub5P8aE.png">


Objective 3 : The total suicide number grouping by ages in each year.

<img width="1434" alt="Screen Shot 2020-10-24 at 7 03 34 pm" src="https://user-images.githubusercontent.com/73279529/97081283-8ffc1800-162b-11eb-8cc2-72581aa7f1ec.png">

<img width="1440" alt="Screen Shot 2020-10-24 at 7 05 25 pm" src="https://user-images.githubusercontent.com/73279529/97081305-c174e380-162b-11eb-8eec-3cffbd86dd17.png">

<img width="1435" alt="Screen Shot 2020-10-24 at 7 06 55 pm" src="https://user-images.githubusercontent.com/73279529/97081340-0ac53300-162c-11eb-9035-ca803ab456e8.png">

Objective 4 : The total suicide number grouping by sex in each year. 

<img width="1440" alt="Screen Shot 2020-10-24 at 7 09 05 pm" src="https://user-images.githubusercontent.com/73279529/97081387-5c6dbd80-162c-11eb-8f42-ab5f7b92b68e.png">

<img width="1440" alt="Screen Shot 2020-10-24 at 7 09 12 pm" src="https://user-images.githubusercontent.com/73279529/97081389-5d9eea80-162c-11eb-99ef-32339f6b99f8.png">

<img width="1440" alt="Screen Shot 2020-10-24 at 7 09 19 pm" src="https://user-images.githubusercontent.com/73279529/97081390-5e378100-162c-11eb-83d0-fedfdf2408cd.png">

# Visualisation results. 
Interactive graph of objective 1 :
https://public.tableau.com/shared/TPG6W3Z3D?:display_count=y&:origin=viz_share_link

Interactive graph objective 2 :
https://public.tableau.com/profile/pakcheera.choppradit#!/vizhome/ProjectMEDA/Dashboard2


Picture of objective 3 :

![122318408_390119215452628_4200788995826467428_n](https://user-images.githubusercontent.com/73279529/97108009-29472f00-16fd-11eb-8eb7-a3c935b6210d.png)

Picture of objective 4 :

![122413637_479076103043914_701202544498308207_n](https://user-images.githubusercontent.com/73279529/97108010-2a785c00-16fd-11eb-98d7-94a909c20d6f.png)



# Any final design reflections or observations.

The report has 4 objectives which are :
1. Overall of each country in map and bar chart.
2. Top n countries of average suicide rate Vs year and suicide number Vs year of each country. 
3. The total suicide number grouping by ages in each year.
4. The total suicide number grouping by sex in each year. 

After creating visualisation of all of these objectives, visualisation reflects several things. Firstly, the first objective shows the overall of suicide statistic. Therefore, it is more effective for creating geovisualization with other visualisations in the same frame helps viewer to more understand the detail of suicide data in each country. In this case, we create bar charts for using to compare sex and a range of age in each country. Moreover, the size and color of circle that located in each country depend on the suicide number. By in the country that has a large suicide number has the big and dark red circle such as Russia. Whereas, the country that has a small suicide number has the small and light yellow circle such as Denmark. furthermore, it could custome the zone of country that interested in to see the suicide statistics. 

Secondly, the country that seem to be peaceful and doesn't has the high competition such as Hungary, Lithuania is one of the country that get one of the highest suicide number. Due to the second visualisation, the most 3 countries that commit suicide are Hungary, Lithuania and Russia respectively. Moreover, this visualisation is able to forecast the future trend in each country. According to the second visualisation, Russia and Hungary have lower trend to commit suicide in the future whereas Lithuania seems to remain constant have trend to commit suicidein the future. Moreover, if you are intrested only in some country, you can see the selected country too in the below graph. 

Next, age range also has effect to commit suicide. According to the third visualisation the age that has the highest suicide number is 35-54 years, whereas the age range that has the lowest suicide number is 5-14 years.

Lastly, sex has effect to comit the suicide. According to the fourth visualisation, male has obviously higher suicide number than female.

In conclusion, sex, age and country have effect to commit the suicide. There are not only adult to commit the suicide but children(5-14 years) also commit suicide too. Do not forget to pay attention to intimates, suicide might be closer that you think. 

