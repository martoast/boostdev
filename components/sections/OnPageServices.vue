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
          title: "Full-range SEO",
          route: "/services/seo/onpage",
          text:
            "On-site SEO optimization is just one part of the equation. We maximize its impact by delivering other core SEO services: content creation, link building, PR and social media management."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "First-class SEO team",
          text:
            "We closely monitor SEO trends and search engines’ updates and know what it takes to rank high in SERPs. Our website SEO services are adequately changing to keep up with new trends and techniques for the benefits of your business."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "ROI-focused SEO optimization",
          text:
            "We build a well-though-out on-site SEO optimization plan for the long term and prioritize queries that will make all the difference to your bottom line. This approach maximizes the impact of our SEO effort on your sales and revenue."
        }
      ]
    };
  }
};
</script>
