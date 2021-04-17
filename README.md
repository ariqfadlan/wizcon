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
  -rgb {0-255} {0-255} {0-255}, --rgb {0-255} {0-255} {0-255}
                        Set RGB color of smart bulb
  -v, --version         show program's version number and exit

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
wizcon --brightness 255 192.168.1.100 ON

Set smart bulb color to blue:
wizcon -rgb 0 0 255 192.168.1.100 ON
```

## Tested bulbs

|   | Model            | Model ID     | Firmware    | 
|---| ---------------- | ------------ |------------ |
| 1 | A19 (RGB)        | 1.22.0       | 23007       |
| 2 | A21 (RGB)        | 1.24.0       | B23078      |
| 3 | AE27 (White)     | 1.17.1       | 23032       |

## Related
[Smart-Bulb-Control](https://github.com/rgomezjnr/Smart-Bulb-Control) - Rainmeter skin for controlling smart light bulbs

## Support
If you find an issue or have any feedback please submit an issue on [GitHub](https://github.com/rgomezjnr/wizcon/issues).

If you would like to show your support donations are greatly appeciated via:
- [GitHub Sponsors](https://github.com/sponsors/rgomezjnr)
- [PayPal](https://paypal.me/rgomezjnr)
- [Bitcoin:](bitcoin:bc1qh46qmztl77d9dl8f6ezswvqdqxcaurrqegca2p) bc1qh46qmztl77d9dl8f6ezswvqdqxcaurrqegca2p
- [Ethereum:](ethereum:0xAB443e578c9eA629088e26A9009e44Ed40f68678) 0xAB443e578c9eA629088e26A9009e44Ed40f68678

## Authors
[Robert Gomez, Jr.](https://github.com/rgomezjnr)

[Ariq Fadlan](https://github.com/ariqfadlan)

## Source code
https://github.com/ariqfadlan/wizcon

## License
[MIT](LICENSE.txt)
