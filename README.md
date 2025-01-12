# homebridge-hyperion
[Homebridge](https://github.com/nfarina/homebridge) accessory plugin for Hyperion

This plugin allows you to remotely control the state of your Hyperion controlled lights.  It allows you to set the on/off state and change the brightness/color.

It optionally allows you to turn on the 'Ambilight' feature on/off. To do so, a switch device will be created. To enable this, set the 'ambilight_name' parameter in the configuration file.

# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-tiedyegeek-hyperion-ng
3. Update your configuration file. See below for a sample.

# Configuration

Configuration sample:

 ```
"accessories": [
    {
        "accessory": "Hyperion",
        "name": "TV Backlight",
        "ambilight_name": "Ambilight",
        "ambilight_brightness": 50,
        "priority": "100",
        "host": "localhost",
        "port": "19444"
    }
]
```

Fields:

* "accessory": Must always be "Hyperion" (required)
* "name": Can be anything (required)
* "ambilight_name": Can be anything (optional, creates a switch to turn ambilight on/off.)
* "ambilight_brightness": brighness to be set at when on ambilight (optional)
* "priority": Hyperion priority channel (lower value means higher priority)
* "host": The hostname or ip of the machine running Hyperion (required)
* "port": The port that Hyperion is using (usually 19444) (required)
