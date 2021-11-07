# Landuse Data Berlin

## About the data source

The geojson files in this data source present areas of different land use in Berlin.

## Usage

Use [Overpass Turbo](https://overpass-turbo.eu/) to get all areas in a certain bounding box that have a given landuse using the syntax is as in the example below.
* replace `cemetery` in this example by any other [valid value for landuse](https://wiki.openstreetmap.org/wiki/Key:landuse)
* the coordinates specify the bounding box, in the example the city of Berlin.

Then, export data as geojson file.

```
[out:json][timeout:25];
(
  node["landuse"~"cemetery"](52.33488609760638, 13.091992716067702, 52.67626223889507, 13.742786470433);
  way["landuse"~"cemetery"](52.33488609760638, 13.091992716067702, 52.67626223889507, 13.742786470433);
  relation["landuse"~"cemetery"](52.33488609760638, 13.091992716067702, 52.67626223889507, 13.742786470433);
);
out geom;
```

* for water use `"natural"~"water"`
* for park use `"leisure"~"park"`