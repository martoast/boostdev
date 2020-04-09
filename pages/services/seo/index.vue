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
              Your dedicated <strong>SEO</strong> agency that stops at nothing to drive you truly qualified organic traffic.<br />
            </h2>

            <p class="subtitle-1">
              At Boost, we develop SEO programs that maximize your visibility. Our campaigns stand out from the crowd through savvy content development and strategic link-building efforts. We leverage insights from paid search partners (including our own colleagues) to develop data-driven organic search strategies, but we know that only actionable SEO plans actually deliver results. That’s why we also maintain close communication with our clients’ extended network of partners, to keep everyone working together towards the goal of maximum web visibility.
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
                src="https://www.goldenservicesgroup.com/wp-content/uploads/2017/09/Google_Search_Page_Display.png"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section>
      <SeoServices />
    </section>

    <!-- <section>
      <SeoBlog />
    </section> -->
  </div>
</template>
<script>
import SeoFeatures from "~/components/sections/SeoFeatures.vue";
import SeoBlog from "~/components/sections/SeoBlog.vue";
import SeoServices from "~/components/sections/SeoServices.vue";
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

  layout: "seoLayout",

  components: { SeoFeatures, SeoBlog, SeoServices },

  data: () => ({}),

  computed: {}
};
</script>
