<template>
  <main>
    <div class="grid">
      <div class="row">
        <div class="text">
          <p>
            To be, or not to be: that is the question:
            Whether ‘tis nobler in the mind to suffer
            The slings and arrows of outrageous fortune,
            Or to take arms against a sea of troubles,
            And by opposing end them? To die: to sleep;
            No more; and by a sleep to say we end
            The heart-ache and the thousand natural shocks
            That flesh is heir to, ‘tis a consummation
            Devoutly to be wish’d. To die, to sleep;
            To sleep: perchance to dream: ay, there’s the rub;
            For in that sleep of death what dreams may come
            When we have shuffled off this mortal coil,
            Must give us pause: there’s the respect
            That makes calamity of so long life;
            For who would bear the whips and scorns of time,
            The oppressor’s wrong, the proud man’s contumely,
            The pangs of despised love, the law’s delay,
            The insolence of office and the spurns
            That patient merit of the unworthy takes,
            When he himself might his quietus make
            With a bare bodkin? who would fardels bear,
            To grunt and sweat under a weary life,
            But that the dread of something after death,
            The undiscover’d country from whose bourn
            No traveller returns, puzzles the will
            And makes us rather bear those ills we have
            Than fly to others that we know not of?
            Thus conscience does make cowards of us all;
            And thus the native hue of resolution
            Is sicklied o’er with the pale cast of thought,
            And enterprises of great pith and moment
            With this regard their currents turn awry,
            And lose the name of action.—Soft you now!
            The fair Ophelia! Nymph, in thy orisons
            Be all my sins remember’d.
          </p>
        </div>

        <div>
          <nuxt-link to="/meditations/1">
            <img :src="images[21].url">
            <div class="status" v-bind:id="images[21].button"></div>
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

.text
  width: 70% !important
  padding: 0 2% 0 2%
  p
    font-size: 13px

.row
  div:nth-child(2)
    margin: 0 2% 0


</style>

