<template>
  <div class="grid">
    <div class="row">
      <div>
        <nuxt-link to="/meditations/26">
          <img :src="images[26].url">
          <div class="status" v-bind:id="images[26].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/10">
          <img :src="images[10].url">
          <div class="status" v-bind:id="images[10].button"></div>
        </nuxt-link>
      </div>

      <div>
        <nuxt-link to="/meditations/24">
          <img :src="images[24].url">
          <div class="status" v-bind:id="images[24].button"></div>
        </nuxt-link>
      </div>

      <div>
        <nuxt-link to="/meditations/11">
          <img :src="images[11].url">
          <div class="status" v-bind:id="images[11].button"></div>
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
  display: flex
  justify-content: center
  align-items: center
  height: 100vh !important

.row
  width: 100%
  display: flex
  justify-content: center
  flex-direction: row
  box-sizing: border-box
  max-height: 700px
  padding: 2%
  a
    display: flex
    flex-direction: column
    width: auto
  div:nth-child(2)
    margin: 0 2% 0 2%
  div:nth-child(3)
    margin: 0 2% 0 0
  img
    width: auto
    max-height: 300px !important
    display: inline-block


.status
  width: 8px !important
  height: 8px !important
  margin: 10px auto 0 !important
  display: inline-block !important
  border-radius: 20px
  &#green
    background: green
  &#red
    background: red
</style>

