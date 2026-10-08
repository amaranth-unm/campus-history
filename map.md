---
layout: essay
title: UNM Campus History Essay Map
---

<!-- Leaflet CSS/JS and Omnivore for KML support -->
<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script src="https://unpkg.com/leaflet-omnivore@0.3.4/leaflet-omnivore.min.js"></script>

<script src="https://unpkg.com/leaflet-responsive-popup@0.2.0/leaflet.responsive.popup.js"></script>
<link rel="stylesheet" href="https://unpkg.com/leaflet-responsive-popup@0.2.0/leaflet.responsive.popup.css" />

<style>
  /* Gray the street map so the blue building outlines stand out */
  #map .leaflet-tile-pane { filter: grayscale(1) contrast(0.85) brightness(1.08); }

  /* A fixed photo height keeps popups short enough to fit on the map, and
     lets the map pan to fit one before its photo has loaded. At full size
     a photo made the popup 600px tall, and it opened off the top. */
  #map .popup-img { display: block; width: 100%; height: 180px; object-fit: cover; }
</style>


<!-- close the container div for full width map -->
{::nomarkdown}
</div>
{:/nomarkdown}


<div id="map" style="height: 80vh;"></div>

<!-- Hidden data container for essays -->
<div id="map-data" style="display:none;">
  {% comment %} An essay appears on the map when assets/kml/ has an outline
     named after its folder, e.g. essays/sub/ and assets/kml/sub.kml {% endcomment %}
  {% assign kml_files = site.static_files | where_exp: "f", "f.path contains '/assets/kml/'" | map: "path" %}
  {% assign essays = site.pages | where_exp: "page", "page.path contains 'essays/'" %}
  {% for page in essays %}
  {% unless page.path contains 'starter-essay' %}
  {% assign folder = page.url | split: '/' | slice: 2, 1 | first %}
  {% assign kml_path = '/assets/kml/' | append: folder | append: '.kml' %}
  {% if kml_files contains kml_path %}
  <div class="map-point" data-name="{{ page.title | escape }}" data-popup-teaser="{{ page.popup-teaser | escape }}"
    data-kml-path="{{ site.baseurl }}/assets/kml/{{ folder }}.kml"
    data-card-image="{{ site.baseurl }}{{ page.card-image | escape }}" data-start="{{ page.start | escape }}"
    data-url="{{ site.baseurl }}{{ page.url }}" data-folder="{{ folder | downcase | replace: ' ', '-' }}">
  </div>
  {% endif %}
  {% endunless %}
  {% endfor %}
</div>


<script>
  document.addEventListener("DOMContentLoaded", function () {
    // Initialize map
    var map = L.map('map').setView([35.0844, -106.6198], 16);

    // Add OpenStreetMap tiles
    // CARTO's tiles, used until October 2026, now need an API key; without
    // one every tile shows "API KEY REQUIRED". OpenStreetMap's need none, only
    // the credit below (https://operations.osmfoundation.org/policies/tiles/).
    L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 19,
      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map);

    // Parse essay data from HTML
    var points = [];
    document.querySelectorAll('.map-point').forEach(function (el) {
      // The essay's start year, if it has one, is shown after its name
      var start = parseInt(el.dataset.start);
      points.push({
        start: isNaN(start) ? null : start,
        name: el.dataset.name,
        teaser: el.dataset.popupTeaser,
        image: el.dataset.cardImage,
        url: el.dataset.url,
        folder: el.dataset.folder,
        kmlFile: el.dataset.kmlPath
      });
    });

    // Draw each essay's outline
    points.forEach(function (pt) {
      var popupHtml = `
  <div class="popup-card">
    ${pt.image ? `<img src="${pt.image}" class="popup-img">` : ""}
    <div class="popup-text">
      <h3>${pt.name}${pt.start ? ` (${pt.start})` : ""}</h3>
      <p>${pt.teaser}</p>
      <a href="${pt.url}">Read more</a>
    </div>
  </div>
`;
      var kmlFile = pt.kmlFile;
      console.log("Loading name:", pt.image); // Add this line
      console.log("Loading KML:", kmlFile); // Add this line

      var kmlLayer = omnivore.kml(kmlFile).on('ready', function () {
        // Attach the popup to each shape in the outline
        this.eachLayer(function (layer) {
          layer.on('click', function (e) {
            // No wider than the map, so a popup fits on a phone too
            L.popup({ maxWidth: Math.min(500, map.getSize().x - 80), autoPanPadding: [16, 16] })
              .setLatLng(e.latlng)
              .setContent(popupHtml)
              .openOn(map);
          });
        });
      });
      kmlLayer.addTo(map);
    });
  });
</script>

