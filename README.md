<!DOCTYPE html>
<html>
<head>
    
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    <script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.js"></script>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"/>
    <link rel="stylesheet" href="https://netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap-glyphicons.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.2.0/css/all.min.css"/>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/python-visualization/folium/folium/templates/leaflet.awesome.rotate.min.css"/>
    
            <meta name="viewport" content="width=device-width,
                initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
            <style>
                #map_51430b7ace495f57cdc23479ea843dd9 {
                    position: relative;
                    width: 100.0%;
                    height: 100.0%;
                    left: 0.0%;
                    top: 0.0%;
                }
                .leaflet-container { font-size: 1rem; }
            </style>

            <style>html, body {
                width: 100%;
                height: 100%;
                margin: 0;
                padding: 0;
            }
            </style>

            <style>#map {
                position:absolute;
                top:0;
                bottom:0;
                right:0;
                left:0;
                }
            </style>

            <script>
                L_NO_TOUCH = false;
                L_DISABLE_3D = false;
            </script>

        
    <script src="https://cdn.jsdelivr.net/gh/python-visualization/folium@main/folium/templates/leaflet_heat.min.js"></script>
</head>
<body>
    
    
<style>
.painel {
    position: fixed;
    z-index: 9999;
    padding: 10px;
    border-radius: 10px;
    text-align: center;
    font-family: Arial, Helvetica, sans-serif;
    background: rgba(255,255,255,0.92);
    box-shadow: 1px 2px 6px rgba(0,0,0,0.25);
}

/* Desktop */
@media (min-width: 769px) {
    #painel-total { left: 20px; bottom: 30px; width: 200px; }
    #painel-ipo   { right: 280px; bottom: 30px; width: 260px; background:#ecfdf5; }
    #painel-ido   { right: 20px; bottom: 30px; width: 260px; background:#fef2f2; }
}

/* Mobile */
@media (max-width: 768px) {
    .painel {
        left: 50% !important;
        transform: translateX(-50%);
        width: 80% !important;
        padding: 6px !important;
        font-size: 10px;
        box-shadow: 0px 1px 3px rgba(0,0,0,0.2);
    }

    .painel .valor {
        font-size: 16px;
        font-weight: bold;
    }

    #painel-total { bottom: 130px; }
    #painel-ipo   { bottom: 75px; }
    #painel-ido   { bottom: 20px; }
}
</style>
    
            <div class="folium-map" id="map_51430b7ace495f57cdc23479ea843dd9" ></div>
        
    
<div id="painel-total" class="painel">
    <b>🔢 Total de Ovos</b>
    <div class="valor">14226</div>
</div>
    
<div id="painel-ipo" class="painel">
    <b>🟢 Índice de Positividade de Ovitrampas (IPO)</b>
    <div class="valor">73%</div>
</div>
    
<div id="painel-ido" class="painel">
    <b>🔴 Índice de Densidade de Ovos (IDO)</b>
    <div class="valor">89</div>
</div>
    
<div style="
    position: fixed;
    top: 8px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 9999;
    background: rgba(30,58,138,0.85);
    color: white;
    padding: 6px 14px;
    border-radius: 10px;
    box-shadow: 0px 3px 8px rgba(0,0,0,0.3);
    text-align: center;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 14px;
">
    <b>Instalação de Ovitrampas • Janeiro/2026</b>
</div>
</body>
<script>
    
    
            var map_51430b7ace495f57cdc23479ea843dd9 = L.map(
                "map_51430b7ace495f57cdc23479ea843dd9",
                {
                    center: [-22.5304, -55.66],
                    crs: L.CRS.EPSG3857,
                    ...{
  "zoom": 13,
  "zoomControl": true,
  "preferCanvas": false,
}

                }
            );

            

        
    
            var tile_layer_05412c672755a4d51f734ef6aff58071 = L.tileLayer(
                "https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png",
                {
  "minZoom": 0,
  "maxZoom": 20,
  "maxNativeZoom": 20,
  "noWrap": false,
  "attribution": "\u0026copy; \u003ca href=\"https://www.openstreetmap.org/copyright\"\u003eOpenStreetMap\u003c/a\u003e contributors \u0026copy; \u003ca href=\"https://carto.com/attributions\"\u003eCARTO\u003c/a\u003e",
  "subdomains": "abcd",
  "detectRetina": false,
  "tms": false,
  "opacity": 1,
}

            );
        
    
            tile_layer_05412c672755a4d51f734ef6aff58071.addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            var heat_map_160fab88ddb8cbe4394c3fe75bcdb333 = L.heatLayer(
                [[-22.57584224, -55.6760529, 41.0], [-22.57531435, -55.68473061, 7.0], [-22.52719331, -55.71117505, 41.0], [-22.52761064, -55.71482031, 69.0], [-22.52836381, -55.7178673, 0.0], [-22.52690007, -55.72389433, 0.0], [-22.52915021, -55.72695016, 124.0], [-22.52732321, -55.73038809, 13.0], [-22.5272091, -55.73398727, 219.0], [-22.52708862, -55.73718552, 75.0], [-22.52385148, -55.73801071, 190.0], [-22.5236532, -55.73380397, 54.0], [-22.57479302, -55.68840108, 53.0], [-22.52405001, -55.72976124, 0.0], [-22.52418281, -55.72567349, 2.0], [-22.52473559, -55.72166349, 59.0], [-22.52338114, -55.71824844, 43.0], [-22.52398929, -55.7145624, 26.0], [-22.52390475, -55.71092148, 14.0], [-22.52285326, -55.70818863, 6.0], [-22.52033523, -55.70754287, 0.0], [-22.52065237, -55.71061132, 122.0], [-22.52117094, -55.71376414, 0.0], [-22.5735426, -55.6900654, 130.0], [-22.52040426, -55.71869739, 0.0], [-22.52052319, -55.72195895, 115.0], [-22.52049352, -55.72694745, 0.0], [-22.52067455, -55.73050767, 94.0], [-22.52053197, -55.73407822, 0.0], [-22.52126754, -55.73871798, 83.0], [-22.51668534, -55.74004556, 72.0], [-22.51672091, -55.73791244, 15.0], [-22.51642095, -55.73429687, 0.0], [-22.5167767, -55.73001809, 26.0], [-22.5705674, -55.69340743, 178.0], [-22.51678523, -55.7271761, 38.0], [-22.51692195, -55.72226979, 61.0], [-22.51666426, -55.71834303, 15.0], [-22.5166048, -55.71508147, 0.0], [-22.51713999, -55.71058231, 24.0], [-22.51692195, -55.70633369, 20.0], [-22.51231232, -55.70392708, 110.0], [-22.5130476, -55.70696636, 2.0], [-22.51364227, -55.71127935, 14.0], [-22.51341222, -55.71906242, 70.0], [-22.57044573, -55.69106854, 120.0], [-22.51345428, -55.72245168, 7.0], [-22.51377404, -55.72694158, 44.0], [-22.51318072, -55.72994623, 0.0], [-22.51319383, -55.73272855, 32.0], [-22.51425869, -55.73720417, 71.0], [-22.51331713, -55.74165512, 144.0], [-22.50933567, -55.744296, 14.0], [-22.51099954, -55.74075163, 0.0], [-22.50900734, -55.73800202, 2.0], [-22.50938398, -55.73396798, 53.0], [-22.57111941, -55.68770036, 157.0], [-22.50958493, -55.72925073, 210.0], [-22.50955027, -55.72637296, 142.0], [-22.50954528, -55.72227699, 60.0], [-22.5098164, -55.71878692, 0.0], [-22.50921416, -55.71437454, 54.0], [-22.50857908, -55.71158549, 172.0], [-22.50978823, -55.70647045, 312.0], [-22.50983738, -55.70268828, 79.0], [-22.50727471, -55.70334382, 193.0], [-22.50477635, -55.70510288, 174.0], [-22.57010889, -55.68375516, 184.0], [-22.50627046, -55.71051287, 202.0], [-22.50645819, -55.71447905, 251.0], [-22.50525042, -55.7188348, 54.0], [-22.50554777, -55.7226384, 16.0], [-22.50639331, -55.72587588, 149.0], [-22.50576527, -55.72971731, 2.0], [-22.50542325, -55.73375148, 71.0], [-22.50534592, -55.73772283, 0.0], [-22.50514894, -55.74050527, 58.0], [-22.50701371, -55.74597973, 0.0], [-22.57063149, -55.67978817, 0.0], [-22.50146106, -55.74452021, 23.0], [-22.50139, -55.74182, 7.0], [-22.5031051, -55.7374472, 104.0], [-22.5028065, -55.7343831, 73.0], [-22.5022768, -55.7299891, 96.0], [-22.5031554, -55.7251693, 64.0], [-22.5027842, -55.7227262, 0.0], [-22.5026854, -55.7188097, 0.0], [-22.5024656, -55.714133, 0.0], [-22.5025676, -55.7108878, 75.0], [-22.5682846, -55.68028402, 6.0], [-22.50032085, -55.7061126, 126.0], [-22.50231468, -55.70325266, 10.0], [-22.50017222, -55.7112595, 62.0], [-22.50053678, -55.71331495, 520.0], [-22.50001124, -55.71985932, 171.0], [-22.49946231, -55.72355661, 201.0], [-22.49819668, -55.72689149, 0.0], [-22.49870783, -55.72983113, 87.0], [-22.49783745, -55.73461993, 0.0], [-22.4979825, -55.73792295, 0.0], [-22.56724, -55.68382, 0.0], [-22.4986098, -55.74304352, 0.0], [-22.4988367, -55.74515834, 0.0], [-22.49617872, -55.74713457, 88.0], [-22.49628778, -55.73990185, 53.0], [-22.49632113, -55.73878276, 228.0], [-22.49666023, -55.73391721, 53.0], [-22.4970815, -55.72979311, 0.0], [-22.49650967, -55.7263839, 62.0], [-22.4936467, -55.7226377, 25.0], [-22.49116257, -55.7215439, 162.0], [-22.5779, -55.6764, 430.0], [-22.56656, -55.68697, 138.0], [-22.4902874, -55.7200612, 34.0], [-22.48802846, -55.71931609, 206.0], [-22.48801109, -55.72404936, 115.0], [-22.48766553, -55.72511016, 112.0], [-22.4873515, -55.7298789, 33.0], [-22.48818079, -55.73509419, 16.0], [-22.48871469, -55.73913911, 161.0], [-22.49020821, -55.73962428, 63.0], [-22.49098529, -55.74134939, 0.0], [-22.49150077, -55.74378623, 64.0], [-22.566694, -55.6913, 117.0], [-22.48803216, -55.74071125, 246.0], [-22.48732976, -55.74644901, 189.0], [-22.48434491, -55.74671995, 0.0], [-22.48470312, -55.74143382, 0.0], [-22.48431027, -55.73752904, 0.0], [-22.48438909, -55.73413104, 0.0], [-22.48431098, -55.72997452, 38.0], [-22.48395125, -55.72652514, 67.0], [-22.48369608, -55.72214773, 0.0], [-22.48467409, -55.71951625, 28.0], [-22.5672, -55.69403, 0.0], [-22.48289608, -55.72487163, 174.0], [-22.48314383, -55.72929089, 72.0], [-22.48212634, -55.73429815, 0.0], [-22.4823279, -55.7372452, 0.0], [-22.47707396, -55.74909308, 8.0], [-22.562942, -55.6969912, 33.0], [-22.5634, -55.69371, 179.0], [-22.5640244, -55.6904818, 78.0], [-22.5641021, -55.6874434, 0.0], [-22.56442967, -55.68365741, 64.0], [-22.5648934, -55.6810013, 81.0], [-22.56053231, -55.68016491, 0.0], [-22.577616, -55.679396, 390.0], [-22.56009637, -55.68385563, 88.0], [-22.56079166, -55.68720333, 0.0], [-22.56045641, -55.69067182, 0.0], [-22.55937153, -55.6949, 62.0], [-22.56009279, -55.69914141, 6.0], [-22.55979556, -55.70320148, 0.0], [-22.556385, -55.70201166, 27.0], [-22.55726744, -55.69791178, 78.0], [-22.55638099, -55.69586885, 5.0], [-22.55773225, -55.68933692, 68.0], [-22.58104476, -55.67673754, 0.0], [-22.5571292, -55.68760542, 0.0], [-22.55862573, -55.68488637, 0.0], [-22.55755915, -55.68152588, 178.0], [-22.5548586, -55.68896148, 115.0], [-22.55391505, -55.69039213, 60.0], [-22.5548915, -55.6957812, 110.0], [-22.55286999, -55.69942617, 71.0], [-22.55357348, -55.70128226, 22.0], [-22.55065504, -55.70117672, 29.0], [-22.549574, -55.69930225, 9.0], [-22.58085813, -55.67906827, 0.0], [-22.5486603, -55.69458274, 29.0], [-22.54833158, -55.69155276, 95.0], [-22.54611011, -55.69863444, 64.0], [-22.54608832, -55.69531537, 0.0], [-22.54556159, -55.6908646, 18.0], [-22.544984, -55.687216, 10.0], [-22.542453, -55.686857, 71.0], [-22.53912, -55.687667, 35.0], [-22.53966321, -55.69000849, 120.0], [-22.5408563, -55.69035025, 97.0], [-22.57986535, -55.68208349, 84.0], [-22.541706, -55.702726, 1.0], [-22.54275098, -55.70680137, 58.0], [-22.54567056, -55.70727567, 51.0], [-22.54544707, -55.70352569, 0.0], [-22.54774357, -55.70468267, 76.0], [-22.54947595, -55.70797873, 0.0], [-22.55039674, -55.70920915, 0.0], [-22.5517427, -55.70782915, 0.0], [-22.55605024, -55.70756005, 0.0], [-22.55660728, -55.71097685, 38.0], [-22.5818827, -55.6831812, 146.0], [-22.55573954, -55.71435028, 0.0], [-22.55295413, -55.71023103, 0.0], [-22.55311267, -55.71441528, 0.0], [-22.55334074, -55.71837031, 0.0], [-22.55199534, -55.72196827, 144.0], [-22.54962682, -55.7193726, 0.0], [-22.54909175, -55.72229084, 0.0], [-22.54831054, -55.7247322, 0.0], [-22.54567651, -55.72658292, 0.0], [-22.54564195, -55.72230274, 0.0], [-22.5807243, -55.6872979, 24.0], [-22.54249538, -55.72337506, 102.0], [-22.54217829, -55.72620747, 21.0], [-22.54125839, -55.72820898, 0.0], [-22.53820736, -55.72967611, 72.0], [-22.53743065, -55.72608181, 2.0], [-22.53795928, -55.72274902, 37.0], [-22.53737405, -55.71968077, 34.0], [-22.53440856, -55.71515989, 244.0], [-22.53492307, -55.71827699, 50.0], [-22.53515099, -55.72197843, 42.0], [-22.5777256, -55.6879824, 46.0], [-22.53550773, -55.72576491, 83.0], [-22.53549782, -55.72909396, 0.0], [-22.53485629, -55.73268543, 82.0], [-22.53130475, -55.73349033, 360.0], [-22.53148313, -55.72986398, 0.0], [-22.53128493, -55.7260016, 13.0], [-22.53170396, -55.72274168, 0.0], [-22.53109044, -55.71834445, 29.0], [-22.53083278, -55.71497559, 107.0], [-22.53000035, -55.71149945, 129.0]],
                {
  "minOpacity": 0.5,
  "maxZoom": 18,
  "radius": 22,
  "blur": 16,
  "gradient": {
  0.0: "white",
  0.35: "green",
  0.7: "yellow",
  1.0: "red",
},
}
            );
        
    
            heat_map_160fab88ddb8cbe4394c3fe75bcdb333.addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            var circle_marker_8a0966a7440fbc1e16ca29077b8c708b = L.circleMarker(
                [-22.57584224, -55.6760529],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8a0966a7440fbc1e16ca29077b8c708b.bindTooltip(
                `<div>
                     Ovitrampa ID: 1.0<br>Nº de ovos: 41
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3ab7dcf2a16c826915a65368cd7cb4a6 = L.circleMarker(
                [-22.57531435, -55.68473061],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3ab7dcf2a16c826915a65368cd7cb4a6.bindTooltip(
                `<div>
                     Ovitrampa ID: 10.0<br>Nº de ovos: 7
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6d313e81cd6bbf40fe795050356f392a = L.circleMarker(
                [-22.52719331, -55.71117505],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6d313e81cd6bbf40fe795050356f392a.bindTooltip(
                `<div>
                     Ovitrampa ID: 100.0<br>Nº de ovos: 41
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_029d2b2dcccb9ed9b111ac84e58b0af0 = L.circleMarker(
                [-22.52761064, -55.71482031],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_029d2b2dcccb9ed9b111ac84e58b0af0.bindTooltip(
                `<div>
                     Ovitrampa ID: 101.0<br>Nº de ovos: 69
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8a065a1b2cc1419c1c421ef8bb1101cf = L.circleMarker(
                [-22.52836381, -55.7178673],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8a065a1b2cc1419c1c421ef8bb1101cf.bindTooltip(
                `<div>
                     Ovitrampa ID: 102.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6f21f729ea4dbffb6319e518907fef74 = L.circleMarker(
                [-22.52690007, -55.72389433],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6f21f729ea4dbffb6319e518907fef74.bindTooltip(
                `<div>
                     Ovitrampa ID: 103.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_18ac9cf425b4a11ea8a80cb5a296aa5e = L.circleMarker(
                [-22.52915021, -55.72695016],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_18ac9cf425b4a11ea8a80cb5a296aa5e.bindTooltip(
                `<div>
                     Ovitrampa ID: 104.0<br>Nº de ovos: 124
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_492707ceb5f563c6e1ac578edfa9870c = L.circleMarker(
                [-22.52732321, -55.73038809],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_492707ceb5f563c6e1ac578edfa9870c.bindTooltip(
                `<div>
                     Ovitrampa ID: 105.0<br>Nº de ovos: 13
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6a2b5dd9d8081766727aca938ab45cfb = L.circleMarker(
                [-22.5272091, -55.73398727],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6a2b5dd9d8081766727aca938ab45cfb.bindTooltip(
                `<div>
                     Ovitrampa ID: 106.0<br>Nº de ovos: 219
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_10afe965698d3f122e746369c17f233f = L.circleMarker(
                [-22.52708862, -55.73718552],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_10afe965698d3f122e746369c17f233f.bindTooltip(
                `<div>
                     Ovitrampa ID: 107.0<br>Nº de ovos: 75
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d455c203befef51439360ae43ae5269c = L.circleMarker(
                [-22.52385148, -55.73801071],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d455c203befef51439360ae43ae5269c.bindTooltip(
                `<div>
                     Ovitrampa ID: 108.0<br>Nº de ovos: 190
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_25afccaeb17d837556fd702c4f2836d9 = L.circleMarker(
                [-22.5236532, -55.73380397],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_25afccaeb17d837556fd702c4f2836d9.bindTooltip(
                `<div>
                     Ovitrampa ID: 109.0<br>Nº de ovos: 54
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_198d557a57ff5cdd3f4257c1ef5960ce = L.circleMarker(
                [-22.57479302, -55.68840108],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_198d557a57ff5cdd3f4257c1ef5960ce.bindTooltip(
                `<div>
                     Ovitrampa ID: 11.0<br>Nº de ovos: 53
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9b1667d0355b3615c87f93a0db1aabc7 = L.circleMarker(
                [-22.52405001, -55.72976124],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9b1667d0355b3615c87f93a0db1aabc7.bindTooltip(
                `<div>
                     Ovitrampa ID: 110.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a03e15a66b2a9e8be116de4feffc9ae9 = L.circleMarker(
                [-22.52418281, -55.72567349],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a03e15a66b2a9e8be116de4feffc9ae9.bindTooltip(
                `<div>
                     Ovitrampa ID: 111.0<br>Nº de ovos: 2
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_be3f20bdffffdd713aa1d48a32a823d2 = L.circleMarker(
                [-22.52473559, -55.72166349],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_be3f20bdffffdd713aa1d48a32a823d2.bindTooltip(
                `<div>
                     Ovitrampa ID: 112.0<br>Nº de ovos: 59
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ae0044b3494e372633a6f684eeeac278 = L.circleMarker(
                [-22.52338114, -55.71824844],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ae0044b3494e372633a6f684eeeac278.bindTooltip(
                `<div>
                     Ovitrampa ID: 113.0<br>Nº de ovos: 43
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a2fc6af96530503320027e526ac2e922 = L.circleMarker(
                [-22.52398929, -55.7145624],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a2fc6af96530503320027e526ac2e922.bindTooltip(
                `<div>
                     Ovitrampa ID: 114.0<br>Nº de ovos: 26
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4c1a0b994fd9cefe05290a0d9a6dbeff = L.circleMarker(
                [-22.52390475, -55.71092148],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4c1a0b994fd9cefe05290a0d9a6dbeff.bindTooltip(
                `<div>
                     Ovitrampa ID: 115.0<br>Nº de ovos: 14
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ee5b8299a509e7dbba8aaab97c691cbf = L.circleMarker(
                [-22.52285326, -55.70818863],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ee5b8299a509e7dbba8aaab97c691cbf.bindTooltip(
                `<div>
                     Ovitrampa ID: 116.0<br>Nº de ovos: 6
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_274820bd04a85c942512a45fabf6c6b2 = L.circleMarker(
                [-22.52033523, -55.70754287],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_274820bd04a85c942512a45fabf6c6b2.bindTooltip(
                `<div>
                     Ovitrampa ID: 117.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_0b321ef3b2977e0292fb590eaa551a1c = L.circleMarker(
                [-22.52065237, -55.71061132],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_0b321ef3b2977e0292fb590eaa551a1c.bindTooltip(
                `<div>
                     Ovitrampa ID: 118.0<br>Nº de ovos: 122
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a55a9377dac3e037f35acd303d5e3a80 = L.circleMarker(
                [-22.52117094, -55.71376414],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a55a9377dac3e037f35acd303d5e3a80.bindTooltip(
                `<div>
                     Ovitrampa ID: 119.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d576ee6d369e084a48c0733ca9b4bae2 = L.circleMarker(
                [-22.5735426, -55.6900654],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d576ee6d369e084a48c0733ca9b4bae2.bindTooltip(
                `<div>
                     Ovitrampa ID: 12.0<br>Nº de ovos: 130
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4f8b8cad1fe2b062187ea12f5675fe79 = L.circleMarker(
                [-22.52040426, -55.71869739],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4f8b8cad1fe2b062187ea12f5675fe79.bindTooltip(
                `<div>
                     Ovitrampa ID: 120.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f96d86b8878a67adbc2d540e2452844c = L.circleMarker(
                [-22.52052319, -55.72195895],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f96d86b8878a67adbc2d540e2452844c.bindTooltip(
                `<div>
                     Ovitrampa ID: 121.0<br>Nº de ovos: 115
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_99a03d7f6c903979ec5bc391d092ccc3 = L.circleMarker(
                [-22.52049352, -55.72694745],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_99a03d7f6c903979ec5bc391d092ccc3.bindTooltip(
                `<div>
                     Ovitrampa ID: 122.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b7b598f8a63963e21686e460f970e525 = L.circleMarker(
                [-22.52067455, -55.73050767],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b7b598f8a63963e21686e460f970e525.bindTooltip(
                `<div>
                     Ovitrampa ID: 123.0<br>Nº de ovos: 94
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7dc0ec3a5add477143e6036b17f1fb24 = L.circleMarker(
                [-22.52053197, -55.73407822],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7dc0ec3a5add477143e6036b17f1fb24.bindTooltip(
                `<div>
                     Ovitrampa ID: 124.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_170b4e6455426dc8ecdcbafbcf745854 = L.circleMarker(
                [-22.52126754, -55.73871798],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_170b4e6455426dc8ecdcbafbcf745854.bindTooltip(
                `<div>
                     Ovitrampa ID: 125.0<br>Nº de ovos: 83
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_945cb768dd039dc19ab8f13d8d1b17c1 = L.circleMarker(
                [-22.51668534, -55.74004556],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_945cb768dd039dc19ab8f13d8d1b17c1.bindTooltip(
                `<div>
                     Ovitrampa ID: 126.0<br>Nº de ovos: 72
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_926e5b100994f65c1a2428acd3a71883 = L.circleMarker(
                [-22.51672091, -55.73791244],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_926e5b100994f65c1a2428acd3a71883.bindTooltip(
                `<div>
                     Ovitrampa ID: 127.0<br>Nº de ovos: 15
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ec49aee18dce0594e07267c0026c4505 = L.circleMarker(
                [-22.51642095, -55.73429687],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ec49aee18dce0594e07267c0026c4505.bindTooltip(
                `<div>
                     Ovitrampa ID: 128.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ce0afc50ea99550044294622d98aeab1 = L.circleMarker(
                [-22.5167767, -55.73001809],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ce0afc50ea99550044294622d98aeab1.bindTooltip(
                `<div>
                     Ovitrampa ID: 129.0<br>Nº de ovos: 26
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6cf692774e94a12253302c96341ce6c7 = L.circleMarker(
                [-22.5705674, -55.69340743],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6cf692774e94a12253302c96341ce6c7.bindTooltip(
                `<div>
                     Ovitrampa ID: 13.0<br>Nº de ovos: 178
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a52aec53936958a0fd897eb72993ff09 = L.circleMarker(
                [-22.51678523, -55.7271761],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a52aec53936958a0fd897eb72993ff09.bindTooltip(
                `<div>
                     Ovitrampa ID: 130.0<br>Nº de ovos: 38
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3f28cdd94a1ee5caf086813894063165 = L.circleMarker(
                [-22.51692195, -55.72226979],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3f28cdd94a1ee5caf086813894063165.bindTooltip(
                `<div>
                     Ovitrampa ID: 131.0<br>Nº de ovos: 61
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2fa50d0b7a3bf06bb768fe76c9e22ba4 = L.circleMarker(
                [-22.51666426, -55.71834303],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2fa50d0b7a3bf06bb768fe76c9e22ba4.bindTooltip(
                `<div>
                     Ovitrampa ID: 132.0<br>Nº de ovos: 15
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4a3c6d4cb60e5a55d2ee67c8871d4121 = L.circleMarker(
                [-22.5166048, -55.71508147],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4a3c6d4cb60e5a55d2ee67c8871d4121.bindTooltip(
                `<div>
                     Ovitrampa ID: 133.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_369221b4038d94f94a41df57ac0480ed = L.circleMarker(
                [-22.51713999, -55.71058231],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_369221b4038d94f94a41df57ac0480ed.bindTooltip(
                `<div>
                     Ovitrampa ID: 134.0<br>Nº de ovos: 24
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_aa2481f83713e70e519e0c16e6706c9c = L.circleMarker(
                [-22.51692195, -55.70633369],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_aa2481f83713e70e519e0c16e6706c9c.bindTooltip(
                `<div>
                     Ovitrampa ID: 135.0<br>Nº de ovos: 20
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_be3a26f1cc4c0035bdd0d85f6aa9c3b5 = L.circleMarker(
                [-22.51231232, -55.70392708],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_be3a26f1cc4c0035bdd0d85f6aa9c3b5.bindTooltip(
                `<div>
                     Ovitrampa ID: 136.0<br>Nº de ovos: 110
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_bff5d19d9aeaee4e1ae9395dfc80451a = L.circleMarker(
                [-22.5130476, -55.70696636],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_bff5d19d9aeaee4e1ae9395dfc80451a.bindTooltip(
                `<div>
                     Ovitrampa ID: 137.0<br>Nº de ovos: 2
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_899b0f08d688376bbbb68463c6aea448 = L.circleMarker(
                [-22.51364227, -55.71127935],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_899b0f08d688376bbbb68463c6aea448.bindTooltip(
                `<div>
                     Ovitrampa ID: 138.0<br>Nº de ovos: 14
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9d4c7808814f28d5abcc72a5c7d4dd26 = L.circleMarker(
                [-22.51341222, -55.71906242],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9d4c7808814f28d5abcc72a5c7d4dd26.bindTooltip(
                `<div>
                     Ovitrampa ID: 139.0<br>Nº de ovos: 70
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_56287bd087cf3f00fe50fa216df11542 = L.circleMarker(
                [-22.57044573, -55.69106854],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_56287bd087cf3f00fe50fa216df11542.bindTooltip(
                `<div>
                     Ovitrampa ID: 14.0<br>Nº de ovos: 120
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c9ae17fc8632515149c0eba7445c8dab = L.circleMarker(
                [-22.51345428, -55.72245168],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c9ae17fc8632515149c0eba7445c8dab.bindTooltip(
                `<div>
                     Ovitrampa ID: 140.0<br>Nº de ovos: 7
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_72f34e3c7c8eeefa3769dd64adf2c00e = L.circleMarker(
                [-22.51377404, -55.72694158],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_72f34e3c7c8eeefa3769dd64adf2c00e.bindTooltip(
                `<div>
                     Ovitrampa ID: 141.0<br>Nº de ovos: 44
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_aa2a2e8e105e2d89c101761e53baf96e = L.circleMarker(
                [-22.51318072, -55.72994623],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_aa2a2e8e105e2d89c101761e53baf96e.bindTooltip(
                `<div>
                     Ovitrampa ID: 142.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ccfd5be4b9b7f50b8d5918384e0c0b9b = L.circleMarker(
                [-22.51319383, -55.73272855],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ccfd5be4b9b7f50b8d5918384e0c0b9b.bindTooltip(
                `<div>
                     Ovitrampa ID: 143.0<br>Nº de ovos: 32
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3b97658cedeff6d5685fdcf52642e3b4 = L.circleMarker(
                [-22.51425869, -55.73720417],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3b97658cedeff6d5685fdcf52642e3b4.bindTooltip(
                `<div>
                     Ovitrampa ID: 144.0<br>Nº de ovos: 71
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_531f1ed82f35bd7c46cd24523e0e730b = L.circleMarker(
                [-22.51331713, -55.74165512],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_531f1ed82f35bd7c46cd24523e0e730b.bindTooltip(
                `<div>
                     Ovitrampa ID: 145.0<br>Nº de ovos: 144
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2e09e95b9e0fbf9242b871b661baaa21 = L.circleMarker(
                [-22.50933567, -55.744296],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2e09e95b9e0fbf9242b871b661baaa21.bindTooltip(
                `<div>
                     Ovitrampa ID: 146.0<br>Nº de ovos: 14
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_cf06feb656a723a6d2b0613a6af4174c = L.circleMarker(
                [-22.51099954, -55.74075163],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_cf06feb656a723a6d2b0613a6af4174c.bindTooltip(
                `<div>
                     Ovitrampa ID: 147.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_358ccfbb6e1bbf20f57984034ebeb3ab = L.circleMarker(
                [-22.50900734, -55.73800202],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_358ccfbb6e1bbf20f57984034ebeb3ab.bindTooltip(
                `<div>
                     Ovitrampa ID: 148.0<br>Nº de ovos: 2
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_eae13903d0533b1a493648689aae42a9 = L.circleMarker(
                [-22.50938398, -55.73396798],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_eae13903d0533b1a493648689aae42a9.bindTooltip(
                `<div>
                     Ovitrampa ID: 149.0<br>Nº de ovos: 53
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_505c94d71effaa88ade948404ac80b61 = L.circleMarker(
                [-22.57111941, -55.68770036],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_505c94d71effaa88ade948404ac80b61.bindTooltip(
                `<div>
                     Ovitrampa ID: 15.0<br>Nº de ovos: 157
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4241dad3b433f9ddf0179dae3bd71bd0 = L.circleMarker(
                [-22.50958493, -55.72925073],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4241dad3b433f9ddf0179dae3bd71bd0.bindTooltip(
                `<div>
                     Ovitrampa ID: 150.0<br>Nº de ovos: 210
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_acecca7c5a59bbc5e6acf4db161f92b9 = L.circleMarker(
                [-22.50955027, -55.72637296],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_acecca7c5a59bbc5e6acf4db161f92b9.bindTooltip(
                `<div>
                     Ovitrampa ID: 151.0<br>Nº de ovos: 142
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_04e9ba635f7701168400dc1d0626f81a = L.circleMarker(
                [-22.50954528, -55.72227699],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_04e9ba635f7701168400dc1d0626f81a.bindTooltip(
                `<div>
                     Ovitrampa ID: 152.0<br>Nº de ovos: 60
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_fdc1a565328d5257093154cfa4854630 = L.circleMarker(
                [-22.5098164, -55.71878692],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_fdc1a565328d5257093154cfa4854630.bindTooltip(
                `<div>
                     Ovitrampa ID: 153.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e5e2b69bc974dfc9e1c5250e6179421e = L.circleMarker(
                [-22.50921416, -55.71437454],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e5e2b69bc974dfc9e1c5250e6179421e.bindTooltip(
                `<div>
                     Ovitrampa ID: 154.0<br>Nº de ovos: 54
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6b07cfe6bfe8a20472bbdbaeb639aff6 = L.circleMarker(
                [-22.50857908, -55.71158549],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6b07cfe6bfe8a20472bbdbaeb639aff6.bindTooltip(
                `<div>
                     Ovitrampa ID: 155.0<br>Nº de ovos: 172
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b238d6f6f42473357be4669bcbd02ee3 = L.circleMarker(
                [-22.50978823, -55.70647045],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b238d6f6f42473357be4669bcbd02ee3.bindTooltip(
                `<div>
                     Ovitrampa ID: 156.0<br>Nº de ovos: 312
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_48f54407df02abbe2614e0f54199b3ff = L.circleMarker(
                [-22.50983738, -55.70268828],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_48f54407df02abbe2614e0f54199b3ff.bindTooltip(
                `<div>
                     Ovitrampa ID: 157.0<br>Nº de ovos: 79
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4ed651200fa2d54696cf8f3b541fb20c = L.circleMarker(
                [-22.50727471, -55.70334382],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4ed651200fa2d54696cf8f3b541fb20c.bindTooltip(
                `<div>
                     Ovitrampa ID: 158.0<br>Nº de ovos: 193
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_0cb190162cb58e393076f17a4391a996 = L.circleMarker(
                [-22.50477635, -55.70510288],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_0cb190162cb58e393076f17a4391a996.bindTooltip(
                `<div>
                     Ovitrampa ID: 159.0<br>Nº de ovos: 174
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_646965bfbfe5624dbe894df7a3d80609 = L.circleMarker(
                [-22.57010889, -55.68375516],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_646965bfbfe5624dbe894df7a3d80609.bindTooltip(
                `<div>
                     Ovitrampa ID: 16.0<br>Nº de ovos: 184
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_93b60cb4871a50229d7c7b802f5abfac = L.circleMarker(
                [-22.50627046, -55.71051287],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_93b60cb4871a50229d7c7b802f5abfac.bindTooltip(
                `<div>
                     Ovitrampa ID: 160.0<br>Nº de ovos: 202
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_561bbb671696cf331c24279c7d6a0678 = L.circleMarker(
                [-22.50645819, -55.71447905],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_561bbb671696cf331c24279c7d6a0678.bindTooltip(
                `<div>
                     Ovitrampa ID: 161.0<br>Nº de ovos: 251
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7e2fe0390145bd191f84f34b7270a2b7 = L.circleMarker(
                [-22.50525042, -55.7188348],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7e2fe0390145bd191f84f34b7270a2b7.bindTooltip(
                `<div>
                     Ovitrampa ID: 162.0<br>Nº de ovos: 54
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_eb9cd4ed6981a51707ba7e310d4c7a33 = L.circleMarker(
                [-22.50554777, -55.7226384],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_eb9cd4ed6981a51707ba7e310d4c7a33.bindTooltip(
                `<div>
                     Ovitrampa ID: 163.0<br>Nº de ovos: 16
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2f1c450b154f74c9af02efe2c306d8ef = L.circleMarker(
                [-22.50639331, -55.72587588],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2f1c450b154f74c9af02efe2c306d8ef.bindTooltip(
                `<div>
                     Ovitrampa ID: 164.0<br>Nº de ovos: 149
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_5d0eaa7775153006f40def7b6925bd02 = L.circleMarker(
                [-22.50576527, -55.72971731],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_5d0eaa7775153006f40def7b6925bd02.bindTooltip(
                `<div>
                     Ovitrampa ID: 165.0<br>Nº de ovos: 2
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2191a3bc9ea77e17591e05299eda62ae = L.circleMarker(
                [-22.50542325, -55.73375148],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2191a3bc9ea77e17591e05299eda62ae.bindTooltip(
                `<div>
                     Ovitrampa ID: 166.0<br>Nº de ovos: 71
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d9a8b540b8934f6ad0e1a885dedd62fb = L.circleMarker(
                [-22.50534592, -55.73772283],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d9a8b540b8934f6ad0e1a885dedd62fb.bindTooltip(
                `<div>
                     Ovitrampa ID: 167.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a248e85d2c452e9dffafb16cbd14522f = L.circleMarker(
                [-22.50514894, -55.74050527],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a248e85d2c452e9dffafb16cbd14522f.bindTooltip(
                `<div>
                     Ovitrampa ID: 168.0<br>Nº de ovos: 58
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_fef31a12b930c97e0c27eb851c1ce4f2 = L.circleMarker(
                [-22.50701371, -55.74597973],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_fef31a12b930c97e0c27eb851c1ce4f2.bindTooltip(
                `<div>
                     Ovitrampa ID: 169.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ab9b7cb5b0674d2204aedd374f1f7dea = L.circleMarker(
                [-22.57063149, -55.67978817],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ab9b7cb5b0674d2204aedd374f1f7dea.bindTooltip(
                `<div>
                     Ovitrampa ID: 17.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_55557ffdad702288cffa810dece43fe4 = L.circleMarker(
                [-22.50146106, -55.74452021],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_55557ffdad702288cffa810dece43fe4.bindTooltip(
                `<div>
                     Ovitrampa ID: 170.0<br>Nº de ovos: 23
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f568140dedf3f44408479ecee754b95f = L.circleMarker(
                [-22.50139, -55.74182],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f568140dedf3f44408479ecee754b95f.bindTooltip(
                `<div>
                     Ovitrampa ID: 171.0<br>Nº de ovos: 7
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e50408911b2ded9b71f226ba7eb09c6f = L.circleMarker(
                [-22.5031051, -55.7374472],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e50408911b2ded9b71f226ba7eb09c6f.bindTooltip(
                `<div>
                     Ovitrampa ID: 172.0<br>Nº de ovos: 104
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8362d700a363bdb212f2dc6fa5a19874 = L.circleMarker(
                [-22.5028065, -55.7343831],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8362d700a363bdb212f2dc6fa5a19874.bindTooltip(
                `<div>
                     Ovitrampa ID: 173.0<br>Nº de ovos: 73
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b84d50977f131acba95908c2f35b4469 = L.circleMarker(
                [-22.5022768, -55.7299891],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b84d50977f131acba95908c2f35b4469.bindTooltip(
                `<div>
                     Ovitrampa ID: 174.0<br>Nº de ovos: 96
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_885b13a178a4d1f5fad9ab14e7c3bae1 = L.circleMarker(
                [-22.5031554, -55.7251693],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_885b13a178a4d1f5fad9ab14e7c3bae1.bindTooltip(
                `<div>
                     Ovitrampa ID: 175.0<br>Nº de ovos: 64
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_93e7e7093622cf2a2ff68ebece20034b = L.circleMarker(
                [-22.5027842, -55.7227262],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_93e7e7093622cf2a2ff68ebece20034b.bindTooltip(
                `<div>
                     Ovitrampa ID: 176.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_40f1b8c79d0b6d9b2292642521469238 = L.circleMarker(
                [-22.5026854, -55.7188097],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_40f1b8c79d0b6d9b2292642521469238.bindTooltip(
                `<div>
                     Ovitrampa ID: 177.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_00a12868f1234cc0dc38fc47b229fd77 = L.circleMarker(
                [-22.5024656, -55.714133],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_00a12868f1234cc0dc38fc47b229fd77.bindTooltip(
                `<div>
                     Ovitrampa ID: 178.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a6c98979f49f3932229be01a9a581f7c = L.circleMarker(
                [-22.5025676, -55.7108878],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a6c98979f49f3932229be01a9a581f7c.bindTooltip(
                `<div>
                     Ovitrampa ID: 179.0<br>Nº de ovos: 75
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7a3b28a7f726ecd9ac3dfc7185df1a1e = L.circleMarker(
                [-22.5682846, -55.68028402],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7a3b28a7f726ecd9ac3dfc7185df1a1e.bindTooltip(
                `<div>
                     Ovitrampa ID: 18.0<br>Nº de ovos: 6
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1fa175c238be74505b359dafabc46c6d = L.circleMarker(
                [-22.50032085, -55.7061126],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1fa175c238be74505b359dafabc46c6d.bindTooltip(
                `<div>
                     Ovitrampa ID: 180.0<br>Nº de ovos: 126
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8b05c89f456607b26244aa08a470c1dd = L.circleMarker(
                [-22.50231468, -55.70325266],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8b05c89f456607b26244aa08a470c1dd.bindTooltip(
                `<div>
                     Ovitrampa ID: 181.0<br>Nº de ovos: 10
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c107360b5394a777adb849aa4e051061 = L.circleMarker(
                [-22.50017222, -55.7112595],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c107360b5394a777adb849aa4e051061.bindTooltip(
                `<div>
                     Ovitrampa ID: 182.0<br>Nº de ovos: 62
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2bfd96092b4a71d782224e8a17a612b2 = L.circleMarker(
                [-22.50053678, -55.71331495],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2bfd96092b4a71d782224e8a17a612b2.bindTooltip(
                `<div>
                     Ovitrampa ID: 183.0<br>Nº de ovos: 520
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_33b653fc21d863097781d24bced4eb41 = L.circleMarker(
                [-22.50001124, -55.71985932],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_33b653fc21d863097781d24bced4eb41.bindTooltip(
                `<div>
                     Ovitrampa ID: 184.0<br>Nº de ovos: 171
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f349d9f5398783b7474f01dab11438d2 = L.circleMarker(
                [-22.49946231, -55.72355661],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f349d9f5398783b7474f01dab11438d2.bindTooltip(
                `<div>
                     Ovitrampa ID: 185.0<br>Nº de ovos: 201
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_84c02c9b7812c61a7484f1dbf12c1463 = L.circleMarker(
                [-22.49819668, -55.72689149],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_84c02c9b7812c61a7484f1dbf12c1463.bindTooltip(
                `<div>
                     Ovitrampa ID: 186.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_53e3d3525b118273d93f17fd6892b99a = L.circleMarker(
                [-22.49870783, -55.72983113],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_53e3d3525b118273d93f17fd6892b99a.bindTooltip(
                `<div>
                     Ovitrampa ID: 187.0<br>Nº de ovos: 87
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1adbbb930b65fb5df1181dec197eff16 = L.circleMarker(
                [-22.49783745, -55.73461993],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1adbbb930b65fb5df1181dec197eff16.bindTooltip(
                `<div>
                     Ovitrampa ID: 188.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_eb5b7ff9513c72d12f58bbed638aa341 = L.circleMarker(
                [-22.4979825, -55.73792295],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_eb5b7ff9513c72d12f58bbed638aa341.bindTooltip(
                `<div>
                     Ovitrampa ID: 189.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6f329c5d702620a5d9d853a82e70e072 = L.circleMarker(
                [-22.56724, -55.68382],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6f329c5d702620a5d9d853a82e70e072.bindTooltip(
                `<div>
                     Ovitrampa ID: 19.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_23b7ef67314bfb4eea66c37ca12f00d2 = L.circleMarker(
                [-22.4986098, -55.74304352],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_23b7ef67314bfb4eea66c37ca12f00d2.bindTooltip(
                `<div>
                     Ovitrampa ID: 190.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c36eb7a62bb8415365023549f3a2770c = L.circleMarker(
                [-22.4988367, -55.74515834],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c36eb7a62bb8415365023549f3a2770c.bindTooltip(
                `<div>
                     Ovitrampa ID: 191.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_29dec7ce72f074b9c8e845adf63ce170 = L.circleMarker(
                [-22.49617872, -55.74713457],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_29dec7ce72f074b9c8e845adf63ce170.bindTooltip(
                `<div>
                     Ovitrampa ID: 192.0<br>Nº de ovos: 88
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a4706ee5c6b825da6662353405e4bfb0 = L.circleMarker(
                [-22.49628778, -55.73990185],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a4706ee5c6b825da6662353405e4bfb0.bindTooltip(
                `<div>
                     Ovitrampa ID: 193.0<br>Nº de ovos: 53
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4d39a23bd1242b85904d96a7c409e255 = L.circleMarker(
                [-22.49632113, -55.73878276],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4d39a23bd1242b85904d96a7c409e255.bindTooltip(
                `<div>
                     Ovitrampa ID: 194.0<br>Nº de ovos: 228
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4cb7261622c2140548150e1cf05e3c4f = L.circleMarker(
                [-22.49666023, -55.73391721],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4cb7261622c2140548150e1cf05e3c4f.bindTooltip(
                `<div>
                     Ovitrampa ID: 195.0<br>Nº de ovos: 53
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a8a0da2f2cc0143476fee4ec0932af84 = L.circleMarker(
                [-22.4970815, -55.72979311],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a8a0da2f2cc0143476fee4ec0932af84.bindTooltip(
                `<div>
                     Ovitrampa ID: 196.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1534da1d56d0237617e1ebfcb421b714 = L.circleMarker(
                [-22.49650967, -55.7263839],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1534da1d56d0237617e1ebfcb421b714.bindTooltip(
                `<div>
                     Ovitrampa ID: 197.0<br>Nº de ovos: 62
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e42827be447ac5eb9a2ba151e077a50a = L.circleMarker(
                [-22.4936467, -55.7226377],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e42827be447ac5eb9a2ba151e077a50a.bindTooltip(
                `<div>
                     Ovitrampa ID: 198.0<br>Nº de ovos: 25
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6efb21796720546c70b180af69370369 = L.circleMarker(
                [-22.49116257, -55.7215439],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6efb21796720546c70b180af69370369.bindTooltip(
                `<div>
                     Ovitrampa ID: 199.0<br>Nº de ovos: 162
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_27494f831a695eb839c6eba0d2188a55 = L.circleMarker(
                [-22.5779, -55.6764],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_27494f831a695eb839c6eba0d2188a55.bindTooltip(
                `<div>
                     Ovitrampa ID: 2.0<br>Nº de ovos: 430
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1367260766c5583a73afb3e13c279e72 = L.circleMarker(
                [-22.56656, -55.68697],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1367260766c5583a73afb3e13c279e72.bindTooltip(
                `<div>
                     Ovitrampa ID: 20.0<br>Nº de ovos: 138
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_441c003432f24b1b4781bacb57d8ae30 = L.circleMarker(
                [-22.4902874, -55.7200612],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_441c003432f24b1b4781bacb57d8ae30.bindTooltip(
                `<div>
                     Ovitrampa ID: 200.0<br>Nº de ovos: 34
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_919354cee05a20bd0d3d9637e8c29694 = L.circleMarker(
                [-22.48802846, -55.71931609],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_919354cee05a20bd0d3d9637e8c29694.bindTooltip(
                `<div>
                     Ovitrampa ID: 201.0<br>Nº de ovos: 206
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_72c64760c73296c49a29d40a7b8b2565 = L.circleMarker(
                [-22.48801109, -55.72404936],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_72c64760c73296c49a29d40a7b8b2565.bindTooltip(
                `<div>
                     Ovitrampa ID: 202.0<br>Nº de ovos: 115
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4337e62fc96278f19fb43c8a807de4f6 = L.circleMarker(
                [-22.48766553, -55.72511016],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4337e62fc96278f19fb43c8a807de4f6.bindTooltip(
                `<div>
                     Ovitrampa ID: 203.0<br>Nº de ovos: 112
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8910c5ab4609dc85c31e6d190be00c6a = L.circleMarker(
                [-22.4873515, -55.7298789],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8910c5ab4609dc85c31e6d190be00c6a.bindTooltip(
                `<div>
                     Ovitrampa ID: 204.0<br>Nº de ovos: 33
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_bbec8ddb22d27bf0241efbe7974f4500 = L.circleMarker(
                [-22.48818079, -55.73509419],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_bbec8ddb22d27bf0241efbe7974f4500.bindTooltip(
                `<div>
                     Ovitrampa ID: 205.0<br>Nº de ovos: 16
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_5d43d7f7dc72cc7a97a872b42b07c303 = L.circleMarker(
                [-22.48871469, -55.73913911],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_5d43d7f7dc72cc7a97a872b42b07c303.bindTooltip(
                `<div>
                     Ovitrampa ID: 206.0<br>Nº de ovos: 161
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4d0e660562d14ee39f303ad602646abf = L.circleMarker(
                [-22.49020821, -55.73962428],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4d0e660562d14ee39f303ad602646abf.bindTooltip(
                `<div>
                     Ovitrampa ID: 207.0<br>Nº de ovos: 63
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f621f4309b9fc9ece61dd92e7d027d65 = L.circleMarker(
                [-22.49098529, -55.74134939],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f621f4309b9fc9ece61dd92e7d027d65.bindTooltip(
                `<div>
                     Ovitrampa ID: 208.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c70e2170b1515e27f4bc46f432cf2ea1 = L.circleMarker(
                [-22.49150077, -55.74378623],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c70e2170b1515e27f4bc46f432cf2ea1.bindTooltip(
                `<div>
                     Ovitrampa ID: 209.0<br>Nº de ovos: 64
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_74bb7bd15ec6c8f9176db546aa314c7f = L.circleMarker(
                [-22.566694, -55.6913],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_74bb7bd15ec6c8f9176db546aa314c7f.bindTooltip(
                `<div>
                     Ovitrampa ID: 21.0<br>Nº de ovos: 117
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_43ee08e567dcfd3ab190f92db1298b16 = L.circleMarker(
                [-22.48803216, -55.74071125],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_43ee08e567dcfd3ab190f92db1298b16.bindTooltip(
                `<div>
                     Ovitrampa ID: 210.0<br>Nº de ovos: 246
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_47dc97c36064d2a0b9bb6412cd1e6cac = L.circleMarker(
                [-22.48732976, -55.74644901],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_47dc97c36064d2a0b9bb6412cd1e6cac.bindTooltip(
                `<div>
                     Ovitrampa ID: 211.0<br>Nº de ovos: 189
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8aa1c57052dcae442ef8b1432e6e0285 = L.circleMarker(
                [-22.48434491, -55.74671995],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8aa1c57052dcae442ef8b1432e6e0285.bindTooltip(
                `<div>
                     Ovitrampa ID: 212.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_cbf03229e5546ccab4072cf8d0479e95 = L.circleMarker(
                [-22.48470312, -55.74143382],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_cbf03229e5546ccab4072cf8d0479e95.bindTooltip(
                `<div>
                     Ovitrampa ID: 213.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_83dd314d0c790aac1e2259ab61084113 = L.circleMarker(
                [-22.48431027, -55.73752904],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_83dd314d0c790aac1e2259ab61084113.bindTooltip(
                `<div>
                     Ovitrampa ID: 214.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6ec40b67f224d0f5e6d0ba748274326a = L.circleMarker(
                [-22.48438909, -55.73413104],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6ec40b67f224d0f5e6d0ba748274326a.bindTooltip(
                `<div>
                     Ovitrampa ID: 215.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e0fb2816b32376f8acc182eaf1c9cdef = L.circleMarker(
                [-22.48431098, -55.72997452],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e0fb2816b32376f8acc182eaf1c9cdef.bindTooltip(
                `<div>
                     Ovitrampa ID: 216.0<br>Nº de ovos: 38
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a6344a264b32f59daf0c7111007e5dd9 = L.circleMarker(
                [-22.48395125, -55.72652514],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a6344a264b32f59daf0c7111007e5dd9.bindTooltip(
                `<div>
                     Ovitrampa ID: 217.0<br>Nº de ovos: 67
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_fa3cdda4a4efc07ec843ae4b986ccccf = L.circleMarker(
                [-22.48369608, -55.72214773],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_fa3cdda4a4efc07ec843ae4b986ccccf.bindTooltip(
                `<div>
                     Ovitrampa ID: 218.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_5b97ea1854c574630c0901bccde5e57f = L.circleMarker(
                [-22.48467409, -55.71951625],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_5b97ea1854c574630c0901bccde5e57f.bindTooltip(
                `<div>
                     Ovitrampa ID: 219.0<br>Nº de ovos: 28
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_cd59066ec54a37fe817a984b355ca3b9 = L.circleMarker(
                [-22.5672, -55.69403],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_cd59066ec54a37fe817a984b355ca3b9.bindTooltip(
                `<div>
                     Ovitrampa ID: 22.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_333bb87559963b86600c233b884e38ad = L.circleMarker(
                [-22.48289608, -55.72487163],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_333bb87559963b86600c233b884e38ad.bindTooltip(
                `<div>
                     Ovitrampa ID: 220.0<br>Nº de ovos: 174
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_6b25d90f0d27423868689dd40f6bf7a4 = L.circleMarker(
                [-22.48314383, -55.72929089],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_6b25d90f0d27423868689dd40f6bf7a4.bindTooltip(
                `<div>
                     Ovitrampa ID: 221.0<br>Nº de ovos: 72
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3efc29fac2e6a7533a4fe84943637692 = L.circleMarker(
                [-22.48212634, -55.73429815],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3efc29fac2e6a7533a4fe84943637692.bindTooltip(
                `<div>
                     Ovitrampa ID: 222.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_be707995ccd614bf88bc9f8e2e46ce99 = L.circleMarker(
                [-22.4823279, -55.7372452],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_be707995ccd614bf88bc9f8e2e46ce99.bindTooltip(
                `<div>
                     Ovitrampa ID: 223.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b66a07c3252a52ed6b81b05552cea8b9 = L.circleMarker(
                [-22.47707396, -55.74909308],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b66a07c3252a52ed6b81b05552cea8b9.bindTooltip(
                `<div>
                     Ovitrampa ID: 224.0<br>Nº de ovos: 8
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7080981c81a33aaafe55c29272d365ce = L.circleMarker(
                [-22.562942, -55.6969912],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7080981c81a33aaafe55c29272d365ce.bindTooltip(
                `<div>
                     Ovitrampa ID: 23.0<br>Nº de ovos: 33
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_5304f15cfd7f11855c7b7282e7c45300 = L.circleMarker(
                [-22.5634, -55.69371],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_5304f15cfd7f11855c7b7282e7c45300.bindTooltip(
                `<div>
                     Ovitrampa ID: 24.0<br>Nº de ovos: 179
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_0246a2e3d167f294c13860dce5aba1c1 = L.circleMarker(
                [-22.5640244, -55.6904818],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_0246a2e3d167f294c13860dce5aba1c1.bindTooltip(
                `<div>
                     Ovitrampa ID: 25.0<br>Nº de ovos: 78
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9dcbcae3230912d6d5c7215f0c5d156f = L.circleMarker(
                [-22.5641021, -55.6874434],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9dcbcae3230912d6d5c7215f0c5d156f.bindTooltip(
                `<div>
                     Ovitrampa ID: 26.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_53c15afb9a3e23b9f1b6573ea8c00ad4 = L.circleMarker(
                [-22.56442967, -55.68365741],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_53c15afb9a3e23b9f1b6573ea8c00ad4.bindTooltip(
                `<div>
                     Ovitrampa ID: 27.0<br>Nº de ovos: 64
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_aab6644398133582696d0251bd891f83 = L.circleMarker(
                [-22.5648934, -55.6810013],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_aab6644398133582696d0251bd891f83.bindTooltip(
                `<div>
                     Ovitrampa ID: 28.0<br>Nº de ovos: 81
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3f86c438db8fe146ac2074fa76f5af4f = L.circleMarker(
                [-22.56053231, -55.68016491],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3f86c438db8fe146ac2074fa76f5af4f.bindTooltip(
                `<div>
                     Ovitrampa ID: 29.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f2e14935710ff3ff5ad0a7522e973ab4 = L.circleMarker(
                [-22.577616, -55.679396],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f2e14935710ff3ff5ad0a7522e973ab4.bindTooltip(
                `<div>
                     Ovitrampa ID: 3.0<br>Nº de ovos: 390
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8107f8eb45b38ed2bfb8c802122bc21e = L.circleMarker(
                [-22.56009637, -55.68385563],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8107f8eb45b38ed2bfb8c802122bc21e.bindTooltip(
                `<div>
                     Ovitrampa ID: 30.0<br>Nº de ovos: 88
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b66f9a983ce5d7a4206564c6c1b4a3c0 = L.circleMarker(
                [-22.56079166, -55.68720333],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b66f9a983ce5d7a4206564c6c1b4a3c0.bindTooltip(
                `<div>
                     Ovitrampa ID: 31.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a50717dedf778f8223166aaa5cb40bdf = L.circleMarker(
                [-22.56045641, -55.69067182],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a50717dedf778f8223166aaa5cb40bdf.bindTooltip(
                `<div>
                     Ovitrampa ID: 32.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1fd9746e68fd20bc3451ff60064278ac = L.circleMarker(
                [-22.55937153, -55.6949],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1fd9746e68fd20bc3451ff60064278ac.bindTooltip(
                `<div>
                     Ovitrampa ID: 33.0<br>Nº de ovos: 62
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_080d45cfc2833d7a6e751a294969d675 = L.circleMarker(
                [-22.56009279, -55.69914141],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_080d45cfc2833d7a6e751a294969d675.bindTooltip(
                `<div>
                     Ovitrampa ID: 34.0<br>Nº de ovos: 6
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_746ab6ac644192e93ae03ed394f93141 = L.circleMarker(
                [-22.55979556, -55.70320148],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_746ab6ac644192e93ae03ed394f93141.bindTooltip(
                `<div>
                     Ovitrampa ID: 35.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_18589d1c10fcfb811f4120fc1ae574e7 = L.circleMarker(
                [-22.556385, -55.70201166],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_18589d1c10fcfb811f4120fc1ae574e7.bindTooltip(
                `<div>
                     Ovitrampa ID: 36.0<br>Nº de ovos: 27
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c6a60e29cec36856b3de36e21e47d9a9 = L.circleMarker(
                [-22.55726744, -55.69791178],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c6a60e29cec36856b3de36e21e47d9a9.bindTooltip(
                `<div>
                     Ovitrampa ID: 37.0<br>Nº de ovos: 78
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_63cf53dd44b92924490f339a756b300c = L.circleMarker(
                [-22.55638099, -55.69586885],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_63cf53dd44b92924490f339a756b300c.bindTooltip(
                `<div>
                     Ovitrampa ID: 38.0<br>Nº de ovos: 5
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e08a31df1db70466556101509c1e4c6e = L.circleMarker(
                [-22.55773225, -55.68933692],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e08a31df1db70466556101509c1e4c6e.bindTooltip(
                `<div>
                     Ovitrampa ID: 39.0<br>Nº de ovos: 68
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_53dc790a5002a9ca60ba41431547c7ad = L.circleMarker(
                [-22.58104476, -55.67673754],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_53dc790a5002a9ca60ba41431547c7ad.bindTooltip(
                `<div>
                     Ovitrampa ID: 4.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7fa3f068e9ac2c9e6bdfb6bde93bfe39 = L.circleMarker(
                [-22.5571292, -55.68760542],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7fa3f068e9ac2c9e6bdfb6bde93bfe39.bindTooltip(
                `<div>
                     Ovitrampa ID: 40.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d736b7ccf4d2297f03b415e8ae9fe53c = L.circleMarker(
                [-22.55862573, -55.68488637],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d736b7ccf4d2297f03b415e8ae9fe53c.bindTooltip(
                `<div>
                     Ovitrampa ID: 41.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8592119c622429c24488425853110ba1 = L.circleMarker(
                [-22.55755915, -55.68152588],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8592119c622429c24488425853110ba1.bindTooltip(
                `<div>
                     Ovitrampa ID: 42.0<br>Nº de ovos: 178
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_07e1debdf40af69103fcb4216fd1bac5 = L.circleMarker(
                [-22.5548586, -55.68896148],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_07e1debdf40af69103fcb4216fd1bac5.bindTooltip(
                `<div>
                     Ovitrampa ID: 43.0<br>Nº de ovos: 115
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e7fa1f4d8d3c913ac07b4892fab6053e = L.circleMarker(
                [-22.55391505, -55.69039213],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e7fa1f4d8d3c913ac07b4892fab6053e.bindTooltip(
                `<div>
                     Ovitrampa ID: 44.0<br>Nº de ovos: 60
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9e319519be1450493e7b596199fcbb9e = L.circleMarker(
                [-22.5548915, -55.6957812],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9e319519be1450493e7b596199fcbb9e.bindTooltip(
                `<div>
                     Ovitrampa ID: 45.0<br>Nº de ovos: 110
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_534c39ceed317b069f0e7b7c431fbf11 = L.circleMarker(
                [-22.55286999, -55.69942617],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_534c39ceed317b069f0e7b7c431fbf11.bindTooltip(
                `<div>
                     Ovitrampa ID: 46.0<br>Nº de ovos: 71
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c39ed73eddf025bfeb64a44baafe212a = L.circleMarker(
                [-22.55357348, -55.70128226],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c39ed73eddf025bfeb64a44baafe212a.bindTooltip(
                `<div>
                     Ovitrampa ID: 47.0<br>Nº de ovos: 22
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_66fabcef7a77f380e3bec420a6b9621c = L.circleMarker(
                [-22.55065504, -55.70117672],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_66fabcef7a77f380e3bec420a6b9621c.bindTooltip(
                `<div>
                     Ovitrampa ID: 48.0<br>Nº de ovos: 29
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d404eea436893c817a4c76f1cf2cfe63 = L.circleMarker(
                [-22.549574, -55.69930225],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d404eea436893c817a4c76f1cf2cfe63.bindTooltip(
                `<div>
                     Ovitrampa ID: 49.0<br>Nº de ovos: 9
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d573ff2bb1f5c296f220eb45941ea415 = L.circleMarker(
                [-22.58085813, -55.67906827],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d573ff2bb1f5c296f220eb45941ea415.bindTooltip(
                `<div>
                     Ovitrampa ID: 5.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7e1371107627cf7460122022db33b21d = L.circleMarker(
                [-22.5486603, -55.69458274],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7e1371107627cf7460122022db33b21d.bindTooltip(
                `<div>
                     Ovitrampa ID: 50.0<br>Nº de ovos: 29
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a2f209ef77dd0403b6d4af5b2c589598 = L.circleMarker(
                [-22.54833158, -55.69155276],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a2f209ef77dd0403b6d4af5b2c589598.bindTooltip(
                `<div>
                     Ovitrampa ID: 51.0<br>Nº de ovos: 95
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_fb93e0c6a689634fd50cb12d9a115394 = L.circleMarker(
                [-22.54611011, -55.69863444],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_fb93e0c6a689634fd50cb12d9a115394.bindTooltip(
                `<div>
                     Ovitrampa ID: 52.0<br>Nº de ovos: 64
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b1e436c83dc9b732fdda2b0c4ef3b86f = L.circleMarker(
                [-22.54608832, -55.69531537],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b1e436c83dc9b732fdda2b0c4ef3b86f.bindTooltip(
                `<div>
                     Ovitrampa ID: 53.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_cf5628adf51d65a881246ed27c323a21 = L.circleMarker(
                [-22.54556159, -55.6908646],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_cf5628adf51d65a881246ed27c323a21.bindTooltip(
                `<div>
                     Ovitrampa ID: 54.0<br>Nº de ovos: 18
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8b80db75966ec0335ffb488702aa6452 = L.circleMarker(
                [-22.544984, -55.687216],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8b80db75966ec0335ffb488702aa6452.bindTooltip(
                `<div>
                     Ovitrampa ID: 55.0<br>Nº de ovos: 10
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_007309088624bb6d2ed0602ee5bed8a2 = L.circleMarker(
                [-22.542453, -55.686857],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_007309088624bb6d2ed0602ee5bed8a2.bindTooltip(
                `<div>
                     Ovitrampa ID: 56.0<br>Nº de ovos: 71
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_501426ea9936625a7789883529be6ef6 = L.circleMarker(
                [-22.53912, -55.687667],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_501426ea9936625a7789883529be6ef6.bindTooltip(
                `<div>
                     Ovitrampa ID: 57.0<br>Nº de ovos: 35
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_58511ab288a645d50e5fe81db2b8604a = L.circleMarker(
                [-22.53966321, -55.69000849],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_58511ab288a645d50e5fe81db2b8604a.bindTooltip(
                `<div>
                     Ovitrampa ID: 58.0<br>Nº de ovos: 120
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3ffcc2cf0e3f6b7e3779c0c9b15e1578 = L.circleMarker(
                [-22.5408563, -55.69035025],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3ffcc2cf0e3f6b7e3779c0c9b15e1578.bindTooltip(
                `<div>
                     Ovitrampa ID: 59.0<br>Nº de ovos: 97
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8eb5c71c889d64cd67d469689fffa3c6 = L.circleMarker(
                [-22.57986535, -55.68208349],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8eb5c71c889d64cd67d469689fffa3c6.bindTooltip(
                `<div>
                     Ovitrampa ID: 6.0<br>Nº de ovos: 84
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4ba1d49fbd622bad862f0d08ab9b0a23 = L.circleMarker(
                [-22.541706, -55.702726],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4ba1d49fbd622bad862f0d08ab9b0a23.bindTooltip(
                `<div>
                     Ovitrampa ID: 60.0<br>Nº de ovos: 1
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_96c9b6aea72f716cb68d8c6e43b372cb = L.circleMarker(
                [-22.54275098, -55.70680137],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_96c9b6aea72f716cb68d8c6e43b372cb.bindTooltip(
                `<div>
                     Ovitrampa ID: 61.0<br>Nº de ovos: 58
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7b87c7261753a91de7908aaefdbd17f6 = L.circleMarker(
                [-22.54567056, -55.70727567],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7b87c7261753a91de7908aaefdbd17f6.bindTooltip(
                `<div>
                     Ovitrampa ID: 62.0<br>Nº de ovos: 51
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b6aa15792dd27436d3310b37ad3f4df2 = L.circleMarker(
                [-22.54544707, -55.70352569],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b6aa15792dd27436d3310b37ad3f4df2.bindTooltip(
                `<div>
                     Ovitrampa ID: 63.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_078145760e2272635ed367215eab0748 = L.circleMarker(
                [-22.54774357, -55.70468267],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_078145760e2272635ed367215eab0748.bindTooltip(
                `<div>
                     Ovitrampa ID: 64.0<br>Nº de ovos: 76
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_745c69c822956b5aafea0210ce2fa2e9 = L.circleMarker(
                [-22.54947595, -55.70797873],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_745c69c822956b5aafea0210ce2fa2e9.bindTooltip(
                `<div>
                     Ovitrampa ID: 65.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a1a80c1fb5774084dcb41a3961189c22 = L.circleMarker(
                [-22.55039674, -55.70920915],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a1a80c1fb5774084dcb41a3961189c22.bindTooltip(
                `<div>
                     Ovitrampa ID: 66.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e7ce58056ffceeae9eac403851aebe6b = L.circleMarker(
                [-22.5517427, -55.70782915],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e7ce58056ffceeae9eac403851aebe6b.bindTooltip(
                `<div>
                     Ovitrampa ID: 67.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7bcbf7bb6c56af73c4e9e5ec711107e8 = L.circleMarker(
                [-22.55605024, -55.70756005],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7bcbf7bb6c56af73c4e9e5ec711107e8.bindTooltip(
                `<div>
                     Ovitrampa ID: 68.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e58d51ab0bd0b8eeb9fd51d2113750ca = L.circleMarker(
                [-22.55660728, -55.71097685],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e58d51ab0bd0b8eeb9fd51d2113750ca.bindTooltip(
                `<div>
                     Ovitrampa ID: 69.0<br>Nº de ovos: 38
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f6e0d4977766d196e8f9fbc9d5f1f9e2 = L.circleMarker(
                [-22.5818827, -55.6831812],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f6e0d4977766d196e8f9fbc9d5f1f9e2.bindTooltip(
                `<div>
                     Ovitrampa ID: 7.0<br>Nº de ovos: 146
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_a7c59f0d5521a68d6e7bd8579164a05b = L.circleMarker(
                [-22.55573954, -55.71435028],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_a7c59f0d5521a68d6e7bd8579164a05b.bindTooltip(
                `<div>
                     Ovitrampa ID: 70.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ac7ddad52dedbf2fbdfa617085763869 = L.circleMarker(
                [-22.55295413, -55.71023103],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ac7ddad52dedbf2fbdfa617085763869.bindTooltip(
                `<div>
                     Ovitrampa ID: 71.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e6b67985460725e97867d9850669d9d9 = L.circleMarker(
                [-22.55311267, -55.71441528],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e6b67985460725e97867d9850669d9d9.bindTooltip(
                `<div>
                     Ovitrampa ID: 72.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_8cde21a7a548e8893e0198f14d0c8558 = L.circleMarker(
                [-22.55334074, -55.71837031],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_8cde21a7a548e8893e0198f14d0c8558.bindTooltip(
                `<div>
                     Ovitrampa ID: 73.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2813614e8ed8da693b08c172af57b531 = L.circleMarker(
                [-22.55199534, -55.72196827],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2813614e8ed8da693b08c172af57b531.bindTooltip(
                `<div>
                     Ovitrampa ID: 74.0<br>Nº de ovos: 144
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_f28b8750e4598fd5c04f9566837743e1 = L.circleMarker(
                [-22.54962682, -55.7193726],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_f28b8750e4598fd5c04f9566837743e1.bindTooltip(
                `<div>
                     Ovitrampa ID: 75.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_87f8b2eec572d292054db9000c430046 = L.circleMarker(
                [-22.54909175, -55.72229084],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_87f8b2eec572d292054db9000c430046.bindTooltip(
                `<div>
                     Ovitrampa ID: 76.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d471351052e75cb47f4ec2364e727a8a = L.circleMarker(
                [-22.54831054, -55.7247322],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d471351052e75cb47f4ec2364e727a8a.bindTooltip(
                `<div>
                     Ovitrampa ID: 77.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d97ea68710293decfe87e7945910b2d5 = L.circleMarker(
                [-22.54567651, -55.72658292],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d97ea68710293decfe87e7945910b2d5.bindTooltip(
                `<div>
                     Ovitrampa ID: 78.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9e1fc197b4c370370bb6e365f38dbb47 = L.circleMarker(
                [-22.54564195, -55.72230274],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9e1fc197b4c370370bb6e365f38dbb47.bindTooltip(
                `<div>
                     Ovitrampa ID: 79.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_96a2219a7c3d62775462c499b1de86f8 = L.circleMarker(
                [-22.5807243, -55.6872979],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_96a2219a7c3d62775462c499b1de86f8.bindTooltip(
                `<div>
                     Ovitrampa ID: 8.0<br>Nº de ovos: 24
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b6a6e00ddee79f1fbfd589979b9220b9 = L.circleMarker(
                [-22.54249538, -55.72337506],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b6a6e00ddee79f1fbfd589979b9220b9.bindTooltip(
                `<div>
                     Ovitrampa ID: 80.0<br>Nº de ovos: 102
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_4e316e45ad65b165b48b8a9b30bb821b = L.circleMarker(
                [-22.54217829, -55.72620747],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_4e316e45ad65b165b48b8a9b30bb821b.bindTooltip(
                `<div>
                     Ovitrampa ID: 81.0<br>Nº de ovos: 21
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_65763fe8ed91790390de96b3db6f6692 = L.circleMarker(
                [-22.54125839, -55.72820898],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_65763fe8ed91790390de96b3db6f6692.bindTooltip(
                `<div>
                     Ovitrampa ID: 82.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_90b09104734d52629bb69df15c4980dc = L.circleMarker(
                [-22.53820736, -55.72967611],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_90b09104734d52629bb69df15c4980dc.bindTooltip(
                `<div>
                     Ovitrampa ID: 83.0<br>Nº de ovos: 72
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_1cf16f3b822d823905a4dae4f6d053f6 = L.circleMarker(
                [-22.53743065, -55.72608181],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_1cf16f3b822d823905a4dae4f6d053f6.bindTooltip(
                `<div>
                     Ovitrampa ID: 84.0<br>Nº de ovos: 2
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_08ec1fc4cb7e056b09c3ddeb586fd1f9 = L.circleMarker(
                [-22.53795928, -55.72274902],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_08ec1fc4cb7e056b09c3ddeb586fd1f9.bindTooltip(
                `<div>
                     Ovitrampa ID: 85.0<br>Nº de ovos: 37
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_df3214f3b1b2285f062897c82ef7e1f3 = L.circleMarker(
                [-22.53737405, -55.71968077],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_df3214f3b1b2285f062897c82ef7e1f3.bindTooltip(
                `<div>
                     Ovitrampa ID: 86.0<br>Nº de ovos: 34
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_2fbc47317dd51ad2129940266ff3baf7 = L.circleMarker(
                [-22.53440856, -55.71515989],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_2fbc47317dd51ad2129940266ff3baf7.bindTooltip(
                `<div>
                     Ovitrampa ID: 87.0<br>Nº de ovos: 244
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7d18df5ed5ce0bdb8fc2b16296336a55 = L.circleMarker(
                [-22.53492307, -55.71827699],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7d18df5ed5ce0bdb8fc2b16296336a55.bindTooltip(
                `<div>
                     Ovitrampa ID: 88.0<br>Nº de ovos: 50
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_d07d29ed4a932cef4edd6f3d6017afab = L.circleMarker(
                [-22.53515099, -55.72197843],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_d07d29ed4a932cef4edd6f3d6017afab.bindTooltip(
                `<div>
                     Ovitrampa ID: 89.0<br>Nº de ovos: 42
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_cb9da88cd18053c7da90ba6f01a97d6c = L.circleMarker(
                [-22.5777256, -55.6879824],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_cb9da88cd18053c7da90ba6f01a97d6c.bindTooltip(
                `<div>
                     Ovitrampa ID: 9.0<br>Nº de ovos: 46
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_7338bd74ee6530667960c57cda04ec3d = L.circleMarker(
                [-22.53550773, -55.72576491],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_7338bd74ee6530667960c57cda04ec3d.bindTooltip(
                `<div>
                     Ovitrampa ID: 90.0<br>Nº de ovos: 83
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_e0b6497a9efaf4268ac884656b5e2125 = L.circleMarker(
                [-22.53549782, -55.72909396],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_e0b6497a9efaf4268ac884656b5e2125.bindTooltip(
                `<div>
                     Ovitrampa ID: 91.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_9403c881b4ae58ea4671063e08e34670 = L.circleMarker(
                [-22.53485629, -55.73268543],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "yellow", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_9403c881b4ae58ea4671063e08e34670.bindTooltip(
                `<div>
                     Ovitrampa ID: 92.0<br>Nº de ovos: 82
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_520058d26f70205cfaa99916b3a8380e = L.circleMarker(
                [-22.53130475, -55.73349033],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_520058d26f70205cfaa99916b3a8380e.bindTooltip(
                `<div>
                     Ovitrampa ID: 93.0<br>Nº de ovos: 360
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_3908e218d6b5462d394ef7ced410e280 = L.circleMarker(
                [-22.53148313, -55.72986398],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_3908e218d6b5462d394ef7ced410e280.bindTooltip(
                `<div>
                     Ovitrampa ID: 94.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_65e85faaf835a59df35f320f1875ec82 = L.circleMarker(
                [-22.53128493, -55.7260016],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_65e85faaf835a59df35f320f1875ec82.bindTooltip(
                `<div>
                     Ovitrampa ID: 95.0<br>Nº de ovos: 13
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_b4f8f77e384c018d99ab6b9add254acd = L.circleMarker(
                [-22.53170396, -55.72274168],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "white", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_b4f8f77e384c018d99ab6b9add254acd.bindTooltip(
                `<div>
                     Ovitrampa ID: 96.0<br>Nº de ovos: 0
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_c9f369aa6ed2621b2254b3d1ec255130 = L.circleMarker(
                [-22.53109044, -55.71834445],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "green", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_c9f369aa6ed2621b2254b3d1ec255130.bindTooltip(
                `<div>
                     Ovitrampa ID: 97.0<br>Nº de ovos: 29
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_17577d91ec2fcf54eef435487b4b77f1 = L.circleMarker(
                [-22.53083278, -55.71497559],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_17577d91ec2fcf54eef435487b4b77f1.bindTooltip(
                `<div>
                     Ovitrampa ID: 98.0<br>Nº de ovos: 107
                 </div>`,
                {
  "sticky": true,
}
            );
        
    
            var circle_marker_ef7c1cda6b7c6a0e859247b579caf33f = L.circleMarker(
                [-22.53000035, -55.71149945],
                {"bubblingMouseEvents": true, "color": "black", "dashArray": null, "dashOffset": null, "fill": true, "fillColor": "red", "fillOpacity": 0.85, "fillRule": "evenodd", "lineCap": "round", "lineJoin": "round", "opacity": 1.0, "radius": 5, "stroke": true, "weight": 3}
            ).addTo(map_51430b7ace495f57cdc23479ea843dd9);
        
    
            circle_marker_ef7c1cda6b7c6a0e859247b579caf33f.bindTooltip(
                `<div>
                     Ovitrampa ID: 99.0<br>Nº de ovos: 129
                 </div>`,
                {
  "sticky": true,
}
            );
        
</script>
</html>
