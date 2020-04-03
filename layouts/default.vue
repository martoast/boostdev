<template>
  <v-app dark>

    <AppBar />
    <Hero />
    <DemoContact2 />
    <v-content>

      <div class="pb-12">
        <nuxt />
      </div>

      <div>

      </div>
      <!-- <Testimonials /> -->

      <!-- <DemoContact /> -->

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
    DemoContact: () => import("~/components/sections/DemoContact"),
    DemoContact2: () => import("~/components/sections/DemoContact"),
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
