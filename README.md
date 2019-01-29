# Eastron setuptool
Minimalistic setuptool for the Eastron sdm120 wattmeter.
Its primary usecase is the setup of the ID and the baudrate.

Note that this tool is more minimalistic than [gianfrdp/SDM120C](https://github.com/gianfrdp/SDM120C) 
and just supports changing the modbus setup values.

## PreRequirements
* python3, python3-minimalmodbus
  * e.g. pip3 install minimalmodbus

## Usage Example
Call the help page: `./setuptool.py --help`

Check connectivity of meter with ID==2, baudrate==2400 (default)\
`./setuptool.py --meterID=2`

**Note** that currently it's not able to *set* the meterID and baudrate 
to a new value at the same time, due to the nature of
the meter which changes the value immediately.\
To change both values one has to follow this example 

Set the Baudrate to 9600 of meter with ID==2\
`./setuptool.py --meterID=2 --setBaudrate=2`

Set meterID to 42 of meter with currentID==2\
`./setuptool.py --serialBaudRate=9600 --meterID=2 --setMeterID=42`
