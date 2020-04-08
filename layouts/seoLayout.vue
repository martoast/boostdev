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
          <h1 class="display-1 font-weight-thin mb-4">Search Engine Optimization (SEO)</h1>
          <h4 class="subheading">Rank Higher, Faster with Boost SEO.</h4>
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
    <LogoSheet />

    <!-- <v-parallax
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
          <h1 class="display-1 font-weight-thin mb-4">Dominate Your Vertical's Share of Voice</h1>
          <h4 class="subheading">Our agency gets your brand in front of consumers with
            comprehensive, holistic SEO services - including website optimization,
            content strategy, and web presence management.</h4>

        </v-col>
      </v-row>
    </v-parallax> -->

    <v-content>

      <v-container class="pb-12">

        <nuxt />
      </v-container>

    </v-content>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">

          <v-list-item-title>shit</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import Contact from "~/components/sections/Contact.vue";
import LogoSheet from "~/components/sections/LogoSheet.vue";
import Footer from "~/components/core/Footer.vue";

export default {
  components: {
    AppBar,
    Hero,
    DemoContact,
    TryIt: () => import("~/components/sections/TryIt"),
    Contact,
    Footer,
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
