
# Air Accidents Analysis using D3
![image](https://user-images.githubusercontent.com/88155960/180509644-1a9dfe85-df92-4551-8c6b-8f36a0108193.png)

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

