The risk map lives at: http://nederland.risicokaart.nl/risicokaart.html

WFS endpoint: http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services

Get all LPG storage locations with 

    ogr2ogr -f GeoJSON lpg.geojson 
    WFS:"http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services"
    'app:p_lpg' -where "INDITB='J'"
