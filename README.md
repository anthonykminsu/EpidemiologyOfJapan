# Lab 04: COVID-19 Case Rates Visualization Project

## Introduction
The COVID-19 Case Rates Visualization is an interactive web-based platform designed to display the spread and intensity of the COVID-19 pandemic across the United States during 2020. The project provides two main interactive maps (`map1.html` and `map2.html`), each offering a unique perspective on the data. The first map attempts to collectively represent the case rate for each county, where the differences in color of each county indicate the percentage for that specific county.

## Project Maps

### Map 1: COVID-19 Case Rates in the United States
This map (`map1.html`) visualizes the COVID-19 case rate per 1000 individuals among those aged 18 and older within U.S. counties. The map uses a choropleth representation to display the different percentages across each county. The color intensity indicates the severity of the outbreak in each county, brighter red indicating a substantial recording of COVID-19 cases.

**Link**: [COVID-19 Case Rates Map](https://anthonykminsu.github.io/EpidemiologyOfJapan/map1.html)

### Map 2: Total COVID-19 Case Counts in U.S. Counties
The second map (`map2.html`) displays total COVID-19 case counts within U.S. counties, represented by proportional circles that indicate the severity of cases. In terms of size, each circle correlates with the total number of cases, providing a clear visual representation of the pandemic's impact at the county level. When zoomed in, each county is represented by a circle to indicate the total count of cases within that specified county.

**Link**: [Total COVID-19 Case Counts Map](https://anthonykminsu.github.io/EpidemiologyOfJapan/map2.html)

## Primary Functions
The main functionality of this project includes:

- Interactive mapping using Mapbox GL JS.
- Data-driven visualization, dynamically rendering based on GeoJSON inputs.
- Proportional symbol mapping (in `map2.html`), where circle sizes represent case counts.
- Choropleth mapping (in `map1.html`), displaying data density through color gradients.
- Custom legend creation, dynamically scaled to data ranges.

## Libraries in Use
- **Mapbox GL JS**: For interactive mapping functionalities.
- **HTML/CSS**: For structuring and styling the web interface.

## Data Sources
Data for this project was sourced from:
- The New York Times
- The U.S. Census Bureau

These sources provided comprehensive data on COVID-19 cases at the county level across the United States.

## Credits and Acknowledgments
This project was developed by Anthony Kim. Special thanks to TA Liz Peng:
- [Bo Zhao]: For the well-curated lab assignment.
- [UW]: For providing necessary resources and support.

## How to Use
1. Open either of the HTML files in a web browser to view the interactive maps.
2. Hover over or click on specific map elements for detailed information.
3. Use the legend as a guide to understand the data representation.

## Code Highlights
The project’s codebase is characterized by its use of advanced mapping techniques and data handling. Key highlights include:

- Fetching and parsing GeoJSON data.
- Dynamic styling of map elements based on data attributes.
- Responsive design for accessibility across various devices.

## Future Enhancements
Future updates may include:
- Live data integration for real-time tracking.
- Additional interactivity features like search and filter tools.
