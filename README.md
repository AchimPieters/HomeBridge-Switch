# homebridge-http-simple-switch

Supports https devices on HomeBridge Platform

For more information visit: http://www.studiopieters.nl/apple-homebridge-Switch/

# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-switch
3. Update your configuration file. See sample-config.json in this repository for a sample. 

# Configuration



Configuration sample:

 ```
"accessories": [
        {
            "accessory": "HTTP-SWITCH",
            "name": "Living Room switch",
            "url": "http://192.168.1.210/switch",
            "default_state_off": true, 
            "sendimmediately": "",
            "http_method": "GET"
        }
    ]

```# homebridge-switch

# Request

This plugin will call the specified URL for both On and Off state. It expects the server, that receives the request, to toggle the state for each subsequent call.

# Response

The plugin expects to receive a JSON body for all responses <= 400 HTTP Status code. It discards the body of the responses for HTTP status codes > 400 and will treat it as an error.
