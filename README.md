# map-handson

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

This project demonstrates how to display maps and markers using SPARQL queries on Google Maps.

## Features
- Displays a Google Map with markers for various facilities like schools, nurseries, and civic points of interest
- Allows filtering and searching facilities based on SPARQL queries
- Provides example usage of the `odp.js` and `fukuno.js` libraries for SPARQL queries and map handling

## Requirements
- Google Maps API key

## Usage
1. Include the necessary JavaScript libraries:
   - `https://maps.google.com/maps/api/js?key=YOUR_API_KEY`
   - `fukuno.js`
   - `odp.js`
2. Create a map container element in your HTML.
3. Use the provided sample code to initialize the map and perform SPARQL queries to display markers.

## Data / API
This project uses the [Open Data Portal (ODP)](http://sparql.odp.jig.jp/data/sparql) as the SPARQL endpoint to retrieve facility data.

## License
This project is licensed under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.