### Add feature layers with Esri Leaflet

In this lab, you will add featurelayers to an Esri Leaflet application.

1. Open the [starter map](../create_starter_map/index.html) HTML and copy the contents to a new [jsbin.com](http://jsbin.com).

2. In `JSBin` > `HTML`, add the following plugin to draw the layer styles:

	```js
	<!-- Load Esri Leaflet Renderers -->
	<script src="https://unpkg.com/esri-leaflet-renderers@2.0.2"></script>

	```

3. Add the following layers to the map:

	```js
	<script type='text/javascript'>
		var map = L.map('map').setView([45.533, -122.657], 12);
		L.esri.basemapLayer('DarkGray').addTo(map);

		 // ADD the rail lines here
		L.esri.featureLayer({
			url: 'https://services.arcgis.com/uCXeTVveQzP4IIcx/arcgis/rest/services/PDX_Rail_Lines_Styled/FeatureServer/0'
		}).addTo(map);

	</script>
	```
4. Run and test the app.

Your app should look something like this:

 * [Code](index.html)
 * [Live App](http://esri.github.io/geodev-hackerlabs/develop/leaflet/add_feature_layer/index.html)

### Bonus
* Add a [Rail Stops feature layer](http://services.arcgis.com/uCXeTVveQzP4IIcx/arcgis/rest/services/PDX_Rail_Stops_Styled/FeatureServer/0) to the map,
 and then add a [Neighborhoods feature layer](http://services.arcgis.com/uCXeTVveQzP4IIcx/arcgis/rest/services/PDX_Neighborhoods_Styled/FeatureServer/0).
* Use Leaflet's new [`Map Panes`](http://leafletjs.com/reference.html#map-panes) to get control over display order
