# pyluchtmeetnet

A python package to use the [Luchtmeetnet 2020 OpenAPI][luchtmeetnet-api].

## Installation

```shell
$ pip3 install pyluchtmeetnet
```

## Code example

```python
from pyluchtmeetnet.luchtmeetnet import Luchtmeetnet

latitude = 52.0808
longitude = 4.3063

lmn = Luchtmeetnet()

# Get nearest station
station = lmn.get_nearest_station(latitude, longitude)
print(station)

# Get latest LKI from station
lki = lmn.get_latest_station_lki(station["number"])
print(lki)

# Get latest measurements from station
measurements = lmn.get_latest_station_measurements(station["number"])
print(measurements)
```

[luchtmeetnet-api]: https://api-docs.luchtmeetnet.nl/
