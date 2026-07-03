<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GeoAI Platform</title>

    <link rel="stylesheet" href="style.css">

    <!-- Leaflet CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css">
</head>
<body>

<header>
    <h1>🌍 GeoAI Platform</h1>
</header>

<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script src="script.js"></script>

</body>
</html>
body{
    margin:0;
    font-family:Arial,sans-serif;
}

header{
    background:#00695c;
    color:white;
    text-align:center;
    padding:15px;
}

#map{
    width:100%;
    height:90vh;
} 
var map = L.map('map').setView([34.0151, 71.5249], 12);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{
    attribution:'© OpenStreetMap'
}).addTo(map);

L.marker([34.0151,71.5249]).addTo(map)
.bindPopup("Welcome to GeoAI Platform")
.openPopup();
