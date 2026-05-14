# map-handson

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

This project provides a hands-on tutorial for displaying open data on Google Maps using SPARQL queries.

## Live Demos & Tutorial Steps

These examples progressively introduce concepts from basic map display to complex data queries. Start with `index.html` to see all demos.

*   **[index.html](index.html)**: Main index of all demos.
*   **[map1.html](map1.html)**: Displays a basic Google Map.
*   **[map2.html](map2.html)**: Adds a single, static marker to the map.
*   **[map3.html](map3.html)**: Executes a simple SPARQL query to fetch and display multiple data points.
*   **[map4.html](map4.html)**: Filters SPARQL results by a keyword in the data.
*   **[map5.html](map5.html)**: Filters SPARQL results using a geographic bounding box (latitude/longitude).
*   **[map-school.html](map-school.html)**: Application example mapping elementary schools in the Shinjuku and Shinagawa areas of Tokyo.
*   **[map-nursery.html](map-nursery.html)**: Application example mapping nurseries and kindergartens in the Shinagawa area.

## Features

*   Step-by-step HTML examples for learning SPARQL and map integration.
*   Renders data points from SPARQL queries as markers on an interactive Google Map.
*   Demonstrates filtering data by keywords and geographic coordinates.
*   Marker click events to display details for each location.
*   Includes reusable JavaScript utility libraries (`fukuno.js`, `odp.js`).

## Getting Started

1.  Clone or download this repository.
2.  Run a local web server in the project's root directory.
3.  Open `index.html` in your web browser to see the list of demos.

**Note on Google Maps API Key:** The demo files are pre-configured with a Google Maps API key for convenience. If the map fails to load, the key may have expired. You can replace it with your own key by editing the `<script>` tag in the HTML files:

```html
<script src="https://maps.google.com/maps/api/js?key=YOUR_OWN_API_KEY"></script>
```

## Code Overview

*   **`.html` files**: Each file is a self-contained example. View the source to see how the map is initialized and the SPARQL query is constructed and executed.
*   **`fukuno.js`**: A general-purpose utility library providing helper functions for DOM manipulation, JSONP requests, and more.
*   **`odp.js`**: A helper library specifically for querying the Open Data Portal (ODP) SPARQL endpoint. Note that the primary HTML demos use a different endpoint and an inline query function for clarity.

## Data Sources

The examples query public SPARQL endpoints to retrieve civic facility data.

*   **[https://sparql.opendata.cc/data/sparql](https://sparql.opendata.cc/data/sparql)**: Used in the primary HTML demos (`map3.html`, `map-school.html`, etc.).
*   **[http://sparql.odp.jig.jp/data/sparql](http://sparql.odp.jig.jp/data/sparql)**: The target endpoint for the `odp.js` helper library.

## License and Attribution

This project is licensed under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.

Created by [Taisuke Fukuno / Ichinichi Isso](http://fukuno.jig.jp/2073).