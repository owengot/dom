<template>
  <div class="grid">
    <div class="row">
     
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
  width: 95%
  height: 100% !important
  margin: 0 auto
  clear: both
  display: inline-block
  overflow: hidden
  div
    width: 32%
    height: 100%
    float: left
    &:nth-child(2)
      margin: 0 2% 0 
      width: 32%
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
        height: 50%
        display: inline-block
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

