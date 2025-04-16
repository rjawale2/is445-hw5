---
layout: default
title: Homework 5
---
## UFO Sightings Visualizations

### Plot 1: Frequency of UFO Sightings by Shape
<div id="vis1"></div>

### Plot 2: Interactive State and Shape Distribution
<div id="vis2"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script type="text/javascript">
  vegaEmbed('#vis1', 'plot1.json');
  vegaEmbed('#vis2', 'plot2.json');
</script>

## Write-Up

### Plot 1: Frequency of UFO Sightings by Shape  
This bar chart visualizes the frequency of UFO sightings categorized by their reported shape. The goal of this visualization is to highlight which shapes are most commonly reported across all sightings. 
For encoding, I used count() for the x-axis to represent the number of sightings and shape on the y-axis, sorted in descending order to emphasize the most frequent shapes at the top. 
I also used color encoding based on the shape field to make each bar distinct, which enhances readability and comparison across categories. The color scheme was automatically chosen by Altair and kept simple, 
with the legend removed to avoid redundancy since shape labels are already visible on the axis. 

### Plot 2: Interactive Sightings by State and Shape Distribution  
This interactive visualization consists of two linked bar charts. The left chart shows the total number of sightings per state, with each bar representing a state and the count of sightings along the x-axis. 
A selection_point interactivity is applied so that clicking on a specific state filters the right chart, which displays the distribution of UFO shapes for only that selected state. The encoding uses state on 
the y-axis and count() on the x-axis in the first chart. For visual clarity, I used a conditional color scheme: the selected state appears in steel blue while all others are light gray, guiding the viewer’s 
attention. In the second chart, shape is on the x-axis and count() on the y-axis, with color representing different shapes. The filtered transformation is applied using .transform_filter(state_click).

### Interactivity Discussion  
For the second plot, I added interactivity using Altair’s selection_point, which allows users to click on a state and dynamically update the adjacent chart with data specific to that state. 
This feature makes the visualization more engaging and informative, as it enables the viewer to drill down into the shape distribution for any state of interest, offering a more personalized
and focused analysis experience.

## Resources

[![The Data](https://img.shields.io/badge/-The%20Data-blue)](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)  
[![The Analysis](https://img.shields.io/badge/-The%20Analysis-orange)](https://github.com/rjawale2/is445-hw5/blob/main/Workbook.ipynb)
