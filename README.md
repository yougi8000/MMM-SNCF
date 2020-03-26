# MMM-SNCF

MMM-SNCF was developped from the ![MMM-Transilien](https://github.com/lgmorand/MMM-Transilien) module.

## Installation

Clone the git in the /modules folder of Magic Mirror and run the "npm install" command which will installed the required node modules

## Example

![Module SNCF](https://github.com/abrochet/MMM-SNCF/blob/master/screenshots/transilien.png)

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:

```javascript
{
    module: 'MMM-SNCF',
    position: 'top_right',
    header: 'Lille-Flandres to Orchies',
    config:{
        departUIC: "stop_area:OCE:SA:87286005",
        arriveeUIC: "stop_area:OCE:SA:87286583",
        trainsdisplayed: '5',
        apiKey: "", // You must add your API key
    }
},
```

## Configuration options

The following properties can be configured:

| Option           | Description
| ---------------- | -----------
| `updateInterval` | How often does the trains have to change? (Milliseconds) <br><br> **Possible values:** `1000` - `86400000` <br> **Default value:** `60000` (60 seconds)
| `animationSpeed` | Speed of the update animation. (Milliseconds) <br><br> **Possible values:**`0` - `5000` <br> **Default value:** `2000` (2 seconds)
| `debugging` | Show logs in console. <br><br> **Possible values:** `true` or `false` <br> **Default value:** `false`
| `retryDelay` | The delay before retrying after a request failure. (Milliseconds) <br><br>Possible values: 1000 - 60000 <br><br>Default value: 10000
| `initialLoadDelay` | The initial delay before loading. If you have multiple modules that use the same API key, you might want to delay one of the requests. (Milliseconds) <br><br> **Possible values:** `1000` - `5000` <br> **Default value:** `0`
| `apiKey` | The [SNCF](https://www.digital.sncf.com/startup/api) API key, which can be obtained by creating an SNCF account. <br><br> This value is **REQUIRED**
| `departUIC` | You need to find your train station and find the [**UIC**](https://ressources.data.sncf.com/explore/dataset/referentiel-gares-voyageurs) of the train station (*not the uic7 column, the UIC*).<br><br> This value is **REQUIRED**
| `arriveeUIC` | You need to find your train station and find the [**UIC**](https://ressources.data.sncf.com/explore/dataset/referentiel-gares-voyageurs) of the train station (*not the uic7 column, the UIC*).<br><br> This value is **REQUIRED**
| `trainsDisplayed` | Number of results to display.<br><br> **Default value:** `3` 

## Further information and support

Please use the forum of magic mirror² [https://forum.magicmirror.builders/](https://forum.magicmirror.builders/)
