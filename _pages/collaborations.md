---
permalink: /collaborations/
title: "Collaborations"
author_profile: true
---

## Open to scientific collaboration

I welcome scientific collaboration with researchers, laboratories and institutions worldwide: joint research projects, co-supervision of PhD and master's students, exchange visits and joint funding applications. I am particularly interested in work that supports the **United Nations Sustainable Development Goals (SDGs)**, in particular **sustainable development**, the **integration of renewable energy** into power systems, and the **water–energy–food (WEF) nexus**.

<p><a class="btn btn--primary" href="mailto:mohammed.djehaf@univ-sba.dz?subject=Scientific%20collaboration">Contact me</a></p>

## Partner institutions

<style>
.collab-grid { display:grid; grid-template-columns:repeat(auto-fit, minmax(260px, 1fr)); gap:1em; margin:1em 0 2em; }
.collab-card { border:1px solid rgba(127,127,127,.35); border-radius:8px; padding:1em; }
.collab-card img { height:56px; max-width:100%; object-fit:contain; display:block; margin-bottom:.6em; background:#fff; padding:4px; border-radius:4px; }
.collab-card h3 { margin:.2em 0 .4em; font-size:1.05em; }
.collab-card p { font-size:.9em; margin:.3em 0; }
#collab-map { height:430px; border-radius:8px; margin:1em 0; }
</style>

<div class="collab-grid">
  <div class="collab-card">
    <img src="/images/logos/estp.png" alt="ESTP logo" onerror="this.style.display='none'">
    <h3>IRC-ESTP, Cachan (France)</h3>
    <p>Institut de recherche de la construction, team <em>Energy Transition for Construction</em> (Dr M.-H. Benzaama).</p>
    <p>Physics-informed neural networks for smart grids, battery racks and heat and mass transfer in bio-based walls. Joint article in <a href="https://doi.org/10.1016/j.applthermaleng.2026.132512"><em>Applied Thermal Engineering</em></a> (2026).</p>
  </div>
  <div class="collab-card">
    <img src="/images/logos/estaca.png" alt="ESTACA logo" onerror="this.style.display='none'">
    <h3>ESTACA'Lab (France)</h3>
    <p>S2ET team, <em>Embedded Systems and Energy for Transportation</em>.</p>
    <p>Thermal management of power-electronics modules for electric vehicles: three joint conference papers in 2026 (CoDIT, JCGE, IEEE VPPC) and co-supervision of a PhD thesis at Université Paris-Saclay.</p>
  </div>
  <div class="collab-card">
    <img src="/images/logos/uliege.png" alt="University of Liège logo" onerror="this.style.display='none'">
    <h3>University of Liège (Belgium)</h3>
    <p>Montefiore Institute, Smart Grids team of Prof. Damien Ernst.</p>
    <p>Part of my PhD work (Erasmus stay 2015–2016 and internships in 2014 and 2015) on smart electrical grids and energy systems.</p>
  </div>
  <div class="collab-card">
    <img src="/images/logos/ulille.png" alt="University of Lille logo" onerror="this.style.display='none'">
    <h3>University of Lille (France)</h3>
    <p>Unité de Mécanique de Lille (Prof. Noureddine Benseddiq).</p>
    <p>Neural-network modelling of fracture mechanics and composite patch repairs: two joint articles in 2026.</p>
  </div>
</div>

Co-authors from other institutions include Nisantasi University and Istanbul Medeniyet University (Istanbul, Turkey), the Research Center in Energy Intelligence and Innovation (CR2Ie, Québec, Canada) and the University of Engineering & Management (Kolkata, India).

## Map of collaborations

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css">
<div id="collab-map"></div>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
(function () {
  var pts = [
    [35.1899, -0.6309, "Djillali Liabès University, Sidi Bel Abbès", "Home institution", "home"],
    [48.7942, 2.3326, "IRC-ESTP, Cachan", "PINN, smart grids, bio-based walls", "partner"],
    [48.0735, -0.7667, "ESTACA'Lab, Laval", "Thermal management of power electronics", "partner"],
    [50.6326, 5.5797, "University of Liège", "Montefiore Institute, smart grids", "partner"],
    [50.6292, 3.0573, "University of Lille", "Neural networks for fracture mechanics", "partner"],
    [41.0082, 28.9784, "Nisantasi University, Istanbul", "Wind-farm control", "coauthor"],
    [41.021, 29.042, "Istanbul Medeniyet University", "Real-time validation of PV pumping", "coauthor"],
    [46.8139, -71.208, "CR2Ie, Québec", "Microgrid energy management", "coauthor"],
    [22.5726, 88.3639, "University of Engineering & Management, Kolkata", "Real-time validation of PV pumping", "coauthor"],
    [48.1351, 11.582, "Technical University of Munich", "Mobility internship, 2023", "mobility"]
  ];
  var colors = { home: "#18304c", partner: "#d1495b", coauthor: "#edae49", mobility: "#66a182" };
  var map = L.map("collab-map", { worldCopyJump: true }).setView([42, 10], 3);
  L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
    maxZoom: 12, attribution: "&copy; OpenStreetMap contributors" }).addTo(map);
  var home = pts[0];
  pts.slice(1).forEach(function (p) {
    L.polyline([[home[0], home[1]], [p[0], p[1]]], { color: colors[p[4]], weight: 1.5, opacity: 0.6, dashArray: "4 4" }).addTo(map);
  });
  var group = [];
  pts.forEach(function (p) {
    L.circleMarker([p[0], p[1]], { radius: p[4] === "home" ? 9 : 7, color: "#fff", weight: 1.5, fillColor: colors[p[4]], fillOpacity: 0.95 })
      .addTo(map).bindPopup("<strong>" + p[2] + "</strong><br>" + p[3]);
    group.push([p[0], p[1]]);
  });
  map.fitBounds(group, { padding: [30, 30] });
})();
</script>
<p style="font-size:.85em"><span style="color:#18304c">&#9679;</span> home institution &nbsp; <span style="color:#d1495b">&#9679;</span> partner institutions &nbsp; <span style="color:#edae49">&#9679;</span> co-authoring institutions &nbsp; <span style="color:#66a182">&#9679;</span> mobility</p>
