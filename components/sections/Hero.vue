<template>
  <v-img
    v-if="namespace"
    height="100vh"
    src="https://cdn.pixabay.com/photo/2016/03/27/18/54/technology-1283624_960_720.jpg"
    class="white--text"
    gradient="to top, rgba(13, 3, 29, .85), rgba(25, 25, 38, .85)"
  >
    <v-container fill-height>
      <v-row
        align="center"
        class="pt-5 px-3"
      >
        <v-sheet
          color="transparent"
          dark
          max-width="500"
        >
          <h1
            class="mb-4"
            :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'"
          >
            Boost Development
          </h1>

          <p class="title font-weight-light">
            Briging your projects to reality using the most powerfull <strong>open source</strong> Frameworks.
          </p>

          <div class="py-4" />

          <v-row
            class="ma-0"
            justify="center"
            justify-md="start"
          >
            <v-btn
              class="mr-md-3 my-2"
              color="white"
              href="#pricing"
              large
              min-width="175"
              outlined
              rounded
              @click.prevent="$vuetify.goTo('#pricing')"
            >
              Learn More
            </v-btn>

            <v-btn
              class="text--primary my-2"
              color="white"
              href="#try-it"
              large
              min-width="175"
              rounded
              @click.prevent="$vuetify.goTo('#try-it')"
            >
              Sign up
            </v-btn>
          </v-row>
        </v-sheet>
      </v-row>
    </v-container>
  </v-img>
</template>

<script>
export default {
  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
