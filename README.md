# JXL vs AVIF simple benchmark

This is a simple benchmark to analyse compression and processing time of JXL and AVIF.

This is not a qualitative analysis of the resulting images. Also not a scientific study.

Read more about qualitative image comparison [here](https://kornel.ski/en/faircomparison).

## How to run

Clone this repo and run using GitHub Actions. Every push to master starts the benchmarking compression.

## Tools used

- [libjxl](https://github.com/libjxl/libjxl)
- [libavif](https://github.com/aomediacodec/libavif)
- [ffmpeg](https://ffmpeg.org) (for animated GIFs)

## Input images sources

I don't have the sources of all the input images, some are just from my collection.

* Eclipse: from NASA
* Central Asia map: https://www.britannica.com/place/Central-Asia
* Subway escalators: https://unsplash.com/photos/an-underground-subway-station-with-escalators-and-stairs-hLIi1IU5IU0

## Some results

### libjxl v0.12.0 q=90, libavif v1.4.2 q=90

| Input | Original size | JXL compression ratio | JXL processing time | AVIF compression ratio | AVIF processing time |
|:-:|:-:|:-:|:-:|:-:|:-:|
| bar.jpg | 302KB | -50% | 0.139s | -34% | 0.254s |
| boxes.jpg | 36KB | -25% | 0.061s | -28% | 0.166s |
| central-asia-elevation-map.png | 2104KB | -79% | 0.549s | -78% | 1.708s |
| curtains.gif | 1092KB | -66% | 0.756s | -82% | 6.736s |
| eclipse.gif | 130KB | +309% | 1.891s | -52% | 1.721s |
| emilia-clarke.gif | 3174KB | -57% | 2.432s | -70% | 17.138s |
| mclaren.png | 6223KB | -94% | 0.894s | -90% | 0.946s |
| misinformation.jpg | 33KB | -16% | 0.076s | -10% | 0.213s |
| organic_chemistry.png | 274KB | +254% | 2.378s | +38% | 2.926s |
| sky_plants.jpg | 5156KB | -37% | 2.01s | -22% | 3.559s |
| space.jpg | 9048KB | -77% | 1.439s | -64% | 2.933s |
| subway-escalators.jpg | 10982KB | -31% | 7.607s | -2% | 10.905s |
| waldo.jpg | 6117KB | -33% | 2.793s | -25% | 4.063s |

### libjxl v0.12.0 q=100 (lossless), libavif v1.4.2 q=90

| Input | Original size | JXL compression ratio | JXL processing time | AVIF compression ratio | AVIF processing time |
|:-:|:-:|:-:|:-:|:-:|:-:|
| bar.jpg | 302KB | -14% | 0.05s | -34% | 0.285s |
| boxes.jpg | 36KB | -20% | 0.02s | -28% | 0.179s |
| central-asia-elevation-map.png | 2104KB | -31% | 1.146s | -78% | 1.965s |
| curtains.gif | 1092KB | -48% | 1.282s | -82% | 6.852s |
| eclipse.gif | 130KB | -36% | 1.179s | -52% | 1.634s |
| emilia-clarke.gif | 3174KB | -15% | 4.059s | -70% | 16.586s |
| mclaren.png | 6223KB | -27% | 2.136s | -90% | 0.927s |
| misinformation.jpg | 33KB | -13% | 0.018s | -10% | 0.213s |
| organic_chemistry.png | 274KB | +14% | 1.818s | +38% | 2.89s |
| sky_plants.jpg | 5156KB | -19% | 0.273s | -22% | 3.502s |
| space.jpg | 9048KB | -20% | 0.496s | -64% | 2.955s |
| subway-escalators.jpg | 10982KB | -13% | 1.065s | -2% | 10.719s |
| waldo.jpg | 6117KB | -35% | 0.321s | -25% | 3.932s |
