Leaflet.locationfilter by Tripbirds.com
=======================================

Provides a location filter for Leaflet. In short, the location filter is 
a draggable/resizable rectangle. It is integrated with your application
through a set of callbacks that are called when the user interacts with
the filter. 

### Usage
Create a new LocationFilter and add it to the map:

```javascript
var locationFilter = new L.LocationFilter({
  onChange: function(bounds) {
    // do something with the the filter bounds
  },

  onEnabled: function(bounds) {
    // do something with the the filter bounds
  },

  onDisabled: function(bounds) {
    // do something with the the filter bounds
  }
}).addTo(map);
```

Get the current bounds:

```javascript
var bounds = locationFilter.getBounds();
```

Check if the location filter is enabled:

```javascript
var isEnabled = locationFilter.isEnabled();
```

### Options
**bounds** (optional): The initial bounds for the location filter. Defaults to the maps own bounds.
**enable** (optional): Set to true to enable the filter as soon as it is added to the map. Defaults to false.
**onChange** (optional): Called every time the location filter changes size or position.
**onEnabled**: (optional): Called when the location filter gets enabled.
**onDisabled** (optional): Called when the location filter gets disabled.
**onEnableClick** (optional): Called when the user clicks the enable button.
**onDisableClick** (optional): Called when the user clicks the disable button.
**onAdjustToZoomClick** (optional): Called when the user clicks the adjust button.

### License
Leaflet.locationfilter is free software, and may be redistributed under the MIT-LICENSE.