# React Native Webview Leaflet
## A Leaflet map component with no native code for React Native apps.

[![npm](https://img.shields.io/npm/v/react-native-webview-leaflet.svg)](https://www.npmjs.com/package/react-native-webview-leaflet)
[![npm](https://img.shields.io/npm/dm/react-native-webview-leaflet.svg)](https://www.npmjs.com/package/react-native-webview-leaflet)
[![npm](https://img.shields.io/npm/dt/react-native-webview-leaflet.svg)](https://www.npmjs.com/package/react-native-webview-leaflet)
[![npm](https://img.shields.io/npm/l/react-native-webview-leaflet.svg)](https://github.com/react-native-component/react-native-webview-leaflet/blob/master/LICENSE)

## Usage

Add the following component to your code.
~~~~
<WebViewLeaflet 
        mapCenterCoords={coords} 
        onMapClicked={this.onMapClicked}
        onMarkerClicked={this.onMarkerClicked}
        onWebViewReady={this.onWebViewReady}
        locations={this.state.locations} />
~~~~

* mapCenterCoords: 5he center of the map in an array fo the form [latitude, longitude]
* onMapClicked: a function that will be called when the map is tapped.  It will receive the location of the tap in an array of the form [latitude, longitude]
* onMarkerClicked: a function that will be called when a marker is tapped.  It will receive the ID of the marker as shown in the location.id object below
* onWebViewReady: a function that is called when the map is ready for display.  It can be useful for displaying an activity indicator
* locations: see below


### Marker Locations
The locations property expects an array of objects with the following format:
~~~
{
        id: Math.floor(Math.random() * 1000),   // The ID attached to the marker. It will be returned when onMarkerClicked is called
        coords: [37.06452161, -75.67364786],    // Latitude and Longitude of the marker
        icon: emoji[Math.floor(Math.random() * emoji.length)],  // An emoji that will be displayed as the marker 

        // This object controls the animation that will be used
        // See below for a list of available animations
        animation: {
                name: animations[Math.floor(Math.random() * animations.length)],
                duration: Math.floor(Math.random() * 3) + 1,
                delay: Math.floor(Math.random()) * 0.5,
                interationCount
        }
}
~~~

### Available Animations
Animations for "bounce", "fade", "pulse", "jump", "waggle", "spin", and "beat" cane be specified in the animation.name property of an individual location. 



## LICENSE

MIT
