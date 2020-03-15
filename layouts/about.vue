<template>
  <v-app dark>

    <AppBar />
    <v-parallax
      height="300"
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
          <h1 class="display-1 font-weight-thin mb-4">Meet Our Team</h1>

        </v-col>
      </v-row>
    </v-parallax>

    <v-content>

      <v-container class="pb-12">

        <nuxt />
      </v-container>
      <div class="mb-12">
        <DemoContact />
      </div>

      <Testimonials />

    </v-content>

    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import Contact from "~/components/sections/Contact.vue";

export default {
  components: {
    AppBar,
    Hero,
    DemoContact,
    Testimonials: () => import("~/components/sections/Testimonials"),
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
