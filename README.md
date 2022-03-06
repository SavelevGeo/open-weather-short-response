# OpenWeatherShortResponse
A short response from OpenWeatherMap forecast.

A simple app to put a 5 days weather forecast into 160 characters.<br />
It gets a request from [OpenWeatherMap.org One Call API](https://openweathermap.org/api/one-call-api), rearranges the daily forecast for 5 days into a short version.

An answer example:
```
14                  
13-18-17-12,804,0   
13-15-16-11,500,53
11-18-18-15,803,0
13-20-19-16,801,0
14-24-24-20,803,0
17-25-26-21,801,0
20-26-25-23,804,13
21-30-28-24,803,0
```
Being: `14` the first day of the forecast.<br />
Then for each day, separated by space:<br />
`13-18-17-12` Morning-Day-Evening-Night temperature in C&deg;`,`[weather id](https://openweathermap.org/weather-conditions#Weather-Condition-Codes-2)`,`probability of precipitation in %

# Getting started

requires a `python3` and `pandas`

    git clone https://github.com/SavelevGeo/open-weather-short-response && cd open-weather-short-response
or download the `weather_ui.py` and `weather_request.py` files

and if `python` stands for Python 3.0 or higher:
    python 
