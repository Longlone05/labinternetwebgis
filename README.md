# labinternetwebgis
WebGIS Shortest Path Application

A WebGIS application for finding the shortest path between two locations using PostgreSQL/PostGIS, pgRouting, GeoServer, and Leaflet.
This project demonstrates how spatial databases and web mapping technologies can be integrated to build an interactive routing system.

Developed as part of the Internet WebGIS coursework at Nong Lam University Ho Chi Minh City.

📌 Features
Interactive WebGIS map interface
Shortest path analysis using Dijkstra Algorithm
Spatial data management with PostGIS
Network topology generation with pgRouting
Geospatial services via GeoServer
Dynamic map rendering using Leaflet
OpenStreetMap road network integration
WMS/WFS support for spatial layers
🛠️ Technologies Used
Technology	Description
PostgreSQL 15	Relational Database Management System
PostGIS 3.4	Spatial extension for PostgreSQL
pgRouting 3.6	Routing and network analysis extension
GeoServer 2.27	Geospatial data server
Leaflet 1.0	JavaScript library for interactive maps
OpenStreetMap	Road network data source

Based on the project report and implementation workflow.

⚙️ System Requirements

Before running the project, install the following software:

PostgreSQL 15+
PostGIS
pgRouting
GeoServer
Node.js or Live Server extension
QGIS (optional)

🌍 Data Preparation

Road network data is collected from OpenStreetMap using:

Overpass Turbo
GeoJSON format

Example Overpass query:
[out:json][timeout:25];
(
  way["highway"]["area"!="yes"]({{bbox}});
);
out body;
>;
out skel qt;
