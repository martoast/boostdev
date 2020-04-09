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
            <h1 class="display-1 font-weight-thin mb-4">Onpage SEO Optimization</h1>
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
          sub-header="Grow your rankings with on-page SEO services"
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
              On-page SEO services, explained<br />
            </h2>

            <p class="subtitle-1">
              Every time you want your website to rank on page 1 for a particular keyword, on-page SEO comes into play. On-page SEO analysis entails a mix of activities that reveal your website's current position and authority in search as well as highlight avenues for growth. Dominating the online landscape is a task that requires knowledge, skills and commitment – and it's the job we truly mastered.
            </p>
            <p class="mb-5">
              We jumpstart the on-site SEO optimization process by running a comprehensive audit of your website: its quality, structure, content and authority. Next, we identify core business keywords you need to rank for and transform these insights into a fully customized action plan, broken down into high- and medium-priority items, milestones and timeframes. We implement it all: from revising the URL structure and fixing technical issues to optimizing content and anything in between.
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
      <OnPageServices />
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
import OnPageServices from "~/components/sections/OnPageServices.vue";
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
    OnPageServices,
    DemoContact,
    SectionHeader,
    VideoSheet
  },

  data: () => ({
    image: require("~/assets/keyword.png")
  }),

  computed: {}
};
</script>
