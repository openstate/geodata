The risk map lives at: http://nederland.risicokaart.nl/risicokaart.html

WFS endpoint: http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services

Examples
========

Get metadata of whole dataset:

    ogrinfo -so WFS:"http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services"
    
Get metadata of LPG layer:

    ogrinfo -so WFS:"http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services" 'app:p_lpg'

Get data from LPG layer in lat/lng using ogr2ogr:

    ogr2ogr -f GeoJSON lpg.geojson WFS:"http://nederland.deegree.risicokaart.nl/ogc_wms_wfs/services" 'app:p_lpg' -where "INDITB='J'" -t_srs "EPSG:4326"

Contact @simeonnedkov for more info.
