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
            <h1 class="display-1 font-weight-thin mb-4">SEO Content Link Building Services</h1>
            <h4 class="subheading">Link building services: powered by data & analysis, driven by results</h4>
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
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Link building services: powered by data & analysis, driven by results<br />
            </h2>

            <p class="subtitle-1">
              We earn you backlinks and coverage you won’t get elsewhere. Credible outlets coupled with outstanding linkable content get your brand to the top positions you rightfully deserve. Just give us the details: URLs, anchor text and preferred industry / niche and we’ll do all the heavy lifting. You get weekly updates on the progress of your campaign and have full control at any point.
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
    image: require("~/assets/boostlinkbuilding.png")
  }),

  computed: {}
};
</script>
