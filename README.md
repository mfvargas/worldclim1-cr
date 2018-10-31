# worldclim1-cr
Variables bioclimáticas de [WorldClim](http://www.worldclim.org/) (versión 1) recortadas para Costa Rica.

Las capas se recortaron con el comando:
```
gdalwarp -dstnodata -9999 -tr 0.00833333 0.00833333 -q -cutline <capa-vectorial> -crop_to_cutline <capa-raster-entrada> <capa-raster-salida>
