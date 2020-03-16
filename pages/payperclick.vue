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
              Start Generating More Leads Today!<br>

            </h2>

            <p class="subtitle-1">
              Pay per click advertising can be intimidating at first, but PPC marketing is an incredible way to attract traffic, leads and sales. PPC can put you in front of audiences who are actively trying to find products and services just like yours, as well as audiences who had no idea that products like yours existed.
            </p>
            <p class="mb-5">
              Pay-per-click (PPC) is an online marketing method to drive traffic to websites where advertisers pay publishers such as Google, Yahoo!, Facebook when the ad is clicked by users.
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

            <v-img
              :src='require("@/assets/PPC-Pay-Per-Click.png")'
              height="500"
            >

            </v-img>

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
    <section>
      <PPCBlog />
    </section>
  </div>
</template>
<script>
import PPCBlog from "~/components/sections/PPCBlog";
export default {
  layout: "ppcLayout",

  head() {
    return {
      title: "Paid Digital Advertizing in Tijuana",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Pay per Click Advertizing Services in Tijuana"
        }
      ]
    };
  },

  components: { PPCBlog },

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
