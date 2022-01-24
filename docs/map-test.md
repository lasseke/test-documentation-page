Test if you can include html
 
 <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
   integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
   crossorigin=""/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
   
<style>
.info {
	padding: 8px;
	background-color: white;
	border: solid 1px black;
	font: 12pt Arial, Helvetica, sans-serif;
	word-wrap: break-word;
	-webkit-hyphens: auto;
	-moz-hyphens: auto;
	-ms-hyphens: auto;
	hyphens: auto;
}

.site-info {
	width: 200px;
	transition: height 1s;
}

.info h4 {
    margin: 0 0 5px;
}

.resetzoom {
	background: white;
	color: black !important;
	padding: 5px;
	border: solid 1pt black;
	border-radius: 5px;
	font: 14pt Arial, Helvetica, sans-serif;
}

.resetzoom:hover {
	background-color: rgba(211,211,211, 0.8) !important;
	cursor: pointer;
}

</style>
   
 <div id="map" style="height: 500px"></div>
   
 <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
   integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
   crossorigin=""></script>
   
<script type="text/javascript">
var map = L.map('map').setView([64.616667, 16.65], 4);
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

var nlpSites = {
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [8.12343, 61.0243]
      },
      "properties": {
        "name": "ALP1",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_ALP1.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [7.27596, 60.8231]
      },
      "properties": {
        "name": "ALP2",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_ALP2.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [7.17561, 60.8328]
      },
      "properties": {
        "name": "ALP3",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_ALP3.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [6.41504, 60.9335]
      },
      "properties": {
        "name": "ALP4",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_ALP4.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [8.70466, 60.8203]
      },
      "properties": {
        "name": "SUB1",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_SUB1.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [7.17666, 60.8760]
      },
      "properties": {
        "name": "SUB2",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_SUB2.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [6.63028, 61.0866]
      },
      "properties": {
        "name": "SUB3",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_SUB3.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [6.51468, 60.5445]
      },
      "properties": {
        "name": "SUB4",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_SUB4.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [9.07876, 61.0355]
      },
      "properties": {
        "name": "BOR1",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR1.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [7.16982, 60.8803]
      },
      "properties": {
        "name": "BOR2",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR2.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [6.33738, 60.6652]
      },
      "properties": {
        "name": "BOR3",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR3.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [5.96487, 60.6901]
      },
      "properties": {
        "name": "BOR4",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "SeedClim"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [7.527008533, 60.59383774]
      },
      "properties": {
        "name": "Finseflux",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [12.25481033, 61.10516357]
      },
      "properties": {
        "name": "Hisaasen_upper",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
	},
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [12.25089836, 61.1115036]
      },
      "properties": {
        "name": "Hisaasen_lower",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [25.29547425, 69.3408715]
      },
      "properties": {
        "name": "Iskoras",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [10.781667, 59.660278]
      },
      "properties": {
        "name": "Aas",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [11.078142, 60.372387]
      },
      "properties": {
        "name": "Hurdal",
        "res": "1x1",
        "url": "https://ns2806k.webs.sigma2.no/EMERALD/EMERALD_platform/inputdata_fates_platform/inputdata_version2.0.0_BOR4.tar",
        "group": "LaticeMIP"
      }
    }
  ]
};

var geojsonMarkerOptions = {
    radius: 6,
    fillColor: "#ff7800",
    color: "#000",
    weight: 1,
    opacity: 1,
    fillOpacity: 0.9
};


// Add hovering
function highlightFeature(e) {
    var layer = e.target;

    layer.setStyle({
        weight: 3,
        color: '#000',
		fillColor: '#DCDCDC',
        dashArray: '',
        fillOpacity: 0.7
    });

    if (!L.Browser.ie && !L.Browser.opera && !L.Browser.edge) {
        layer.bringToFront();
    }
	info.update(layer.feature.properties);
}

var geojson;

function resetHighlight(e) {
    geojson.resetStyle(e.target);
	info.update();
}

function zoomToFeature(e) {
	 map.setView(e.latlng, 7);
}



function onEachFeature(feature, layer) {
	layer.on({
        mouseover: highlightFeature,
        mouseout: resetHighlight,
        click: zoomToFeature
    });
    // Display box with site group name on click
    //if (feature.properties && feature.properties.name) {
    //    layer.bindPopup(feature.properties.name);
    //}
}

// Apply to geojson

geojson = L.geoJSON(nlpSites, {
    pointToLayer: function (feature, latlng) {
        return L.circleMarker(latlng, geojsonMarkerOptions);
    },
	style: function(feature) {
        switch (feature.properties.group) {
            case 'SeedClim': return {fillColor: "#50c878"};
            case 'LaticeMIP': return {fillColor: "#4169E1"};
        }
    },
	onEachFeature: onEachFeature
}).addTo(map);


// Add a legend

function getColor(d) {
        return d === 'SeedClim'  ? "#50c878" :
               d === 'LaticeMIP'  ? "#4169E1" :
                            "#ff7f00";
    }
	
var legend = L.control({position: 'bottomleft'});

legend.onAdd = function(map) {
    var div = L.DomUtil.create('div', 'info legend');
    labels = ['<strong>Sites</strong>'],
    categories = ['SeedClim', 'LaticeMIP'];

    for (var i = 0; i < categories.length; i++) {

            div.innerHTML += 
            labels.push(
                '<i class="fa fa-circle" style="color:' + getColor(categories[i]) + '"></i> ' +
            (categories[i] ? categories[i] : '+')
			);

        }
        div.innerHTML = labels.join('<br>');
    return div;
    };
legend.addTo(map);

// Add info box
var info = L.control();

info.onAdd = function (map) {
    this._div = L.DomUtil.create('div', 'info site-info'); // create a div with a class "info"
    this.update();
    return this._div;
};

// method that we will use to update the control based on feature properties passed
info.update = function (props) {
    this._div.innerHTML = '<h4>Site info</h4>' +  (props ?
        '<b>' + props.name + '</b><br />' + 'Additional site information will be shown here.'
        : 'Hover over a site.');
};

info.addTo(map);

// Reset zoom button
(function() {
	var control = new L.Control({position:'topleft'});
	control.onAdd = function(map) {
			var azoom = L.DomUtil.create('a','resetzoom leaflet-bar');
			azoom.innerHTML += '<i class="fa fa-refresh" aria-hidden="true"></i>';
			L.DomEvent
				.disableClickPropagation(azoom)
				.addListener(azoom, 'click', function() {
					map.setView([64.616667, 16.65], 4);
				},azoom);
			return azoom;
		};
	return control;
}())
.addTo(map);


</script>