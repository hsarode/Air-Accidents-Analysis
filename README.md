
# Air Accidents Analysis using D3
![image](https://user-images.githubusercontent.com/88155960/180510661-49b0c0b6-cd6b-4ce0-ac57-0126f83dfe00.png)

Two datasets from kaggle are used to display the visualization and 
can be found at [Dataset 1](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses)
and [Dataset 2](https://www.kaggle.com/datasets/saurograndi/airplane-crashes-since-1908).

This dashboard visualizes the crashes that have occurred from 
1901 till 2021. The dashboard has 6 major graphs, three of them 
being bar charts, one line graph and two donut charts. The donut 
charts display the number of crashes based on the day of week 
and the month of the year separately. This done to analyse which 
days of the week and which months of year have higher crash rates.

Coming to the line graph, it displays the history of crashes and fatalities per year from 1901 till 2021. Dark blue line represents the number of crashes per year and light blue line displays number of deaths per year. The line graph is multipurpose. When user clicks on any bar from the three bar graphs, the line graph updates to display the number of crashes in dark blue and the number of deaths in light blue for the same category that the bar was displaying.

Coming to the bar graphs, we have one major bar graph that is the largest graph in this dashboard. It tells us about fatality rate per accident i.e., the number of people that die on average whenever a crash occurs. This is done to visualize the most dangerous categories that cause deaths.

The bar graph with the title “Crash Rate” displays the number of crashes per category and the bar graph with the title “Death Rate” displays the percentage of passengers that die whenever an accident occurs for example 50% of the passengers die when there is crash from the selected category.

Then the dashboard has three buttons namely “Phase of Flight”, “Carrier Wise”, “Flight Wise”, and “Reset”. The first button displays all the crashes and deaths related to the phase of flight. Phase of flight is defined as current manoeuvre the flight is performing. A few examples of phase of flight are “climb” i.e., when the plane is climbing, or gaining altitude just after take-off, “approach” i.e., when the plane is approaching an airport for landing, “go-around” i.e., when a place cannot land and must redo a landing attempt etc.

The second button displays all the crashes and deaths related to the air carrier that crashed. Air carrier is the airline that was operating that aircraft.

The third button displays all the crashes and deaths by the type of flight that crashed. We don’t have just commercial airplanes data in the dataset. It has data from skydiving crashes, test flights, air shows, federal flights, business flights etc.

The fourth button is reset. This button sets the dashboard to original state by clearing out all filters.

Whenever any graph updates a small red circle appears on the top-right side of that graph to indicate that this graph is newly generated. Old graphs do not have a red circle on the top-right. 
## Features

- Cross interactivity between all graphs
- Brushing possible on line graphs
- Data filtering by clicking on the data point
- Mouse click and hover events to display more information


## Run Locally

To visualize this dashboard, open the HTML file in any live server. For 
Visual Studio Code users, an extension called live server is available
that can be used. Once live server has been installed, right click on the file
and click "Open with Live Server" and the dasboard will display 
in your web browser.
## Screenshots

A few examples of mouse events and interactivity have been demonstrated below
### Pie Chart

![image](https://user-images.githubusercontent.com/88155960/180511185-c1f49b1b-82f6-44c3-8581-416eef9e250a.png)

We start off with donut charts on the top right-hand side. The donut charts represent crashes per day of the week and per month of the year. When hovered upon any section of the donut chart, the percentage of crashes that took place on that day and the number of crashes that took place in that month are displayed at the centre of the donut. That hovered section of the donut gets highlighted, and the other sections get faded. Furthermore, a user can also click on any section of the donut chart and that section will remain highlighted. The highlighted section stays highlighted until a user double clicks on the donut chart. After double-click, the pie chart is reset with no highlight and text elements.
### Line Graph

The line graph at the bottom right of the dashboard displays the number of crashes and deaths per year. Brushing is applied on the line graph and a user can brush on any time-period in the line graph.

![image](https://user-images.githubusercontent.com/88155960/180512019-0501783d-7e8c-4ac1-b6a7-127795796c99.png)

Brushing on the line graph also filters the bar charts to display the data between the selected time period only. For instance in the above example, we have brushed over the area between 1985 to 2005. Thus, all our bar graphs will also filter to display data only between 1985 and 2005. This is useful if one wants to analyse crashes between specific year ranges.
### Bar Graph

![image](https://user-images.githubusercontent.com/88155960/180512513-d368e477-3041-4aad-9319-22772f45df3e.png)

All the bar graphs have interactivity embedded into them. Whenever a bar is hovered upon in any graph, bars that represent data from the same category are highlighted in the other 2 graphs as well. All the other bars fade. Upon mouseover, the data that the bar represents is also displayed on top of the bar for all the highlighted bars.
Whenever any bar is clicked upon, they line graph at the bottom right of the dashboard filters to show the crashes and deaths from the selected category only. For instance, in the above picture, we have selected “Descent” which indicates crashes and fatality rate when the aircraft is lowering altitude to land. When this bar is clicked upon, the bottom right graph filters to display crashes and deaths only from “Descent” stage of flight as seen below. The light blue line indicates deaths, and the dark blue line indicates crashes.

![image](https://user-images.githubusercontent.com/88155960/180513697-9da0547b-2828-4d46-98d8-2e5af4753c45.png)

### Line graph – after click event on bar

![image](https://user-images.githubusercontent.com/88155960/180513883-344d3b62-ad55-4b44-90b6-d98fc54b4d3c.png)

The newly generated line graph is also interactive. The data from each year is marked with a circle to easily access that information. Whenever mouse if hovered upon any of the circle, it is highlighted and the same circle from the other line is also highlighted. Also, the data point of that circle is displayed as text above the circle on mouseover.

## Insights
### Crashes on days of week and months in a year
Looking at the donut charts, we can observe that majority of the crashes have occurred on Saturday and Sunday. This implies more flights fly on weekends and people prefer to fly on weekends possibly due to reduced workload. We can also notice that there is a peak in aircraft crashes during mid-year i.e., June, July, and August. The high percentage of crashes during mid-year are a direct result of increase in passenger traffic due to the summer and spring breaks.
### Crashes and deaths related to phase of flight
Coming to the phase of flight, we can observe that majority of the crashes occur during the landing and take off phase of a flight followed by others. However, despite landing and take-off contributing to the greatest number of crashes, we observe that the fatality rate is surprisingly low for those two phases. This indicates that crashes that occur during take-off and landing are not as fatal. This is because take-off and landing occur near the airport and if the plane was to crash, emergency services are ready to be deployed instantly, thus saving more lives. On the contrary we notice that the climb phase of a flight has the highest fatality rate if an accident occurs despite having only 2000 crashes overall.
### Crashes and deaths by air carriers
We observe that American, United and Delta airlines has the highest number of crashes in the history of aviation. This is majorly because a lot of the data is from United States, and these are American airliners. The fatality rate for United airlines is also high indicating that it has a very poor safety record and is not recommended for flying. American airlines and Delta airlines despite having high number of crashes have relatively lesser fatality rates and death percentages indicating a decent safety record. Air Canada and Usair too have very less number of crashes yet their fatality rate is quite high which implies a poor safety record. Delta airlines on the other hand have 0 fatality rate despite having many accidents (129) which tells us that the crew of Delta airlines are well trained and equipped in the event of a crash. Other airliners need to train their crew more rigorously for handling crashes.
Out of the ordinary we notice that the fatality rate (1.56) and death percentage (around 67%) is exceptionally high for private charter planes. The only explanation for this would be that charter flights usually have less than 10 passengers and the plane is not as structurally sound as a commercial airliner thus, in the event of crash, it is likely that majority of the passengers die which explains the high fatality rate and death percentage.
### Crashes and deaths by type of flight
We immediately notice that the crash rate of the personal charter flights is the highest followed by others. However, personal charter flights don’t have a high fatality rate nor a high death percentage compared to other flight activities. On the contrary we note that skydiving has the highest fatality rate despite having the least number of crashes which makes skydiving the most dangerous activity to perform. Observing the death rate graph, we see that air race shows, ferries and skydiving have the highest percentage of people who die. Thus, we can assume that these 3 activities are dangerous and should be performed with utmost care and the passengers and crew must be trained well to avoid crashes and handle them well if they occur.
Overall, we can observe that the number of crashes and deaths have gone down significantly indicating an increase in safety measures and technological advances in the field of aviation. Air travel nowadays has become the safest forms of travel.
### Critical Analysis
The developed dashboard does not include all the data from the dataset. There is data about the country, name of the airport, the weather conditions, the model of the plane and the number of engines that were on the plane. However, upon conducting EDA it was observed that majority of the data was from United States, majority of the data for number of engines was 2, majority of the weather data was unknown and there were too many airport and plane model names to plot in an efficient manner due to lack of space. Thus, these columns have not been included in the dashboard.
Coming to donut charts, whenever any section of the donut chart is clicked upon, the line graph does not update to show deaths and crashes from that section only. There may be a pattern between the selected day of the week or month of year and the year when the crash occurs that could be important to make air travel safer.
The line graph that is displayed whenever a user clicks upon a bar does not incorporate the time range set when user has performed brushing. For instance, if the user brushes over a time period from 1990 to 2010, the data that is displayed when a bar chart is clicked upon is not filtered to be in-between 1990 and 2010 only. Instead, all the data is displayed that exists for that category. However, since not all categories have data from all the years, there is no specific need to filter the data upon brushing. 
Finally, in some cases when the bars below the title of the graph are too tall, mouseover events that display the data value of the bar overlap with the title and are not easy to read. This can be easily fixed by adding more padding between the title and the graph.
