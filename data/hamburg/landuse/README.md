# Landuse Data Hamburg

## About the data source

The geojson files in this data source present areas of different land use in Hamburg.

## Usage

Use [Overpass Turbo](https://overpass-turbo.eu/) to get all areas in a certain bounding box that have a given landuse using the syntax is as in the example below.
* replace `cemetery` in this example by any other [valid value for landuse](https://wiki.openstreetmap.org/wiki/Key:landuse)
* the coordinates specify the bounding box, in the example the city of Hamburg.

Then, export data as geojson file.

```
[out:json][timeout:25];
(
  node["landuse"~"cemetery"](53.1319, 7.7179, 54.2845, 10.7117);
  way["landuse"~"cemetery"](53.1319, 7.7179, 54.2845, 10.7117);
  relation["landuse"~"cemetery"](53.1319, 7.7179, 54.2845, 10.7117);
);
out geom;
```

* for water use `"natural"~"water"`
* for park use `"leisure"~"park"`
