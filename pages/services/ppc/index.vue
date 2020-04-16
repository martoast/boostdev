<template>
  <div>
    <section>
      <v-parallax
        dark
        src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            class="text-center"
            cols="12"
          >
            <h1 class="display-1 font-weight-thin mb-4">ROI-focused PPC Services</h1>
            <h4 class="subheading">Boost your inbound lead gen with Boost Today!</h4>
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
          sub-header="ROI-focused PPC services"
          header="Mastering Organic Growth"
        />
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Run intelligent, well-optimized PPC campaigns to drive qualified traffic, leads and conversions and put your brand in front of new audiences.
            </h2>

            <p class="subtitle-1">
              As PPC management experts, we have worked with businesses across industries over the past years. SaaS startups, eCommerce and healthcare brands, software developers and many others.We view your PPC campaign as an exercise in lead generation and implement the campaign setup that makes the most of your budget. We’re ROI focused at all stages.
            </p>
            <p class="mb-5">
              We’ve got you covered on all fronts: from keyword research, copywriting and design to campaign setup, budget planning and A/B testing. We’re the one-stop shop destination you can rely on.
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
            <v-card class="hidden-sm-and-down">
              <v-img
                :src="this.image"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <ppcServices />
    </section>
    <section>
      <DemoContact />
    </section>
    <section>

      <ppcVideoSheet />
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
import ppcServices from "~/components/sections/ppcServices.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import ppcVideoSheet from "~/components/sections/ppcVideoSheet.vue";
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
    ppcServices,
    DemoContact,
    SectionHeader,
    ppcVideoSheet,
    Contact: () => import("~/components/sections/Contact")
  },

  data: () => ({
    image: require("~/assets/ppc.jpg")
  }),

  computed: {}
};
</script>
