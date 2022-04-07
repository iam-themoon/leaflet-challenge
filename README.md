# leaflet-challenge
Repository for HW 15 - Visualizing Data with Leaflet!

For this assignment, we create a map with a variety of layers.

## Tile layers / map backgrounds
* For each tile layer we create a variable with the layer name and link it to the map link
    * These sections are copied and pasted from "leaflet-extras.github.io" maps 

## basemaps object
* This basemaps object is another variable that holds our map layers as their names which will appear on the map itself
* Note: whichever layer is last on this list will automatically load, which is why we have put the "default" last

## map object
* This is the overall map object (L.map()) which we use to set the center coordinates, zoom, and most importantly, add our tile layers
* Then we add the default map to the map object

## tectonic plate data 
* To add the tectonic plate outlines, we create another variable/layer group (L.layerGroup())
* Then we use d3.json to grab the api for pulling the plate data
* Then load the data using L.geoJson and add styling to make the lines visible
* Then we add that data to the map object

## earthquake data
* We create a variable to hold the earthquake data layer
* Then we use d3.json to grab the data from the USGS geoJson api
* Within that call, we create a function to return specific colors based on the "depth" value of the earthquake
* Then we create another function to set the radius size for each data point 
* Then we create another function to style each data point 
* Then we add the data to the earthquake layer group (L.geoJson) and apply all of the color, radius, and stying functions to it
* Then we add the earthquake layer to the map object

## overlays
* We create a variable for overlays to add the plate and quake data as overlays

## layer control & legend control
* We create a control object to add the basemap and overlay toggle to the map
* We also create a legend L.control()

## legend properties
* With the legend control, we add its functionalities
* We add it to the map with L.DomUtil.create()
* We set its intervals and respective colors
* We loop through each interval and create a label with the colors
* Then we add it to the map object

And we're done! Thanks! :)