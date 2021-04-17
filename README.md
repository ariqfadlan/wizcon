# wizcon
Control Philips WiZ Connected Turnable White smart light bulbs

**This fork supports Turnable White variant only**

## Requirements
- [Python 3.7 or higher](https://www.python.org/downloads/)
- [pywizlight](https://github.com/sbidy/pywizlight)

## Installation
    `pip install git+https://github.com/ariqfadlan/wizcon.git`

## Usage
```
usage: wizcon.py [-h] [-si 6 | {9,16} | 18 | {29-32}] [-b {0-255}] IP {ON,OFF,SWITCH}

Control Philips WiZ Connected Turnable White smart bulb

positional arguments:
  IP                    IP address of smart bulb
  {ON,OFF,SWITCH}       Command sent to the smart bulb

optional arguments:
  -h, --help            show this help message and exit
  -si 6 | {9,16} | 18 | {29-32}, --scene_id 6 | {9,16} | 18 | {29-32}
                        Set scene of smart bulb using scene ID
  -b {0-255}, --brightness {0-255}
                        Set brightness of smart bulb

Scene Table
6: "Cozy"
9: "Wake up"
10: "Bedtime"
11: "Warm White"
12: "Daylight"
13: "Cool white"
14: "Night light"
15: "Focus"
16: "Relax"
18: "TV time"
29: "Candlelight"
30: "Golden white"
31: "Pulse"
32: "Steampunk"

Examples

Turn smart bulb on:
python3 wizcon.py 192.168.1.100 ON

Turn smart bulb off:
python3 wizcon.py 192.168.1.100 OFF

Switch smart bulb between on and off states:
python3 wizcon.py 192.168.1.100 SWITCH

Set scene to "Focus" using scene ID:
python3 wizcon.py 192.168.1.100 ON --scene_id 16

Set brightness to 255 (max brightness):
python3 wizcon.py 192.168.1.100 ON --brightness 255
```

## Source code
https://github.com/ariqfadlan/wizcon

## Author
[Robert Gomez, Jr.](https://github.com/rgomezjnr)

## License
[MIT](LICENSE.txt)
