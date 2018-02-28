ogr2ogr -f GeoJSON -t_srs crs:84 neighborhoods.geojson Neighbourhoods.shp

---

<html>
<head>

</head>

<body>
  <div id="map"></div>
</body>
</html>

---

<link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.css" />
<script src="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.js"></script>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.2/jquery.min.js"></script>

<style type="text/css">
  #map {
    height: 100%;
  }
</style>

---

<script type="text/javascript">
// get the map element
var map = new L.Map('map');
</script>

---

// create a new open street map tile layer
var osm = new L.TileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
 minZoom: 8,
 maxZoom: 18,
 attribution: 'Map data © <a href="http://openstreetmap.org">OpenStreetMap</a> contributors'
});

// add it to the map
map.addLayer(osm);

// set the map view to lethbridge
var lethbridge = new L.LatLng(49.6942, -112.8328); // ˚N, ˚E (˚W is negative ˚E, similar for N and S)
map.setView(lethbridge, 12); // zoom in at level 12

// add geojson features to map
var neighborhoods = new L.geoJson();

$.ajax({
  dataType: "json",
  url: "neighborhoods.geojson",
  success: function (data) {
    data.features.forEach(function (feature) {
      neighborhoods.addData(feature);
    });
  }
}).error(function () {});

neighborhoods.addTo(map);
