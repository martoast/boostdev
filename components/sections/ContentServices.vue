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
          title: "Boost organic traffic and growth",
          route: "/services/seo/onpage",
          text:
            "Brands that produce content regularly benefit from constantly growing traffic and organic rankings in search results while staying cost-efficient."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "An exciting avenue for growth",
          text:
            "According to DemandMetric research, content generates 3x more leads than traditional marketing but costs 62% less. Traditional advertising isn’t even close."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "Keep up with the industry's trends",
          text:
            "According to CMI, 93% of B2B marketers rely on content, rather than paid acquisition, to build trust with their audience, engage, sell and stay on top of their customers’ minds."
        }
      ]
    };
  }
};
</script>
