<template>
  <v-app dark>

    <AppBar />
    <Hero />
    <v-content>

      <v-container class="pb-12">

        <nuxt />
      </v-container>
      <div class="mb-12">
        <Demo />
      </div>

      <Testimonials />

    </v-content>

    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import Demo from "~/components/sections/Demo.vue";
import Contact from "~/components/sections/Contact.vue";

export default {
  components: {
    AppBar,
    Hero,
    Demo,
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
