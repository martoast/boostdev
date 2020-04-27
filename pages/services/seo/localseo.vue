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
            <h1 class="display-1 font-weight-thin mb-4">Boost Local SEO Services</h1>
            <h4 class="subheading">Dominate local search and consistently outrank your competition.</h4>
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
          sub-header="Need a Local SEO Agency to Help You Boost Rankings and Scale Inbound Lead Gen?"
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
              We help you drive digital traffic to your website and foot traffic to your brick-and-mortar location.<br />
            </h2>

            <p class="subtitle-1">
              In this day and age, your brand needs interesting, compelling content to delight and empower your audience. Brands that produce content regularly benefit from constantly growing traffic and organic rankings in search results while staying cost-efficient.
            </p>
            <!-- <p class="mb-5">
              We jumpstart the on-site SEO optimization process by running a comprehensive audit of your website: its quality, structure, content and authority. Next, we identify core business keywords you need to rank for and transform these insights into a fully customized action plan, broken down into high- and medium-priority items, milestones and timeframes. We implement it all: from revising the URL structure and fixing technical issues to optimizing content and anything in between.
            </p> -->

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
      <LocalServices />
    </section>

    <section>

      <LocalVideoSheet />
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
import LocalServices from "~/components/sections/LocalServices.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import LocalVideoSheet from "~/components/sections/LocalVideoSheet.vue";
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
    LocalServices,
    DemoContact,
    SectionHeader,
    LocalVideoSheet,
    Contact: () => import("~/components/sections/Contact")
  },

  data: () => ({
    image: require("~/assets/localseo.jpg")
  }),

  computed: {}
};
</script>
