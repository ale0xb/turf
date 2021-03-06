# @turf/transform-translate

# translate

Moves any geojson Feature or Geometry of a specified distance along a Rhumb Line
on the provided direction angle.

**Parameters**

-   `geojson` **[GeoJSON](http://geojson.org/geojson-spec.html#geojson-objects)** object to be translated
-   `distance` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** length of the motion; negative values determine motion in opposite direction
-   `direction` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** of the motion; angle from North in decimal degrees, positive clockwise
-   `units` **\[[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)]** in which `distance` will be express; miles, kilometers, degrees, or radians (optional, default `kilometers`)
-   `zTranslation` **\[[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)]** length of the vertical motion, same unit of distance (optional, default `0`)
-   `mutate` **\[[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** allows GeoJSON input to be mutated (significant performance increase if true) (optional, default `false`)

**Examples**

```javascript
var poly = turf.polygon([[[0,29],[3.5,29],[2.5,32],[0,29]]]);
var translatedPoly = turf.translate(poly, 100, 35);

//addToMap
translatedPoly.properties = {stroke: '#F00', 'stroke-width': 4};
var addToMap = [poly, translatedPoly];
```

Returns **[GeoJSON](http://geojson.org/geojson-spec.html#geojson-objects)** the translated GeoJSON object

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/transform-translate
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
