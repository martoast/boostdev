<template>
  <div>

    <div>
      <SectionHeader
        header="Welcome"
        sub-header="Our Business is Growing Yours."
      />
    </div>

    <section class="white">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <h1
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >

              Our full-service web solutions help your business grow online leads, calls, and revenue.

            </h1>

            <p class="display-1 font-weight-light">
              Boost Media is a full-service Internet marketing and SEO company offering innovative web marketing solutions to mid to large size companies across the globe. As a leader in SEO, web design, ecommerce, website conversion, and Internet marketing services,
              our firm prides ourselves on driving traffic, converting visitors, and measuring effectiveness to ultimately deliver real results for our clients.
            </p>

          </v-col>
          <v-col
            cols="12"
            md="6"
          >
            <v-card>
              <v-img
                :src="this.src"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                max-height="450px"
                min-height="300"
              ></v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    src: require("@/assets/grow.png"),
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
    experiences: [
      ["mdi-vuejs", "75", "Vue"],
      ["mdi-vuetify", "100", "Vuetify"],
      ["mdi-aws", "67", "AWS"],
      ["mdi-server-security", "95", "Security"]
    ]
  })
};
</script>
