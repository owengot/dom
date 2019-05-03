<template>
  <div class="grid">
    <div class="row">
      <div>
        <nuxt-link to="/meditations/13">
          <img :src="images[13].url">
          <div class="status" v-bind:id="images[13].button"></div>
        </nuxt-link>
      </div>
       </div>
        <div class="row">
      <div>
        <nuxt-link to="/meditations/7">
          <img :src="images[7].url">
          <div class="status" v-bind:id="images[7].button"></div>
        </nuxt-link>
      </div>
       </div>
   
  </div>
</template>

<script>
import images from "~/content/meditations.json";
export default {
  data() {
    return {
      images
    };
  },
  asyncData({ params }) {
    // called every time before loading the component
    const slug = params.slug;

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


.grid
  width: 100vw !important
  display: block
  height: 100vh !important
  overflow: hidden
  .row
    display: block
    clear: both
    height: 50%
    padding: 4% 0 0 5%
    &:nth-child(2)
      padding: 0 0 0 5%
  div
    height: 90%
    width: auto
    float: none
    display: inline-block
  a
    width: auto
  img
    width: auto
    height: 90% !important
    clear: both
    display: block


.status
  width: 8px !important
  height: 8px !important
  margin: 10px auto 0 !important
  display: block !important
  clear: both
  border-radius: 20px
  &#green
    background: green
  &#red
    background: red

</style>

