# Iterator Pattern Exercise

## Problem Description

You're developing a software for a digital radio. This radio stores stations in different frequencies (FM, AM, LW). Users can tune into a specific frequency and then iterate through the stations in that frequency.

Your task is to implement the Iterator Pattern to allow users to traverse through the different radio stations within a specific frequency.

## Instructions

1. Define a `Station` class which represents a radio station. The station has a property `frequency` which represents its frequency.

2. Define an interface (or an abstract class) `StationIterator` with methods `has_next` and `next`.

3. Define an interface (or an abstract class) `StationList` with a method `create_iterator`.

4. Implement concrete `FMStationList`, `AMStationList`, and `LWStationList` classes that implement the `StationList` interface. Each of these classes should store a list of stations and return an iterator for this list.

5. Implement a `FrequencyStationIterator` class that implements the `StationIterator` interface. It should be initialized with a list of stations and allow iteration over this list.

6. In your main program, create instances of `FMStationList`, `AMStationList`, and `LWStationList`, add some stations to each list, create an iterator for each list, and print all stations in each frequency.

## Tips

- Make sure the `next` method in your iterator returns the next station and advances to the following station, and `has_next` checks if there are more stations to iterate over.

## Expected Output

You should be able to iterate over the stations in each frequency. For example:

```python
fm_stations = FMStationList()
fm_stations.add_station(Station(89.1))
fm_stations.add_station(Station(90.9))
fm_stations.add_station(Station(101.2))

iterator = fm_stations.create_iterator()

while iterator.has_next():
    print(iterator.next().get_frequency())
```
