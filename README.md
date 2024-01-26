# JXL vs AVIF simple benchmark

This is a simple benchmark to analyse compression and processing time of JXL and AVIF.

This is not a qualitative analysis of the resulting images. Also not a scientific study.

Read more about qualitative image comparison [here](https://kornel.ski/en/faircomparison).

## How to run

Clone this repo and run using GitHub Actions. Every push to master starts the benchmarking compression.

The numbers for comparison can be obtained inside the .zip files produced.

## Input images sources

I don't have the sources of all the input images, some are just from my collection.

* Eclipse: from NASA
* Central Asia map: https://www.britannica.com/place/Central-Asia
* Subway escalators: https://unsplash.com/photos/an-underground-subway-station-with-escalators-and-stairs-hLIi1IU5IU0

## Some results

### JXL q=90, AVIF q=90

libjxl version: 0.9.1
libjxl quality factor: 90
cavif-rs version: 1.5.5
cavif-rs quality factor: 90

| Input | Original size | JXL compression ratio | JXL processing time | AVIF compression ratio | AVIF processing time |
|-------|---------------|-----------------------|---------------------|------------------------|----------------------|
| bar.jpg | 302KB | -51% | 0.139s | -55% | 2.396s |
| boxes.jpg | 36KB | -20% | 0.063s | -48% | 0.712s |
| central-asia-elevation-map.png | 2104KB | -79% | 0.84s | -87% | 8.831s |
| curtains.gif | 1092KB | -62% | 0.983s | -98% | 5.651s |
| eclipse.gif | 130KB | 389% | 1.694s | -70% | 2.911s |
| emilia-clarke.gif | 3174KB | -20% | 2.32s | -98% | 12.32s |
| mclaren.png | 6223KB | -94% | 1.003s | -97% | 10.784s |
| misinformation.jpg | 33KB | -10% | 0.065s | -34% | 0.808s |
| organic_chemistry.png | 274KB | 208% | 3.585s | 36% | 30.855s |
| sky_plants.jpg | 5156KB | -39% | 1.758s | -44% | 38.25s |
| space.jpg | 9048KB | -79% | 1.598s | -76% | 26.657s |
| subway-escalators.jpg | 10982KB | -34% | 8.619s | -25% | 81.62s |

### JXL q=80, AVIF q=80

libjxl version: 0.9.1
libjxl quality factor: 80
cavif-rs version: 1.5.5
cavif-rs quality factor: 80

| Input | Original size | JXL compression ratio | JXL processing time | AVIF compression ratio | AVIF processing time |
|-------|---------------|-----------------------|---------------------|------------------------|----------------------|
| bar.jpg | 302KB | -71% | 0.131s | -76% | 1.803s |
| boxes.jpg | 36KB | -39% | 0.06s | -64% | 0.558s |
| central-asia-elevation-map.png | 2104KB | -85% | 0.786s | -91% | 7.836s |
| curtains.gif | 1092KB | -76% | 0.97s | -98% | 5.561s |
| eclipse.gif | 130KB | 294% | 1.706s | -70% | 2.846s |
| emilia-clarke.gif | 3174KB | -45% | 2.175s | -98% | 12.185s |
| mclaren.png | 6223KB | -97% | 0.968s | -99% | 10.651s |
| misinformation.jpg | 33KB | -34% | 0.063s | -55% | 0.718s |
| organic_chemistry.png | 274KB | 134% | 3.613s | 8% | 30.316s |
| sky_plants.jpg | 5156KB | -61% | 1.667s | -66% | 35.361s |
| space.jpg | 9048KB | -86% | 1.526s | -86% | 21.839s |
| subway-escalators.jpg | 10982KB | -63% | 7.762s | -51% | 74.183s |

