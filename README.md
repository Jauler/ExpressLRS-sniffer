# ExpressLRS RX as sniffer

In some cases it may be useful to receive information about the flight on some other device (other than Radio or drone itself).
For example it may be useful for collecting telemetry and RC commands for logging purposes.

For example - by connecting it to a RaspberryPI or laptop.

## Disclaimer

As this is out-of-tree functionality, unlikely to be well maintained - use it at your own risk.
Do not blame me, if it bricks your receiver `¯\_(ツ)_/¯`.

## Flashing

Flashing can be done using ExpressLRS configurator:
1. Download source code from github.
2. Extract somewhere convenient
3. Select "Local" and select a folder where the code was extracted plus `/src`. For example if you extracted in `/home/user/ExpressLRS` select directory `/home/user/ExpressLRS/src`
4. Flash as normal

## Usage

In this case RX is fully silent.
Meaning, that TX will not know about existance of this RX and will **not** show connection to it.
RX-as-Sniffer however - will show (via LED statuses) that connection is established.
Whenever such connection is established - it will start dumping CRSF packets via UART. 

## Limitations

- Only CRSF protocol is supported
- LinkStatistics does not show RSSI which Radio is receiving UAV's - telemetry, but RSSI at which RX-as-sniffer receives UAV's telemetry.


