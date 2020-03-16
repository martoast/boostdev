<template>
  <div>
    <div class="hidden-sm-and-down">
      <v-footer dark height="auto" padless>
        <v-row class="ma-0">
          <v-col class="py-5 primary darken-2 white--text" cols="12" md="3">
            <h3 class="headline mb-3">
              Boost Media Inc
            </h3>
            <ul class="body-1 pl-0">
              <li v-for="(c, i) in company" :key="i" class="mb-3">
                <a class="transition-swing" v-text="c.title" :href="c.link" />
              </li>
            </ul>
          </v-col>
          <v-col class="blue-grey darken-2 pa-5" cols="12" md="9">
            <v-row>
              <v-col
                v-for="(category, i) in categories"
                :key="i"
                cols="12"
                md="6"
              >
                <v-btn text v-text="category.title" :to="category.link"></v-btn>
              </v-col>
            </v-row>
          </v-col>

          <v-col class="text-center blue-grey darken-4 pa-3" cols="12">
            &copy; 2020 Boost Media Inc — All Rights reserved.
          </v-col>
        </v-row>
      </v-footer>
    </div>
    <div class="hidden-md-and-up">
      <v-footer dark padless>
        <v-card class="flex" flat tile>
          <v-card-title class="teal">
            <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
              <v-icon size="24px">{{ icon }}</v-icon>
            </v-btn>
          </v-card-title>

          <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    categories: [
      { title: "Success Stories", link: "/stories" },
      { title: "Case Studies", link: "/case-studies" },
      { title: "Testimonials", link: "/testimonials" }
    ],
    company: [
      { title: "Services", link: "/services" },
      { title: "Projects", link: "/projects" },
      { title: "Our Team", link: "/about/team" }
    ],
    icons: [
      "mdi-facebook",
      "mdi-twitter",
      "mdi-google-plus",
      "mdi-linkedin",
      "mdi-instagram"
    ]
  })
};
</script>

<style lang="sass">
.v-application .v-footer
  ul
    list-style-type: none

    a
      color: white
      text-decoration: none

      &:hover
        color: grey
</style>
