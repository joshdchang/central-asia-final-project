<template>
  <Html class="bg-slate-100">
    <Head>
      <Title>Central Asia: Is Physical Geography Destiny?</Title>
    </Head>
  </Html>
  <div class="absolute inset-14 grid items-center w-full max-w-5xl mx-auto">
    <div class="grid items-center justify-between font-serif grid-flow-col gap-2 self-end mb-8">
      <div class="grid gap-2">
        <div class="text-xl uppercase tracking-widest text-slate-600">
          Central Asia
        </div>
        <div class="text-4xl font-bold text-slate-900">
          Is Physical Geography Destiny?
        </div>
      </div>
      <NuxtLink
        to="/about"
        class="text-xl text-slate-500 hover:text-slate-600 bg-slate-200 hover:bg-slate-300 transition-colors hover:cursor-pointer pt-3 pb-2 px-8 rounded-full">
        About this project
      </NuxtLink>
    </div>
    <div class="relative border-2 border-slate-500 overflow-hidden rounded-2xl self-start h-[70vh] max-h-full">
      <l-map style="max-height: 100% !important;" :zoom="5" :minZoom="5" :maxZoom="10" :zoomAnimation="true" :center="[45.6, 68]" :markerZoomAnimation="true"
        :maxBounds="[
          [35.21639549928713, 90.44351810932858],
          [55.64710121676032, 45.45447164119719],
        ]">
        <l-image-overlay
          :url="image"
          :bounds="bounds"
          :options="imageOptions"></l-image-overlay>
        <l-geo-json
          :geojson="geojson"
          :options="geojsonOptions"></l-geo-json>
      </l-map>
    </div>
    <NuxtPage />
  </div>
</template>

<script>
  import { LMap, LGeoJson, LImageOverlay } from "@vue-leaflet/vue-leaflet";

  export default {
    components: {
      LMap,
      LGeoJson,
      LImageOverlay,
    },
    data() {
      return {
        geojson: {
          type: "FeatureCollection",
          features: [
            {
              "type": "Feature",
              "properties": {
                "name": "yurt",
                "image": "artifacts/yurt.jpg"
              },
              "geometry": {
                "type": "Point",
                "coordinates": [69, 49]
              }
            },
            // {
            //   "type": "Feature",
            //   "properties": {
            //     "name": "clothes",
            //     "image": "artifacts/bazaar.png"
            //   },
            //   "geometry": {
            //     "type": "Point",
            //     "coordinates": [79, 40]
            //   }
            // },
            {
              "type": "Feature",
              "properties": {
                "name": "sulaiman",
                "image": "artifacts/sulaiman.jpg"
              },
              "geometry": {
                "type": "Point",
                "coordinates": [72.8, 41.3]
              }
            },
            {
              "type": "Feature",
              "properties": {
                "name": "plov",
                "image": "artifacts/plov.jpg"
              },
              "geometry": {
                "type": "Point",
                "coordinates": [64, 42]
              }
            },
          ],
        },
        geojsonOptions: {
          // Options that don't rely on Leaflet methods.
        },
        image: "terrain3.png",
        bounds: [
          [35.21639549928713, 45.45447164119719],
          [55.64710121676032, 90.44351810932858],
        ],
        imageOptions: {
          // Options that don't rely on Leaflet methods.
        },
      };
    },
    async beforeMount() {
      // HERE is where to load Leaflet components!
      const { marker, icon } = await import("leaflet/dist/leaflet-src.esm");

      // And now the Leaflet circleMarker function can be used by the options:
      this.geojsonOptions.pointToLayer = (feature, latLng) => {
        return marker(latLng, {
          icon: icon({
            iconUrl: feature.properties.image,
            iconSize: [70, 70],
            iconAnchor: [35, 35],
            className: "click-" + feature.properties.name,
          })
        });
      }
      this.mapIsReady = true;
    },
    async mounted() {
      for(let name of ["yurt", "clothes", "sulaiman", "plov"]) {
      
        const interval = setInterval(() => {
          const artifact = document.querySelector(".click-" + name);
          if (artifact) {
            artifact.addEventListener("click", () => {
              console.log(name)
              this.$router.push("/" + name);
            })
            clearInterval(interval)
          }
        }, 100)
      }
    }
  };
</script>

<style>
  .leaflet-touch .leaflet-control-layers,
  .leaflet-touch .leaflet-bar {
    @apply border-none shadow-lg rounded-lg overflow-hidden;
  }

  .leaflet-touch .leaflet-bar a span {
    @apply relative bottom-[2px];
  }

  .leaflet-control-attribution {
    @apply hidden;
  }

  .leaflet-interactive {
    @apply drop-shadow-lg;
  }

  .leaflet-marker-icon {
    @apply border-white border-4 rounded-full;
  }
  .leaflet-top, .leaflet-bottom {
    z-index: 1000;
  }
</style>