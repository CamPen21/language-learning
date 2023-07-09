# Observer Pattern Exercise

## Problem Description

You are developing a weather station application that collects and distributes weather data. This application needs to notify various components (e.g., Current Conditions Display, Statistics Display, and Forecast Display) whenever it receives new weather data. Different display elements show different kinds of information and need to be updated independently.

Your task is to implement the Observer pattern to allow for an efficient and organized distribution of weather data to the different displays.

## Instructions

1. Define an abstract class `Subject` with methods to `register_observer`, `remove_observer`, and `notify_observers`.

2. Define an abstract class `Observer` with a method `update` that takes the temperature, humidity, and pressure as arguments.

3. Implement a `WeatherData` class that extends `Subject`. It should have methods to `get_temperature`, `get_humidity`, `get_pressure`, and `measurements_changed`, which is called whenever new weather measurements are available.

4. Implement `CurrentConditionsDisplay`, `StatisticsDisplay`, and `ForecastDisplay` classes that extend `Observer` and implement the `update` method to display the relevant information.

5. In your main program, create an instance of `WeatherData` and multiple display instances. Register these displays with the weather data instance.

6. Demonstrate the weather station working by randomly changing the weather data a few times and showing the display components updating accordingly.

## Tips

- You may use `random` module to simulate the changes in weather conditions.
- Ensure that the display components can be added and removed dynamically.

## Expected Output

You should be able to update weather data and see each of your displays react and show the updated data.

```python
weather_data = WeatherData()

current_display = CurrentConditionsDisplay()
weather_data.register_observer(current_display)

stats_display = StatisticsDisplay()
weather_data.register_observer(stats_display)

forecast_display = ForecastDisplay()
weather_data.register_observer(forecast_display)

# Simulate new weather measurements
weather_data.set_measurements(80, 65, 30.4)
weather_data.set_measurements(82, 70, 29.2)
weather_data.set_measurements(78, 90, 29.2)

# Output will depend on your implementation of the update method in each display class
```
