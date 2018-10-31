# worldclim1-cr
Variables bioclimáticas de [WorldClim](http://www.worldclim.org) (versión 1) recortadas para Costa Rica.

Las capas se recortaron con el comando [gdalwarp](https://www.gdal.org/gdalwarp.html) de [GDAL](https://gdal.org/):
```
gdalwarp -dstnodata -9999 -tr 0.00833333 0.00833333 -q -cutline <capa-vectorial> -crop_to_cutline <capa-raster-entrada> <capa-raster-salida>
```

Por ejemplo:
```
gdalwarp -dstnodata -9999 -tr 0.00833333 0.00833333 -q -cutline costa-rica.shp -crop_to_cutline bio1.asc bio1_cr.asc
```

La capa vectorial para realizar el recorte puede obtenerse en [GADM](https://gadm.org).
