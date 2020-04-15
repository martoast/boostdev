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
            <h1 class="display-1 font-weight-thin mb-4">Page Speed Optimization Services</h1>
            <h4 class="subheading">Rank higher, with faster a loading speed.</h4>
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
          sub-header="Grow your rankings with Boost SEO page speed services"
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
              The Pagespeed services you need to help you successfully meet your project planning goals and deadline<br />
            </h2>

            <p class="subtitle-1">
              Slow loading website only leads to abandoned shopping carts, higher bounce rates, and lower Google rankings. Google views the loading speed of your web site as one of the most crucial components to a good user experience. So why hesitate, when your chance at better website performance and increased conversions is here.
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
      <ContentServices />
    </section>
    <section>
      <DemoContact />
    </section>
    <section>

      <VideoSheet />
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
    VideoSheet
  },

  data: () => ({
    image: require("~/assets/boostpagespeed.png")
  }),

  computed: {}
};
</script>
