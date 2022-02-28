<template>
  <v-app>
    <navigation :color="color" :flat="flat" />
    <v-main>
      <Header />
      <HomeSection />
    </v-main>
    <v-scale-transition>
      <v-btn
        fab
        v-show="fab"
        v-scroll="onScroll"
        dark
        fixed
        bottom
        right
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
import Header from "./components/Header.vue";
import HomeSection from "./components/HomeSection";

import foote from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    Header,
    foote,
    HomeSection,
  },

  data: () => ({
    //
  }),
};
</script>
