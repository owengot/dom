<template>
  <div class="grid">
    <div class="row">
      <div>
        <nuxt-link to="/meditations/27">
          <img :src="images[27].url">
          <div class="status" v-bind:id="images[27].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/35">
          <img :src="images[35].url">
          <div class="status" v-bind:id="images[35].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/17">
          <img :src="images[17].url">
          <div class="status" v-bind:id="images[17].button"></div>
        </nuxt-link>
      </div>
    </div>
    <div class="row">
      <div>
        <nuxt-link to="/meditations/3">
          <img :src="images[3].url">
          <div class="status" v-bind:id="images[3].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/22">
          <img :src="images[22].url">
          <div class="status" v-bind:id="images[22].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/12">
          <img :src="images[12].url">
          <div class="status" v-bind:id="images[12].button"></div>
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

.row
  display: flex
  justify-content: center
  flex-direction: row
  box-sizing: border-box
  height: 50vh !important
  padding: 2%
  div
    width: 33.33%
    height: 100%
    a 
      width: 100%
      height: 100%;
      text-align: center
      display: flex
      justify-content: center
      align-items: center
      flex-direction: column
      img
        width: auto
        max-height: 70%
        display: block
        margin: 0 auto 2% !important


.status
  width: 8px !important
  height: 8px !important
  margin: 4px auto 0 !important
  display: inline-block !important
  border-radius: 20px
  &#green
    background: green
  &#red
    background: red

</style>

