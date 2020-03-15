<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'rgba(13, 3, 29, .95)'"
    :flat="!isScrolling"
    app
  >
    <VuetifyLogo />

    <v-spacer />

    <v-toolbar-items>
      <v-btn
        href="#try-it"
        text
        to="/contact"
        dark
      >
        Contact Us
      </v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    VuetifyLogo
  },
  data: () => ({
    isScrolling: false
  }),

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
