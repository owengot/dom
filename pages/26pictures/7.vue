<template>
<main>
  <div class="grid">
    <div class="row">
    
      <div>
        <nuxt-link to="/meditations/19">
          <img :src="images[7].url">
          <div class="status" v-bind:id="images[7].button"></div>
        </nuxt-link>
      </div>
    
      <div>
        <nuxt-link to="/meditations/1">
          <img :src="images[8].url">
          <div class="status" v-bind:id="images[8].button"></div>
        </nuxt-link>
      </div>
   </div>
    </div>
    <div class="navigation">
      <div class="links">
        <nuxt-link :to="nav[slug].link.left">< left</nuxt-link>
        <nuxt-link :to="nav[slug].link.up">up</nuxt-link>
        <nuxt-link :to="nav[slug].link.down">down</nuxt-link>
        <nuxt-link :to="nav[slug].link.right">right ></nuxt-link>
      </div>
      <div class="index">
        <nuxt-link :to="nav[slug].link.index">index</nuxt-link>
      </div>
    </div>
  </main>
</template>

<script>
import images from "~/content/26pictures.json";
import nav from "~/content/26pictures_nav.json";

export default {
  data() {
    return {
      images,
      nav
    };
  },
  asyncData({ params, route }) {
    // called every time before loading the component
    const slug = route.path.split("/")[2];

    return {
      slug
    };
  },
  //  transition (to, from) {
  //   if (!from) { return 'slide-left' } else {return 'slide-right'}
  // },

  components: {}
};
</script>

<style lang="sass" scoped>
@import '~/assets/pictures.sass'
</style>