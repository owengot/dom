<template>
  <div class="grid">
    <div class="row">
      <div>
        <nuxt-link to="/26pictures/2">
          <img src="/26pictures/pages/1.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/2">
          <img src="/26pictures/pages/2.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/4">
          <img src="/26pictures/pages/4.jpg">
        </nuxt-link>
      </div>
    </div>
    <div class="row">
      <div>
         <nuxt-link to="/26pictures/6">
          <img src="/26pictures/pages/6.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/8">
          <img src="/26pictures/pages/8.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/10">
          <img src="/26pictures/pages/10.jpg">
        </nuxt-link>
      </div>
    </div>
    <div class="row">
      <div>
         <nuxt-link to="/26pictures/12">
          <img src="/26pictures/pages/12.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/14">
          <img src="/26pictures/pages/14.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/16">
          <img src="/26pictures/pages/16.jpg">
        </nuxt-link>
      </div>
    </div>

    <div class="row">
      <div>
         <nuxt-link to="/26pictures/18">
          <img src="/26pictures/pages/18.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/20">
          <img src="/26pictures/pages/20.jpg">
        </nuxt-link>
      </div>
      <div>
         <nuxt-link to="/26pictures/22">
          <img src="/26pictures/pages/22.jpg">
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
  height: 25vh !important
  padding: 0%
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

