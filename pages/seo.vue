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
              Our agency gets your brand in front of consumers.<br />
            </h2>

            <p class="subtitle-1">
              At Path, we develop SEO programs that maximize your visibility. Our campaigns stand out from the crowd through savvy content development and strategic link-building efforts. We leverage insights from paid search partners (including our own colleagues) to develop data-driven organic search strategies, but we know that only actionable SEO plans actually deliver results. That’s why we also maintain close communication with our clients’ extended network of partners, to keep everyone working together towards the goal of maximum web visibility.
            </p>
            <p class="mb-5">
              Great SEO is collaborative, multi-faceted, and constantly evolving. That's why we build close working relationships with all the crucial stakeholders and agency teams on the client side, from PR to social to paid media to business development, to ensure that our search engine optimization efforts are driven by smart, consistent, and realistically actionable strategies.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
            >
              Read More
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card>
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

    <section>
      <SeoFeatures />
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
      <SeoBlog />
    </section>
  </div>
</template>
<script>
import SeoFeatures from "~/components/sections/SeoFeatures.vue";
import SeoBlog from "~/components/sections/SeoBlog.vue";
import SeoServices from "~/components/sections/SeoServices.vue";
export default {
  head() {
    return {
      title: "Experts in SEO and SERPS",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Boost your website or store to the first page of Google!"
        }
      ]
    };
  },
  metaInfo() {
    return {
      title: "Boost Development SEO",
      content: "Experts in SEO and SERP"
    };
  },
  layout: "service",

  components: { SeoFeatures, SeoBlog, SeoServices },

  data: () => ({
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
