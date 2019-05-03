<template>

<div class="grid">
<div v-for="item in about">
{{ item.file }}
<img :src="'/pages/' + item.file" />
</div>


</div>

</template>

<script>
import about from "~/assets/why37.json";

export default {
  data() {
    return {
      about
    }
  },
  name: "Index",
};
</script>
<style lang="sass">
.grid
  width: 100vw !important
  display: block
  height: 100vh !important

.row
  width: 100%
  height: 25vh !important
  display: flex
  justify-content: space-between
  div
    height: 100%
    width: 33.33%
    border: 1px solid green
    display: inline-flex
    justify-items: center
    align-content: center
    img
      height: 90%
      width: auto
      display: inline-block
      margin: 2% auto !important


</style>

