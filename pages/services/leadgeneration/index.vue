<template>
  <div>
    <section>
      <v-parallax
        dark
        src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
      >
        <v-row align="center" justify="center">
          <v-col class="text-center" cols="12">
            <h1 class="display-1 font-weight-thin mb-4">
              Boost Lead Generation Services
            </h1>
            <h4 class="subheading">
              Lead generation services that fuel your sales pipeline
            </h4>
            <div class="py-2" />
            <v-btn
              class="mr-md-3 my-2"
              color="white"
              large
              min-width="175"
              outlined
              rounded
              to="/about/"
            >
              Learn More
            </v-btn>

            <v-btn
              class="text--primary my-2"
              color="white"
              large
              min-width="175"
              rounded
              href="tel: +1 (619) 888-5258"
            >
              <v-icon class="pa-2">mdi-phone-outgoing</v-icon>
              CALL NOW
            </v-btn>
          </v-col>
        </v-row>
      </v-parallax>
    </section>

    <section>
      <v-container>
        <div class="py-2" />
        <SectionHeader
          sub-header="Trusted Link Building Services"
          header="Mastering Organic Growth"
        />
        <v-row>
          <v-col cols="12" md="6">
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Need to Scale Inbound Lead Gen?
            </h2>

            <p class="subtitle-1">
              The foundation of our lead generation services is data predictive
              analysis driven by data. Our performance is the result of a
              strategy crafted around your target audience, search engine
              optimization strategies and your ROI.
            </p>
            <p class="mb-5">
              The <strong>Boost Lead Generation Service</strong> is designed to
              help you generate business from the internet while you pay only
              for every lead that is generated through our activities. Our Lead
              generation campaigns are designed to give you value for money
              while you focus on your core business.
            </p>

            <v-btn outlined color="primary" class="px-5" large to="/contact">
              Contact Us
            </v-btn>
          </v-col>
          <v-col cols="12" md="5" offset-md="1">
            <v-card class="hidden-sm-and-down">
              <v-img :src="this.image" height="500"> </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <LeadGenerationServices />
    </section>
    <section>
      <DemoContact />
    </section>
    <section>
      <LeadGenerationVideoSheet />
    </section>
    <section>
      <Contact />
    </section>

    <!-- <section>
      <SeoBlog />
    </section> -->
  </div>
</template>
<script>
import SeoFeatures from "~/components/sections/SeoFeatures.vue";
import SeoBlog from "~/components/sections/SeoBlog.vue";
import ContentServices from "~/components/sections/ContentServices.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import VideoSheet from "~/components/sections/VideoSheet.vue";
export default {
  head() {
    return {
      title: "#1 SEO Service in Tijuana",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Professional SEO services in Tijuana"
        }
      ]
    };
  },

  layout: "services",

  components: {
    SeoFeatures,
    SeoBlog,
    ContentServices,
    DemoContact,
    SectionHeader,
    LeadGenerationVideoSheet: () =>
      import("~/components/sections/LeadGenerationVideoSheet"),
    Contact: () => import("~/components/sections/Contact"),
    LeadGenerationServices: () =>
      import("~/components/sections/LeadGenerationServices")
  },

  data: () => ({
    image: require("~/assets/leadgeneration.jpg")
  }),

  computed: {}
};
</script>
