Geodocs
=======

Notes and docs about geo processing (GDAL/OGR, etc.)


GDAL
----

Print reprojected coordinates of a point

```
echo 2 48 | gdaltransform  -s_srs EPSG:4326 -t_srs EPSG:27571
```

OGR
----

Shapefile to PostGIS
```
ogr2ogr -f PostgreSQL -nlt MULTILINESTRING PG:"host='host' dbname='dbname' user='user' password='password' port=port"  -lco SCHEMA=schema_name -lco OVERWRITE=YES -lco GEOMETRY_NAME=geom my_shapefile.shp
```
