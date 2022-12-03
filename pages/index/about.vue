<template>
  <div>
    <div class="modal modal-open font-serif z-[1001]">
      <div class="modal-box w-11/12 max-w-4xl p-24">
        <div class="grid gap-2 pb-6">
          <div class="text-2xl uppercase tracking-widest text-slate-600">
            Central Asia
          </div>
          <div class="text-5xl font-bold text-slate-900">
            Is Physical Geography Destiny?
          </div>
        </div>
        <p class="py-4 text-2xl">
          Consider your surroundings. Where are you right now? What do you notice? If you are reading this, chances are you are indoors, in
          a room,
          surrounded by walls, a floor, and a ceiling. And, that sort of environment is probably where you spend most of your day. Whether
          we are
          sleeping, eating, showering, relaxing, driving, or working, the vast majority of our life is spent experiencing things that were
          created by
          people. In our everyday existence, the scale of the man-made environment feels endless, and endlessly important.
        </p>
        <p class="py-4 text-2xl">
          Our maps confirm this intuition. They are littered with human inventions: words and lines defining cities, states, countries,
          continents,
          and other features of political geography. But, as we all know (but often forget), none of these concepts exist on the physical
          Earth.
        </p>
        <p class="py-4 text-2xl">
          Take
          this image from a NASA satellite: even at this scale, which accounts for less than a twentieth of our planet’s surface, it is
          nearly
          impossible to discern any artifact of human existence.
        </p>
        <div class="py-4">
          <img src="/sattelite.png" class="w-full rounded-lg">
          <figcaption class="mt-3">Source: NASA</figcaption>
        </div>
        <p class="py-4 text-2xl">
          That isn’t to say that political geography isn’t important — it obviously is. But, it is easy to overlook, amidst the business of
          everyday
          life, that we live on a huge, powerful, dynamic planet that, like it or not, shapes how we live.
        </p>
        <p class="py-4 text-2xl">
          This project seeks to explore the connection between the physical and cultural landscapes of Central Asia. It aims to give a small
          glimpse
          into how the earth influences the expression of music, religion, food, and lifestyle of the region.
        </p>
        <p class="py-4 text-2xl">
          The map for this project is probably different from the maps you are used to. It is designed with the goal of demonstrating the
          Earth as a
          physical object rather than a political concept. It strips away all the labels and borders, and instead is based on scientific
          data
          collected about the world itself. To render the map, I first used elevation data from NASA to create a three-dimensional model of
          Central
          Asia in an open-source three-dimensional animation program called Blender (similar to the programs used by Pixar, for example). In
          Blender,
          I added two light sources, one from directly overhead to illuminate the entire landscape and one that is placed to the top right
          of the
          landscape, creating shadows and highlights that make it look three-dimensional. I then overlaid a color layer called a “hypometric
          tint,”
          which is just a fancy word for a mixture of temperature and precipitation. Places with more precipitation are more green and
          places with
          less are more tan. Places with a higher elevation are lighter in color, like the white mountain peaks. The hypsometric tint is
          based on data
          from another open-source project called Natural Earth. Finally, I placed a layer to show major lakes, rivers, and seas, also
          derived from
          Natural Earth. The overall idea was to create a map that feels “real,” that almost feels like you could touch it.
        </p>
        <p class="py-4 text-2xl">
          Each of the icons on the map represents one example of a cultural artifact, and if you click on one, it will open an explanation
          of the
          artifact and its connection to the Earth. The artifacts — a yurt, mosque, dish, bazaar, and instrument — come from diverse parts
          of Central
          Asian culture, although by no means do they represent the entirety, or even a sliver, of what the region has to offer. Another
          thing to
          note: the location where the icon is placed on the map roughly corresponds to a place where that artifact can be found, but that
          doesn’t
          mean that region is the only place where the artifact holds significance.
        </p>
        <p class="py-4 text-2xl">
          Perhaps the best way to think of this project is as an interactive essay: this summary is like the introduction and conclusion,
          the
          artifacts each represent a body paragraph, and the website and map act as transitions. I hope that, as you explore, you gain a new
          perspective on the geography of Central Asia and its connection to culture. Additionally, I hope that you think about maps, their
          purpose,
          and their impact.
        </p>
        <div class="modal-action">
          <NuxtLink to="/">
            <label for="my-modal-5" class="btn px-7 pb-1 pt-2 text-lg tracking-wide">Back</label>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>