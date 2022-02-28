<template>
  <v-app>
    <v-navigation :color="color" :flat="flat" />
    <v-main>
      <Header />

    </v-main>
    <v-scale-transition>
      <v-btn
      fab
      v-show="fab"
      v-scroll="onScroll"
      darkfixed
      bottom
      color="secondary"
      @click="toTop"
      >
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </v-scale-transition>
    <foote />
  </v-app>
</template>

<script>
import Header from './components/Header.vue';




import foote from './components/Footer.vue';

export default {
  name: 'App',

  components: {
    Header,
    foote,
  },

  data: () => ({
    //
  }),
};
</script>
