<template>
  <v-app dark>

    <AppBar />

    <PageHeader />

    <v-content>
      <v-container class="pb-12">
        <nuxt />
      </v-container>
      <DemoContact />
    </v-content>

    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import PageHeader from "~/components/PageHeader.vue";
import Contact from "~/components/sections/Contact.vue";

export default {
  components: {
    AppBar,
    Hero,
    DemoContact,
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
