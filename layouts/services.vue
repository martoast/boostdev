<template>
  <v-app dark>

    <AppBar2 />

    <!-- <v-parallax
      height="200"
      src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
    >
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          class="text-center"
          cols="12"
        >
          <h1 class="display-1 font-weight-thin mb-4">Services</h1>

        </v-col>
      </v-row>
    </v-parallax> -->

    <v-content>

      <nuxt />

      <!-- <Demo /> -->
    </v-content>
    <Contact />

    <Footer />
  </v-app>
</template>

<script>
import AppBar2 from "~/components/core/AppBar2.vue";
import Contact from "~/components/sections/Contact.vue";

export default {
  components: {
    AppBar2,
    Footer: () => import("~/components/core/Footer"),
    Contact
  },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  }
};
</script>
