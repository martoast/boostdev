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
            <h1 class="display-1 font-weight-thin mb-4">Keyword Optimization</h1>
            <h4 class="subheading">Rank higher, faster with Boost SEO</h4>
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
          sub-header="Advanced SEO keyword research services tailored to your business needs."
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
              Your dedicated <strong>SEO</strong> agency that stops at nothing to drive you truly qualified organic traffic.<br />
            </h2>

            <p class="subtitle-1">
              At Boost, We build the very foundation of your digital marketing strategy by identifying a unique set of keywords your business must be laser-targeting. Advanced SEO keyword research services tailored to your business needs.
            </p>
            <p class="mb-5">
              Our proven, repeatable SEO optimization process results in a strong and meaningful action plan to land your website high in organic search results. We streamline your SEO efforts and help you focus on the right marketing goals.
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
      <DemoContact />
    </section>

    <section>
      <KeyWordServices />
    </section>
    <section>

      <VideoSheet />
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
import KeyWordServices from "~/components/sections/KeyWordServices.vue";
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
    KeyWordServices,
    DemoContact,
    SectionHeader,
    VideoSheet,
    Contact: () => import("~/components/sections/Contact")
  },

  data: () => ({
    image: require("~/assets/keyword.png")
  }),

  computed: {}
};
</script>
