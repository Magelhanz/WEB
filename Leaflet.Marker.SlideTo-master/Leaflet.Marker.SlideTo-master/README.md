# Leaflet.Marker.SlideTo

A plugin for [LeafletJS](http://www.leafletjs.com) to smoothly move (slide) markers to a new location.

Tested with Leaflet 1.0.0-rc3. Do not expect this to work in Leaflet 0.7.x.

See the [demo](http://ivansanchez.gitlab.io/Leaflet.Marker.SlideTo/demo.html).

### API

This plugin adds two new methods to all `L.Marker`s, `L.Circle`s and `L.CircleMarker`s:
* `.slideTo(latlng, slideOptions)`.
* `.slideCancel()`

The `slideTo` method will start moving the marker (or circle) towards `latlng`, taking
some time to do so, using a linear animation.

Two options are available:
* `duration` is the number of milliseconds the slide animation will last.
* `keepAtCenter` is a boolean, whether the map center will follow the marker for the duration of the animation. If set to true, the map's dragging handler will be disabled momentarily.

```
var marker = L.marker([10,10]);

marker.slideTo(	[20, 20], {
	duration: 2000,
	keepAtCenter: true
});

```

The `slideCancel` method will stop the sliding animation (if applicable). Running
`setLatLng` or dragging the marker will also stop the animation.

### Installation through `npm`

```
npm install leaflet.marker.slideto
```

(Idem for `yarn add`)

### Usage through unpkg

```
<script src='https://unpkg.com/leaflet.marker.slideto@0.2.0/Leaflet.Marker.SlideTo.js'></script>
```

### Legalese


"THE BEER-WARE LICENSE":
<ivan@sanchezortega.es> wrote this file. As long as you retain this notice you
can do whatever you want with this stuff. If we meet some day, and you think
this stuff is worth it, you can buy me a beer in return.


