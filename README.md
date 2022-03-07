# OpenWeatherShortResponse
A short response from OpenWeatherMap forecast.

A simple app to put a 5 days weather forecast into 160 characters.<br />The response can be sent via SMS, for example, if recipient doesn't have access to the Internet.<br />
It gets a request from [OpenWeatherMap.org One Call API](https://openweathermap.org/api/one-call-api), rearranges the daily forecast for 5 days into a short version.

A response example:
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
requires a `python3`, `pandas` and `requests`

    git clone https://github.com/SavelevGeo/open-weather-short-response && cd open-weather-short-response
or download the `weather_ui.py` and `weather_request.py` files

and if `python` stands for `Python 3.0` or higher with `pandas` and `requests`:

    python weather_ui.py

The main and only window appears:

![ui](https://user-images.githubusercontent.com/57714410/156938215-1b51b1e7-48a7-4d41-a4ac-1a9c171d3f2e.png)

# Get your point and take your weather
As an example, go to your favourite map service and copy the coordinate in decimal `lat, lon` format separated by `,`:

![google maps](https://user-images.githubusercontent.com/57714410/156938376-5b3c1ed9-6bf5-4d78-8d71-2a363ac2271a.png)

Then press `paste from clipboard`, then `request`

and `copy to clipboard` the response you got

![the request](https://user-images.githubusercontent.com/57714410/156938914-cde42b8b-69d9-4792-8494-a5a03cf07281.png)

The response format is explained [at the top](#openweathershortresponse)

# Send it!

the maximum size of the forecast text is 160 symbols. It is the maximum size for the satellite phone online SMS as for [Iridium](https://messaging.iridium.com)

![send sms](https://user-images.githubusercontent.com/57714410/156939049-11c0aee0-698d-4177-9bd4-4534fc69e37f.png)

# NB!

The limit for one api key is 60 calls/minute or 1,000,000 calls/month.
If you are planning to use it more often than once, you need to [get your own API key](https://openweathermap.org/price) and replace my API key with it [here](https://github.com/SavelevGeo/open-weather-short-response/blob/22a4ad19a49cdd9beaceec7d01ed38170efc7276/weather_request.py#L8) in `weather_request.py`. With the same limit the API key is free.
