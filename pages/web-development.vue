<template>
  <div>
    <section>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Quality Designs with Lighting Performance<br>

            </h2>

            <p class="subtitle-1">
              We design websites, digital campaigns and social media presences that command attention, inspire engagement and serve the needs of all your visitors. We build digital creative assets that work as seamless extensions of your brand, providing users with an optimal experience across multiple devices that keeps them on your website and drives them to convert.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
              to="/contact"
            >
              Contact Us
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card>
              <v-img
                src="https://picsum.photos/510/300?random"
                height="500"
              >

              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="(highlight, i) in highlights"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="mx-n3"
              color="transparent"
              flat
            >
              <v-card-title v-text="highlight" />
              <v-card-text>
                Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Fusce id purus. Proin faucibus arcu quis ante. Nulla consequat massa quis enim. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Fusce a quam.
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="([icon, number, name], i) in experiences"
            :key="i"
            cols="6"
            md="3"
          >
            <div class="text-center">
              <v-icon
                size="64"
                class="mb-3"
                v-text="icon"
              />
              <div
                class="display-2 font-weight-bold mb-2"
                v-text="number"
              />
              <div
                class="text-uppercase"
                v-text="name"
              />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>
<script>
export default {
  layout: "webdevLayout",
  metaInfo() {
    return {
      title: ""
    };
  },

  components: {},

  data: () => ({
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
    experiences: [
      ["mdi-vuejs", "Vue"],
      ["mdi-vuetify", "Vuetify"],
      ["mdi-aws", "AWS"],
      ["mdi-server-security", "Security"]
    ]
  }),

  computed: {}
};
</script>
