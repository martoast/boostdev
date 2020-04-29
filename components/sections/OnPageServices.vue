<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="SEO Onpage Services"
          header="Mastering Organic Growth"
        />

        <v-row>
          <v-col
            v-for="({ icon, title, route, text }, i) in features"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="py-8 px-4"
              color="grey lighten-5"
              flat
            >
              <v-theme-provider dark>
                <div>
                  <v-avatar
                    color="primary"
                    size="88"
                  >
                    <v-icon
                      large
                      v-text="icon"
                    ></v-icon>
                  </v-avatar>
                </div>
              </v-theme-provider>

              <v-card-title
                class="justify-center font-weight-black text-uppercase"
                v-text="title"
              ></v-card-title>

              <v-card-text
                class="subtitle-1"
                v-text="text"
              >
              </v-card-text>
              <v-btn to="/contact">Talk to an Expert</v-btn>
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
  layout: "services",
  data() {
    return {
      features: [
        {
          icon: "mdi-magnify",
          title: "Website audit",
          route: "/services/seo/onpage",
          text:
            "We investigate website speed, navigation, URL structure, XML sitemaps, mobile performance, crawl errors, redirects and much more to build a full picture of your website performance. We recommend actions to resolve errors and eliminate deficiencies."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "Keyword research",
          text:
            "We conduct detailed keyword research and define core keywords your business should be targeting. We also align these keywords with content assets and pages your website should feature in order to rank for them."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "Backlinks audit",
          text:
            "Quality backlinks have a positive effect on your website’s authority and positions in search. We run a deep backlinks audit to put together your backlink profile and flag low-quality or broken backlinks that threaten your credibility and might result in a penalty from search engines."
        }
      ]
    };
  }
};
</script>
