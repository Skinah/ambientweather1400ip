# Ambient Weather WS-1400IP Binding

This is the binding for the Ambient Weather WS-1400IP weather station, via local updates.

## Supported Things

Ambient Weather WS-1400IP weather station locally via the IPObserver module (not thru Weather Underground clouds etc)


![Alt Ambient Weather IPObserver module](web/ipobserver.png?raw=true "Ambient Weather IPObserver module")

## Discovery

No automatic discovery, manual configuration

## Binding Configuration

*.things


```

Thing ambientweather1400ip:weatherstation:Weather1 [hostname="192.168.1.243", autoReboot=5000, scanrate=20]

```



*.items

```

Number WeatherOutdoorTemp "Outdoor Temp" {channel="ambientweather1400ip:weatherstation:Weather1:outdoor_temp"}
Number WeatherOutdoorHumidity "Outdoor Humidity %" {channel="ambientweather1400ip:weatherstation:Weather1:outdoor_humidity"}
Number WeatherWindDir "Wind Direction" {channel="ambientweather1400ip:weatherstation:Weather1:wind_direction"}
Number WeatherWindSpeed "Wind Speed" {channel="ambientweather1400ip:weatherstation:Weather1:wind_speed"}
Number WeatherWindGust "Wind Gust" {channel="ambientweather1400ip:weatherstation:Weather1:wind_gust"}
Number WeatherSolarRad "Solar Radiation" {channel="ambientweather1400ip:weatherstation:Weather1:solar_radiation"}
Number WeatherUV "UV" {channel="ambientweather1400ip:weatherstation:Weather1:uv"}
Number WeatherUVIndex "UV Index" {channel="ambientweather1400ip:weatherstation:Weather1:uvi"}
Number WeatherRainHourly "Rain Hourly mm" {channel="ambientweather1400ip:weatherstation:Weather1:hourly_rain"}
Number WeatherRainDaily "Rain Last 24 hours mm" {channel="ambientweather1400ip:weatherstation:Weather1:daily_rain"}
Number WeatherRainWeekly "Rain this week mm" {channel="ambientweather1400ip:weatherstation:Weather1:weekly_rain"}
Number WeatherRainMonthly "Rain this month mm" {channel="ambientweather1400ip:weatherstation:Weather1:monthly_rain"}
Number WeatherRainYearly "Rain this year mm" {channel="ambientweather1400ip:weatherstation:Weather1:yearly_rain"}
String WeatherBatteryOut "Battery Status" {channel="ambientweather1400ip:weatherstation:Weather1:battery_out"}
Number WeatherResponse "Response (ms)" {channel="ambientweather1400ip:weatherstation:Weather1:web_response"}
Switch WeatherReboot "Reboot Station" {channel="ambientweather1400ip:weatherstation:Weather1:reboot"}


```


*.sitemap

```

    Text label="WeatherStation" icon="rain"{
        Default item=WeatherOutdoorTemp
        Default item=WeatherOutdoorHumidity
        Default item=WeatherWindDir
        Default item=WeatherWindSpeed
        Default item=WeatherWindGust
        Default item=WeatherSolarRad
        Default item=WeatherUV
        Default item=WeatherUVIndex
        Default item=WeatherRainHourly
        Default item=WeatherRainDaily
        Default item=WeatherRainWeekly
        Default item=WeatherRainMonthly
        Default item=WeatherRainYearly
        Default item=WeatherBatteryOut
        Default item=WeatherResponse
        Default item=WeatherReboot
    }


```


## Channels

Channels are based on what is available on the local ObserverIP web page
![Alt Ambient Weather WS-1400IP channels](web/channels.png?raw=true "Ambient Weather WS-1400IP channels")
