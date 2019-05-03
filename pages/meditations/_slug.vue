<template>
<div>
  <main>
          <img :src="'http://localhost:3000'+images[slug].url" />
          <div class="status" v-bind:id='images[slug].button'></div>
           <div class="links">
            <nuxt-link :to="images[slug].link.left">< left</nuxt-link>
            <nuxt-link :to="images[slug].link.up">up</nuxt-link>
            <nuxt-link :to="images[slug].link.down">down</nuxt-link>
            <nuxt-link :to="images[slug].link.right">right ></nuxt-link>
          </div>
          <div class="index">
             <nuxt-link :to="images[slug].link.index">index</nuxt-link>
          </div>
           </main>
          
                </div>
</template>



<script>
import images from "~/content/meditations.json";
export default {
   data() {
    return {
      images
    }
  },
   asyncData ({ params }) {
    // called every time before loading the component
    const slug = params.slug;
  
    return {
      slug
    }
  },
  //  transition (to, from) {
  //   if (!from) { return 'slide-left' } else {return 'slide-right'}
  // },

  components: {
  }
};
</script>

<style lang="sass" scoped>
main
  width: 100%
  margin: 0 auto
  overflow: hidden
  position: absolute
  top: 30px
  img
    height: 80vh
    margin: 0 auto !important
    display: block

.index
  margin: 0px auto
  width: auto
  text-align: center
  display: block
  position: relative
.links
  margin: 10px auto 0
  width: auto
  text-align: center
  display: block
  position: relative

.status
  width: 23px
  height: 23px
  margin: 20px auto 0
  border-radius: 60px
  &#green
    background: green
  &#red
    background: red


</style>

