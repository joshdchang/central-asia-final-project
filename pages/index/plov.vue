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
        <h3 class="font-bold text-5xl pb-6">Plov</h3>
        <progress class="progress my-10" v-if="!loaded"></progress>
        <template v-else>
          <p class="py-4 text-2xl">
            Plov, sometimes known as pilaf, is a popular rice stew dish in Central Asia and elsewhere. The constituent ingredients vary from place to
            place, but according to Russell Zanca, “The main ingredients for Uzbeks are rice, carrots, onions, mutton or beef, and plenty of salt and
            cumin.” Plov is the national dish of Uzbekistan.
          </p>
          <p class="py-4 text-2xl">
            Although plov is “ubiquitous” across various places, what makes Central Asian plov unique, and specifically Uzbek plov unique, is the sheer
            quantity of oil and fat. Zanca describes an Uzbek expression as saying, “A good plov is one where the oil drips to your elbow after you eat
            a handful from the platter.” This expression bluntly describes how much Uzbeks value oil in their plov.
          </p>
          <p class="py-4 text-2xl">
            So, why is oily plov so highly valued in Uzbekistan? Zanca argues it is to supplement a diet high in grains. “Lest the reader think that
            most rural Uzbeks enjoy such frequent oily repasts, it’s necessary to understand that most Uzbeks derive the bulk of their calories from
            grains, especially bread and rice.” To reiterate this point, he writes “the infrequent feasting and explosive consumption of rich,
            especially animal fat foods took place among peasantries and fat-deprived townspeople because so much of the rest of the diet comprised
            grain consumption.” Essentially, what Zanca points out is that when grains make up most of your diet, a fatty dish is not seen as an
            unhealthy indulgence but rather as a part of general nutrition. “Uzbeks want to praise and consume fats not only in the sense of imbibing
            the commonsensical good life but also because they see it as an essential part of healthful or nutritious dining,” Zanca writes, confirming
            that a constrained diet, based primarily on grains, is the reason many Uzbeks love oily plov.
          </p>
          <p class="py-4 text-2xl">
            This brings us to the concept that ties plov, and really all food, so deeply to the earth: agriculture. Agriculture is quite literally the
            foundation of civilization, and with food playing such a large role in everyday life and traditions, its cultural impact cannot be
            overstated. And, while agriculture is impacted by political and social realities, it is fundamentally based on land, water, soil, and other
            physical geographic features.
          </p>
          <p class="py-4 text-2xl">
            From the very beginning, Central Asian agriculture was grain based. In a paper titled “The spread of agriculture into northern Central Asia:
            Timing, pathways, and environmental feedbacks” Robert N Spengler writes, “The earliest crops introduced into Central Asia likely came as a
            mixed package of free-threshing wheat, naked barley, and broomcorn millet, an assemblage pioneered further south along the northern
            foothills of the Central Asian mountains.” Here, Spengler claims that wheat, barley, and millet — all cereal grains — were some of the first
            crops in Central Asia, which provides a good starting point for understanding their prominence. He also adds that they spread along the
            foothills and mountains, implying that topography played a role in this.
          </p>
          <p class="py-4 text-2xl">
            From there, agriculture spread north as a result of the specific mix of geological features, especially topography and water. Spengler
            writes, “The foothill ecotone provided a belt of arable land allowing crops from southern Central Asia to slowly become incorporated into
            the pastoralist system, already in place. Mountain barriers, such as the Altai, provide buffers to seasonal environmental extremes and
            climatic changes by allowing pastoralists to move up and down in elevation.” Again, it is clear that mountains and their layout played an
            essential role in spreading grains throughout Central Asia, acting as “buffers” to extremes and enabling the movement of grains into
            pastoralist communities.
          </p>
          <p class="py-4 text-2xl">
            In the modern day, agriculture in Central Asia is still deeply tied to geographic conditions. In a 2019 report titled, “Territorial
            Structure of Agriculture Development in Uzbekistan in Terms of Economical Geography,” Nilufar Komilova et al. writes, “Further industrial
            development has led to regional expansion of specialization and greater involvement of land and water resources,” implying that land and
            water are intertwined with agriculture — which matches intuition. Komilove also writes that, “grain plays an important role as the main
            agricultural sector in the country, and this direction has been established mainly in fertile lands in the valleys of the mountains, in the
            delta.” Here, Komilove restates the continued significance of grain as well as emphasizing how the physical geographical features of the
            land — valleys, mountains, and deltas — allows for the continued success of this grain agriculture, the grain agriculture that defines Uzbek
            cuisine, including plov.
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