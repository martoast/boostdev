<template>
  <v-app dark>

    <AppBar />

    <PageHeader />
    <LogoSheet />

    <v-content>
      <div class="pd-12">

      </div>

      <nuxt />

    </v-content>

    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";

import PageHeader from "~/components/PageHeader.vue";
import Contact from "~/components/sections/Contact.vue";
import LogoSheet from "~/components/sections/LogoSheet.vue";

export default {
  components: {
    AppBar,
    Hero,

    Footer: () => import("~/components/core/Footer"),
    PageHeader,
    Contact,
    LogoSheet
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
