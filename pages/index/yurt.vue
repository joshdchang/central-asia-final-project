<script setup>
  const loaded = ref(false)
  setTimeout(() => {
    loaded.value = true
  }, 2000)
</script>
<template>
  <div>
    <div class="modal modal-open font-serif z-[1001]">
      <div class="modal-box w-11/12 max-w-4xl p-24">
        <h3 class="font-bold text-5xl pb-6">The Yurt</h3>
        <progress class="progress my-10" v-if="!loaded"></progress>
        <template v-else>
          <p class="py-4 text-2xl">
            The yurt, a type of dwelling used by nomadic and semi-nomadic people, is one of the most recognizable symbols of nomadic life on
            the Central Asia steppe. Yurts come in different varieties,
            but most
            have generally the same structure. In a paper titled “​​Architecture of the yurt and its impact on teaching young architects,”
            Zhandarbek
            Malibekuly writes, “Basically, the yurt is divided into three structural parts: the kerege, uyk and shanyrak.”
          </p>
          <p class="py-4 text-2xl">
            According to Malibekuly, “The kerege is a bearing structural element,…. The uyk is a constructive element that rests on a kerege
            base under
            an incline, and is fixed at the end to support the shanyrak. The insulation of what is called uzіk felt, rests on the uyk and
            provides heat
            inside the yurt; at the same time as protecting it from precipitation, e.g. snow and rain. The shanyrak is the upper part of the
            yurt.
            Dome-shaped, the shanyrak protects the yurt from pressure in the form of snow and rain because of its shape. The round,
            streamlined shape of
            a truncated cone provides protection from strong winds.”
          </p>
          <p class="py-4 text-2xl">
            From this description, it is clear that the yurt and its design are largely a function of the environment in which it exists.
            The
            overall
            form of the yurt is to fight against “strong winds,” and other major aspects of the design combat the precipitation of the
            steppe,
            including
            snow, rain.
          </p>
          <p class="py-4 text-2xl">
            Perhaps the best evidence of the yurt as a function of its environment are the variations of yurts from place to place.
            Malibekuly
            writes,
            “In the Mongolian steppe, climatic conditions vary with sultry, strong winds whereas mountainous areas with rocky slopes are
            characteristic
            of Kyrgyzstan. Residential settlements are located mainly between the mountain ranges. The characteristic shape of the
            configuration of the
            Kyrgyz yurt is elongated and pointed. The yurts of the mountainous Altai retained the type of a classical hut or polygonal log
            ail. Forests
            and mountains cover the area from Altai to the Caspian Sea between about 45⁰ and 50⁰ north latitude. In addition, in the vast
            expanses of
            the Kazakh steppe, the yurts differ, but the overall proportions of the Kazakh yurts differ from others in the neighboring
            states
            of Russia,
            Kyrgyzstan, Mongolia and others.” (Malibekuly et al).
          </p>
          <p class="py-4 text-2xl">
            From the steppe to the mountains to the forest, Malibekuly shows that the physical environment is perhaps the single most
            important factor
            guiding the differences between yurts across regions. Precipitation, wind, vegetation, topography, and latitude all have a
            profound
            influence on the yurt’s shape and structure.
          </p>
          <p class="py-4 text-2xl">
            The yurt, however, is not simply a utilitarian object. The yurt is also a place of art and spiritual culture. According to
            Yelena Yurievna
            Lichman, “The Kazakh yurt is not only an element of material culture of the folk, but also contains symbolism, in which
            different
            information about religious and mythological image of the world is focused. In Kazakhs folk image of the world available to
            usual conscious,
            such external features of the surrounding world as the sky, the Sun, the stars and the steppe served as a model for the outer
            and inner
            space of yurt.” Even the spiritual aspects of the yurt are connected to the land and the environment. According to Lichman, the
            “surrounding
            world” is central to the image of the yurt in a religious and mythological sense.
          </p>
          <p class="py-4 text-2xl">
            The yurt is defined and characterized, perhaps most clearly of all the artifacts in this project, by the physical landscape it
            exists in and
            the climatic conditions that it protects its inhabitants from. The yurt, an essential part of Central Asian nomadic and
            semi-nomadic
            culture, is a dwelling place, but more than that, it is a grounded symbol of identity amidst a constantly changing world.
          </p>
          <p class="py-6 text-lg">
            Note: the bibliography will be here, but I'm going to wait until I after I finish editing the content in case things change.
          </p>
        </template>
        <div class="modal-action">
          <NuxtLink to="/">
            <label for="my-modal-5" class="btn px-7 pb-1 pt-2 text-lg tracking-wide">Back</label>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>