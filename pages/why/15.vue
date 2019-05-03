<template>
  <div class="grid">
    <div class="row">
      <div>
        <nuxt-link to="/meditations/14">
          <img :src="images[14].url">
          <div class="status" v-bind:id="images[14].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/13">
          <img :src="images[13].url">
          <div class="status" v-bind:id="images[13].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/5">
          <img :src="images[5].url">
          <div class="status" v-bind:id="images[5].button"></div>
        </nuxt-link>
      </div>
    </div>
    <div class="row">
      <div>
        <nuxt-link to="/meditations/11">
          <img :src="images[11].url">
          <div class="status" v-bind:id="images[11].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/7">
          <img :src="images[7].url">
          <div class="status" v-bind:id="images[7].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/2">
          <img :src="images[2].url">
          <div class="status" v-bind:id="images[2].button"></div>
        </nuxt-link>
      </div>
    </div>
    <div class="row">
      <div>
        <nuxt-link to="/meditations/19">
          <img :src="images[19].url">
          <div class="status" v-bind:id="images[19].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/32">
          <img :src="images[32].url">
          <div class="status" v-bind:id="images[32].button"></div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="/meditations/10">
          <img :src="images[10].url">
          <div class="status" v-bind:id="images[10].button"></div>
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
  height: 33.3vh !important
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

