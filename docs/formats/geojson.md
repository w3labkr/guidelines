# GeoJson

GeoJSON is a format for encoding a variety of geographic data structures.

- [geojson.org](https://geojson.org){:target="_blank"}
- [en.wikipedia.org/wiki/GeoJSON](https://en.wikipedia.org/wiki/GeoJSON){:target="_blank"}

## Syntax

```json
{
  "type": "Feature", // Feature, FeatureCollection
  "geometry": {
    "type": "Point", // Point, LineString, Polygon, MultiPoint, MultiLineString, and MultiPolygon.
    "coordinates": [125.6, 10.1] // longitude, latitude
  },
  "properties": {
    "name": "Dinagat Islands"
  }
}
```

## GeoJSON Objects

Point

```json
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  }
}
```

MultiPoint

```json
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "MultiPoint",
                "coordinates": [
                    [10.0, 40.0], [40.0, 30.0], [20.0, 20.0], [30.0, 10.0]
                ]
            }
        }
    ]
}
```

LineString

```json
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "LineString",
                "coordinates": [
                    [30.0, 10.0], [10.0, 30.0], [40.0, 40.0]
                ]
            }
        }
    ]
}
```

MultiLineString

```json
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "MultiLineString",
                "coordinates": [
                    [[10.0, 10.0], [20.0, 20.0], [10.0, 40.0]], 
                    [[40.0, 40.0], [30.0, 30.0], [40.0, 20.0], [30.0, 10.0]]
                ]
            }
        }
    ]
}
```

Polygon

```json
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "Polygon",
                "coordinates": [
                    [[30.0, 10.0], [40.0, 40.0], [20.0, 40.0], [10.0, 20.0], [30.0, 10.0]]
                ]
            }
        }
    ]
}
```

MultiPolygon

```json
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "MultiPolygon",
                "coordinates": [
                    [
                        [[30.0, 20.0], [45.0, 40.0], [10.0, 40.0], [30.0, 20.0]]
                    ], 
                    [
                        [[15.0, 5.0], [40.0, 10.0], [10.0, 20.0], [5.0, 10.0], [15.0, 5.0]]
                    ]
                ]
            }
        }
    ]
}
```

GeometryCollection

```json
{
    "type": "GeometryCollection",
    "geometries": [
        {
            "type": "Point",
            "coordinates": [40.0, 10.0]
        },
        {
            "type": "LineString",
            "coordinates": [
                [10.0, 10.0], [20.0, 20.0], [10.0, 40.0]
            ]
        },
        {
            "type": "Polygon",
            "coordinates": [
                [[40.0, 40.0], [20.0, 45.0], [45.0, 30.0], [40.0, 40.0]]
            ]
        }
    ]
}
```
