# Lab 04: COVID-19 Case Rates Visualization Application

## Introduction
The COVID-19 Case Rates Visualization is an interactive web-based platform designed to display the spread and intensity of the COVID-19 pandemic across the United States during 2020. The project provides two main interactive maps (`map1.html` and `map2.html`), each offering a unique perspective on the data. The first map attempts to collectively represent the case rate for each county, where the differences in color of each county indicate the percentage for that specific county. The seconf map on the otherhand attempts to visualize the total cases in each county through a series of elipses that are configured to the count of cases. Each map acquires a feature where you can hover over each county to see the actual count, this includes case rate and total number of cases.

## Primary Functions
The main functionality of this application includes:

- Interactive mapping using Mapbox GL JS.
- Data-driven visualizations with dynamic rendering based on GeoJSON inputs.
- Proportional symbol mapping (in `map2.html`), where circle sizes represent case counts.
- Choropleth mapping (in `map1.html`), displaying data density through color gradients.
- Custom legend creation, dynamically scaled to data ranges.
- Hover over the map to get matched statistics of the given county.

## Project Maps

### Map 1: COVID-19 Case Rates in the United States
This map (`map1.html`) visualizes the COVID-19 case rate per 1000 individuals among those aged 18 and older within U.S. counties. The map uses a choropleth representation to display the different percentages across each county. The color intensity indicates the severity of the outbreak in each county, brighter red indicating a substantial recording of COVID-19 cases.

<img width="1440" alt="Screen Shot 2024-02-04 at 6 44 51 PM" src="https://github.com/anthonykminsu/EpidemiologyOfJapan/assets/77130958/03875817-01b3-450e-ae6b-1efe22d1c809">

**Link**: [COVID-19 Case Rates Map](https://anthonykminsu.github.io/EpidemiologyOfJapan/map1.html)

### Map 2: Total COVID-19 Case Counts in U.S. Counties
The second map (`map2.html`) displays total COVID-19 case counts within U.S. counties, represented by proportional circles that indicate the severity of cases. In terms of size, each circle correlates with the total number of cases, providing a clear visual representation of the pandemic's impact at the county level. When zoomed in, each county is represented by a circle to indicate the total count of cases within that specified county.

<img width="1440" alt="Screen Shot 2024-02-04 at 6 45 00 PM" src="https://github.com/anthonykminsu/EpidemiologyOfJapan/assets/77130958/484931e7-1b4d-462a-a194-82a44353aac7">

**Link**: [Total COVID-19 Case Counts Map](https://anthonykminsu.github.io/EpidemiologyOfJapan/map2.html)

## Libraries in Use
- **Mapbox GL JS**: For interactive mapping functionalities.
- **HTML, CSS, & Javascript**: For structuring and styling the web interface.

## How to Use
1. Open either of the HTML files in a web browser to view the interactive maps.
2. Hover over or click on specific map elements for detailed information.
3. Use the legend as a guide to understand the data representation.

## Detailed Functionality Overview of Code

### Map Initialization
- `mapboxgl.Map`: This function allows the initialization of the map, setting its container and styles. This is the foundational step for creating the map and is critical for both `map1.html` and `map2.html`.

### Data Loading and Processing
- `fetch`: Used to asynchronously retrieve the GeoJSON data from a specified path. This function was essential when loading the COVID-19 case data into the map.
- `.then()`: Used to handle the response from the `fetch` function. The function ensures that the map is rendered only after the data has been successfully loaded.
- `JSON.parse`: This function converts the fetched JSON data into JavaScript objects for further processing.

### Map Source and Layer Configuration
- `map.addSource`: This function adds a data source to the map. Within these maps. the function is used to define the GeoJSON data source for COVID-19 case rates and counts.
- `map.addLayer`: This function is used to add a layer to the map using the defined data source. It specifies the type of layer (like 'fill' for choropleth maps or 'circle' for proportional symbols) and styling properties.

### Dynamic Styling
- `['step']`, `['get']`, `['interpolate']`: These expressions were used within the `map.addLayer` function to dynamically style the map layers based on the data. For instance, they helped in setting the radius of circles proportional to case counts or the color intensity for different case rates.

### Interactive Legend Creation
- `document.getElementById`: This function was used to select the HTML element where the legend will be appended.
- `document.createElement`: This was used to create new HTML elements dynamically.
- `appendChild`: This method was used to add newly created elements (legend items) to the legend container.

### Error Handling
- `.catch()`: This Promise method is used to catch and log any errors that occur during the data fetching process, ensuring that any issues are appropriately handled and logged.

Each of these functions played a vital role in creating interactive and data-driven maps for visualizing COVID-19 case rates and counts. They collectively contribute to the project’s functionality of fetching, processing, and visually representing complex geographic and statistical data.

## Data Sources
Data for this project was sourced from:
- [The New York Times](https://github.com/nytimes/covid-19-data/blob/43d32dde2f87bd4dafbb7d23f5d9e878124018b8/live/us-counties.csv)
- [The U.S. Census Bureau](https://data.census.gov/table/ACSDP5Y2018.DP05?g=0100000US$050000&d=ACS%205-Year%20Estimates%20Data%20Profiles&hidePreview=true)

These sources provided comprehensive data on COVID-19 cases at the county level across the United States.

## Future Enhancements
Future updates may include:
- Live data integration for real-time tracking.
- Additional interactivity features like search and filter tools.

## Credits and Acknowledgments
This project was developed by Anthony Kim. Special thanks to TA Liz Peng and: 
- Bo Zhao: For the well-curated lab assignment.
- UW: For providing necessary resources and support.
