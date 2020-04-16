<template>
  <v-app dark>

    <AppBar />
    <v-parallax src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg">
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          class="text-center"
          cols="12"
        >
          <h1 class="display-1 font-weight-thin mb-4">Web Design & Development</h1>
          <h3>Quality design with lighting performance</h3>
          <div class="pt-6">
            <v-btn
              class="mr-md-3 my-2"
              color="white"
              large
              min-width="175"
              outlined
              rounded
              to="/about/"
            >
              Learn More
            </v-btn>

            <v-btn
              class="text--primary my-2"
              color="white"
              large
              min-width="175"
              rounded
              href="tel: +1 (619) 888-5258"
            >
              <v-icon class="pa-2">mdi-phone-outgoing</v-icon>
              CALL NOW
            </v-btn>

          </div>

        </v-col>
      </v-row>
    </v-parallax>

    <v-content>
      <v-container class="pb-12">
        <nuxt />
      </v-container>
      <Demo />
    </v-content>

    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import Demo from "~/components/sections/Demo.vue";
import PageHeader from "~/components/PageHeader.vue";
import Contact from "~/components/sections/Contact.vue";

export default {
  components: {
    AppBar,
    Hero,
    Demo,
    Footer: () => import("~/components/core/Footer"),
    PageHeader,
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
