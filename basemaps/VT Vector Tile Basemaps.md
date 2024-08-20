# Vermont Vector Tile Basemaps

# Examples

# USGS Topo
## [Sources](https://www.usgs.gov/faqs/what-sources-vector-data-were-used-create-base-maps-national-map)
- National Hydrography Dataset (NHD)
- Geographic Names Information System (GNIS)
- Census TIGER/Line data for Governmental Unit Boundaries, Structures, and Transportation

## Services

- [National Map Services](https://apps.nationalmap.gov/services/)
- [USGS Topo](https://basemap.nationalmap.gov/arcgis/rest/services/USGSTopo/MapServer)  - combines the most current data (boundaries, geographic names, transportation, elevation, hydrography, land cover, and other themes) that make up The National Map. Contours generated for the US Topo product are included and are visible along with other data to 1:9,000 zoom scale.
- [USGS Shaded Relief](https://basemap.nationalmap.gov/arcgis/rest/services/USGSShadedReliefOnly/MapServer) - created using data from the 3D Elevation Program (3DEP), which maintains a seamless dataset of best available raster elevation data for the conterminous United States, Alaska, Hawaii, and Territorial Islands of the U.S.  
- [USGS Imagery Only](http://basemap.nationalmap.gov/arcgis/rest/services/USGSImageryOnly/MapServer) - combines imagery from the U.S.; resolution may vary from 6 inches to 1 meter. 
- [USGS Imagery Topo](http://basemap.nationalmap.gov/arcgis/rest/services/USGSImageryTopo/MapServer) - combines imagery with contours and other vector themes (boundaries, geographic names, hydrography, structures, and transportation), based on cartographic styling used on US Topo products. 
- [Hydrography](https://basemap.nationalmap.gov/arcgis/rest/services/USGSHydroCached/MapServer) - combines naturally occurring and man-made bodies of surface water, paths through which water flows, and ​related features​ such as stream gages and dams​​, and additional hydrologic information​.
- [Base Map-Blank](https://basemap.nationalmap.gov/arcgis/rest/services/USGSTNMBlank/MapServer) - consists of ocean tints and coastlines to provide an outline of the United States as a blank base map for addition of other services.

## Symbols

- [USGS Topographic Map Symbol Sheet](https://www.usgs.gov/faqs/where-can-i-find-topographic-map-symbol-sheet) [(Sample)](https://www.usgs.gov/media/images/us-topo-map-symbol-file-sample)

## Projections

- Tiled Base Map Service: World Geodetic System 1984 (WGS 84) Web Mercator (Auxiliary Sphere)
- Dynamic Base Map Services: WGS 84 / [EPSG:4326](https://spatialreference.org/ref/epsg/4326/)
- Contours: Not projected, but provided in geographic coordinates (lat / lon) in units of decimal degrees, horizontally referenced to NAD 1983 datum. Elevation values referenced to NAVD 88 datum.
