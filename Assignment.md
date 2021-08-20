# Assignment 6 | Interactions + Transitions

This assignment focuses on using interactions and transitions in d3 visualizations. The homework will revisit past visualizations to add interaction and transitions to them. Unless otherwise stated, all tasks should be done using D3.

### Part 1

Use your chart from **Assignment 3: Part 2 (air quality bar chart)** to add interaction and transitions.
  1. Create three radio buttons on the html page labeled 'Sort By State', 'Sort By Emissions Descending', 'Sort By Emissions Ascending'
      - Each radio button should when clicked result in the data being sorted either by state alphabetical order, emissions (high to low), or emissions (low to high) respectively.
      - After the data is sorted your chart should be updated correctly. This update should happen through the use of a transition that takes 1.5 seconds.
      - **NOTE**: nothing on the chart should be re-drawn during this update/transition
  2. Once you have completed this, add a text box to your html file with a label of Delay (in milliseconds).
      - The number in this box will be used so that it represents the number of millisecond delay that each element must wait before transitioning. This delay should be implemented so that all elements start and finish at different times according to their current order. Therefore, the first element should be delayed 1 x (number of millseconds in text box), the second element should be delayed 2 x (number of milliseconds in text box), and so on and so forth. The implementation should be fairly straight forward, if you sense you are hacking this together, take a step back and try to think through the solution based on everything you have used to date. 
      - **NOTE**: This textbox should only take a number (you must handle in your javascript if it is not a number and alert the user that they must enter a number). You can do this by using the javascript alert method.
  
### Part 2

Use your chart from **Assignment 5: Part 1 (weather station map)** to add interaction and transitions.
  1. Create a list of checkboxes where each checkbox represents a class of stations. All checkboxes should be checked to start. 
      - When a class checkbox is unchecked: the circles that represent those stations should be removed from the visualization (not hidden, but their elements removed). They should have a a transition when they are removed which is the circles being removed should have their radius shrink until the circles disappear.
      - When a checkbox that is unchecked is checked: the circles should re-appear on the map. Their entrance transition should be the opposite of the removal transition. The circles should appear in their correct spaces with a radius that goes from 0 to their appropriate size. 
  2. Create two textboxes that take numbers. The textboxes will represent the min and max elevation of the stations you want to keep on the map. Create a button that says filter stations. On click, the javascript should ensure that both inputs have a number in them (if not alert the user similiar to part 1). If there is no value in min or max assume that the user wants to keep down to the lowest value (if min is empty) or up to the highest value (if max is empty). When a circle falls outside the range it should be removed from the visualization. Its transition should appear as if the circle "falls off the bottom of page". When a circle that has been removed should re-appear it should "fall from the top of the page" and land in its appropriate spot given its lat/long. 

### What to submit

* `us-station-interaction.html`: Part 1
* `us-emissions-interaction.html`: Part 2
