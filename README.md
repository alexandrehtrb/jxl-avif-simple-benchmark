# JXL vs AVIF simple benchmark

This is a simple benchmark to analyse compression and processing time of JXL and AVIF.

This is not a qualitative analysis of the resulting images. Also not a scientific study.

## How to run

Clone this repo and run using GitHub Actions. Every push to master starts the benchmarking compression.

The numbers for comparison can be obtained inside the .zip files produced.

## Input images sources

I don't have the sources of all the input images, some are just from my collection.

* Eclipse: from NASA
* Central Asia map: https://www.britannica.com/place/Central-Asia
* Subway escalators: https://unsplash.com/photos/an-underground-subway-station-with-escalators-and-stairs-hLIi1IU5IU0

## Last results

| Source | Source file size | JXL file size | JXL size diff | JXL processing time | AVIF file size | AVIF size diff | AVIF processing time |
|--------|------------------|---------------|---------------|---------------------|----------------|----------------|----------------------|
| bar.jpg | 302KB | 150KB | -51% | 1s | 136KB | -55% | 5s |
| boxes.jpg | 36KB | 29KB | -20% | 1s | 19KB | -48% | 2s |
| central-asia-elevation-map.png | 2104KB | 450KB | -79% | 2s | 293KB | -87% | 16s |
| curtains.gif | 1092KB | 415KB | -62% | 2s | 32KB | -98% | 8s |
| eclipse.gif | 130KB | 636KB | 389% | 4s | 40KB | -70% | 4s |
| emilia-clarke.gif | 3174KB | 2558KB | -20% | 5s | 79KB | -98% | 17s |
| mclaren.png | 6223KB | 416KB | -94% | 2s | 225KB | -97% | 18s |
| misinformation.jpg | 33KB | 30KB | -10% | 1s | 22KB | -34% | 2s |
| organic_chemistry.png | 274KB | 844KB | 208% | 9s | 371KB | 35% | 54s |
| sky_plants.jpg | 5156KB | 3171KB | -39% | 4s | 2915KB | -44% | 67s |
| space.jpg | 9048KB | 1984KB | -79% | 4s | 2249KB | -76% | 45s |
| subway-escalators.jpg | 10982KB | 7344KB | -34% | 18s | 8312KB | -25% | 147s |
