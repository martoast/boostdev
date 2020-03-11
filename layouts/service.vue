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
          <h1 class="display-1 font-weight-thin mb-4">SEO</h1>
          <h4 class="subheading">Google rank your site today!</h4>
        </v-col>
      </v-row>
    </v-parallax>

    <v-content>

      <v-container class="pb-12">

        <nuxt />
      </v-container>
      <Demo />

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
    <try-it />
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import Demo from "~/components/sections/Demo.vue";

export default {
  components: {
    AppBar,
    Hero,
    Demo,
    TryIt: () => import("~/components/sections/TryIt")
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
