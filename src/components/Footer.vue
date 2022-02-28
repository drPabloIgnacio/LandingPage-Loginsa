<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nesciunt nobis
        officiis eligendi ipsum impedit reprehenderit deleniti consequuntur
        omnis? Quod cumque adipisci accusamus minima ut dolore veniam nihil unde
        error repellendus! Nihil dolore sint sunt? Ea, aspernatur labore libero
        facilis quibusdam suscipit fuga mollitia. Doloribus rem quibusdam ea
        quam architecto enim consequuntur ad commodi animi expedita cumque,
        error, explicabo adipisci voluptatibus?
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Saepe
        explicabo iste in tempore id corporis exercitationem enim ad, dolores
        veritatis consectetur alias a quae? Labore fugit debitis quos doloribus
        quam.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        &copy; {{ new Date().getFullYear() }} - <strong>Loginsa</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "",
      },
      {
        text: "mdi-twitter",
        link: "https://twitter.com/loginsachile",
      },
      {
        text: "mdi-instagram",
        link: "",
      },
      {
        text: "mdi-web",
        link: "http://www.loginsa.com/",
      },
    ],
  }),
};
</script>

<style>
.v-card {
  width: 100%;
}
</style>