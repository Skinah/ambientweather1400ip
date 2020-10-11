# Ambient Weather WS-1400IP Binding

This is a binding for the Ambient Weather WS-1400IP weather station and any other branded units that use an IPObserver module. It scrapes the livedata.htm webpage that the module offers and means cloud free and fully local weather updates.

## Supported Things

Ambient Weather WS-1400IP weather station locally via the IPObserver module (not thru Weather Underground clouds etc)


![Alt Ambient Weather IPObserver module](web/ipobserver.png?raw=true "Ambient Weather IPObserver module")

## Discovery

No automatic discovery, manual configuration

## Configuration

Leave all on defaults unless you have issues. It only needs the IP address for it to come online.

## Example Sitemap

In openHAB V3.x make sure you select SETTINGS>MODEL> 'create equipment from thing' after you login as an admin. Then the below should work with the auto generated items that the above creates.

*.sitemap

```

    Text label="WeatherStation" icon="rain"{
        Default item=WeatherStation_OutdoorTemperature icon=temperature
        Default item=WeatherStation_OutdoorHumidity icon=humidity
        Default item=WeatherStation_WindDirection icon=wind
        Default item=WeatherStation_WindSpeed icon=wind
        Default item=WeatherStation_SolarRadiation icon=sun
        Default item=WeatherStation_UVIndex icon=sun
        Default item=WeatherStation_HourlyRainRate icon=rain
        Default item=WeatherStation_DailyRain icon=rain
        Default item=WeatherStation_WeeklyRain icon=rain
        Default item=WeatherStation_MonthlyRain icon=rain
        Default item=WeatherStation_YearlyRain icon=rain
        Default item=WeatherStation_ReboottheIPObserverunit
    }


```
