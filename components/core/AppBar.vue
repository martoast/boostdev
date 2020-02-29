<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'rgba(13, 3, 29, .95)'"
    :flat="!isScrolling"
    app
    hide-on-scroll
  >
    <v-img
      class="shrink"
      contain
      max-width="50%"
      src="/static/alpha-software-logo.png"
    />

    <v-spacer />

    <v-toolbar-items>
      <v-btn
        href="#try-it"
        text
        @click.prevent="$vuetify.goTo('#try-it')"
      >
        Try It
      </v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";

export default {
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
