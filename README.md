Historical traffic data in the City of Manila for May 31 to June 6, 2023 was collected from tomtom.com and transcribed into a dataset.

This data consists of 7 days worth of hourly traffic data (168 rows) consisting of 3 features:

1.   Live Speed (kilometers/hour) - Formula is km-driven over travel time. The travel time and km-driven are calculated for each directed road segment (DSEG) within the city circle (s.a.) on an hourly basis.
2.   Usual Time per 10km (seconds) - Typical travel time per 10km based on TomTom historic data (from 2022). Converted from minutes and seconds format.
3.   Live Time per 10km (seconds) - Real-time measurement of traffic in the city. Shows the average time it would currently take to travel 10 km. Converted from minutes and seconds format.

(Descriptions summarized from https://www.tomtom.com/traffic-index/about/)

From our project proposal, we have changed the weather data source to https://meteostat.net/en/station/98425 as the data is recorded in hourly intervals and there is more information available. It is more reliable than the previous source because it also indentifies from which station the weather data was recorded.

The weather data for the City of Manila during the same time period was also collected and transcribed from meteostat.net. 

This data consists of 7 days worth of weather data (168 rows) consisting of 7 features:

1.   Temperature (temp) (degrees Celsius) - Air temperature taken in the area.
2.   Dew Point (dwpt) (degrees Celsius) - The dew point is the temperature the air needs to be cooled to (at constant pressure) in order to achieve a relative humidity of 100%. 
3.   Relative Humidity (rhum) (percent) - the amount of water vapor in the air, expressed as a percentage of the maximum amount of water vapor the air can hold at the same temperature.
4.   Total Precipitation (prcp) (millimeters) - The amount of water (rain, snow, etc.) that falls to the surface.
5.   Snow Depth (snow) - Irrelevant to this study, as it does not snow in Manila.
6.   Wind Direction (wdir) (degrees) - The true direction from which the wind is blowing at a given location (i.e., wind blowing from the north to the south is a north wind). It is normally measured in tens of degrees from 10 degrees clockwise through 360 degrees. North is 360 degrees. A wind direction of 0 degrees is only used when wind is calm.
7.   Average Wind Speed (wspd) (kilometers/hour) - The rate at which air is moving horizontally past a given point.
8.   Wind Peak Gust (wpgt) (kilometers/hour) - The highest instantaneous wind speed observed or recorded.
9.   Sea-Level Air Pressure (pres) (hectopascal) - Air pressure reading, converted to a value that would be observed if that instrument were located at sea level.
10.   Total Sunshine Duration (tsun) (minutes) - How much sunshine is recorded during the period.
11.   Weather Condition Code (coco) - Numerical code from 1-27 representing the type of weather recorded.

(Source for feature names and units: https://dev.meteostat.net/formats.html#meteorological-parameters) 

(Descriptions from: https://dev.meteostat.net/formats.html#meteorological-parameters, https://www.weather.gov/arx/why_dewpoint_vs_humidity, https://education.nationalgeographic.org/resource/humidity/, https://education.nationalgeographic.org/resource/precipitation/, https://forecast.weather.gov/glossary, https://www.noaa.gov/jetstream/atmosphere/air-pressure)

There are also 2 unnamed features that are shared between the datasets:

1.   Time - the 24 hour hh:mm format of the hour the measurements were taken
2.   Date - the mm/dd/yyyy format of what day the data was taken

For this project, we are concerned with these features: Live Speed (which we are trying to predict), Temperature, Dew Point, Relative Humidity, Total Precipitation, Average Wind Speed, Sea-Level Air Pressure, and Time.
