<template>
  <v-app dark>
    <AppBar />
    <PageHeader />

    <v-content>
      <v-container class="pb-12">
        <nuxt />
      </v-container>
      <Demo />
    </v-content>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-title>shit</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <try-it />
    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import AppBar from "~/components/core/AppBar.vue";
import Hero from "~/components/sections/Hero.vue";
import Demo from "~/components/sections/Demo.vue";
import PageHeader from "~/components/PageHeader.vue";

export default {
  components: {
    AppBar,
    Hero,
    Demo,
    TryIt: () => import("~/components/sections/TryIt"),
    PageHeader
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
