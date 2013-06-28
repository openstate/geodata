Data comes from [ruimtelijkeplannen.nl](http://www.ruimtelijkeplannen.nl). 

WFS endpoint: http://afnemers.ruimtelijkeplannen.nl/afnemers/services

Examples
========

Get metadata of dataset:

    ogrinfo -so WFS:"http://afnemers.ruimtelijkeplannen.nl/afnemers/services"
    
Get Provenciaalverbindingen layer as GeoJSON in lat/lng:

    ogr2ogr -f GeoJSON provenciaalverbindigen.geojson WFS:"http://afnemers.ruimtelijkeplannen.nl/afnemers/services" 'app:ProvinciaalVerbinding' -t_srs "EPSG:4326"
