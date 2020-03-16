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

        </v-col>
      </v-row>
    </v-parallax>

    <v-parallax
      height="300"
      src="https://images-na.ssl-images-amazon.com/images/I/11zGghjmy%2BL._SX355_.jpg"
    >
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          class="text-center"
          cols="12"
        >
          <h1 class="display-1 font-weight-thin mb-4">Great Websites Command Attention & Get Found</h1>
          <p>We build user-centric websites increasing the ease of use for visitors to do what it is that brought them there, whether it's learn more about your products, submit an inquiry or make a purchase. We design with purpose with best-in-class SEO and UX optimization.</p>

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
