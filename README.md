# datamaps-custom-marker
A datamaps plugin for custom map markers.

![datamaps-custom-markers](https://cloud.githubusercontent.com/assets/124599/10392845/ea6d5048-6e9b-11e5-9d2d-c92b3ddb8c5a.png)

## Installation

Include this file:

```
<script src="/datamaps.markers.js"></script>
```

## Usage

```
// Build map.
var map = new Datamap({
    element: document.getElementById('map'),
    scope: 'world',
    geographyConfig: {
      highlightOnHover: true,
      popupOnHover: false
    }
});

// Add the custom markers plugin.
map.addPlugin('markers', Datamap.customMarkers);

// Add markers with the `icon` config. Specify the `url, width and height` properties.
var options = {
  fillOpacity: 1,
  popupOnHover: true,
  icon: {
    url: '/path/to/icon.png',
    width: 20,
    height: 20
  }
};
map.markers([
  {name: 'foo', radius: 10, latitude: 50.17, longitude: 78.41},
  {name: 'bar', radius: 10, latitude: 60.23, longitude: 63.13},
  {name: 'baz', radius: 10, latitude: 70.11, longitude: 82.76}
], options);
```

Based on [@markmarkoh](https://github.com/markmarkoh)'s work [here](http://jsbin.com/pamigahifi/1/edit?html,output).
