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
          title: "Premium PR link building",
          route: "/services/seo/onpage",
          text:
            "We earn you first-class placements in top-tier outlets. Exclusive features and mentions of your brand by resources that get millions of readers every month."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "Guest post campaigns",
          text:
            "We handpick a robust selection of outlets with the right balance of domain authority and relevance and produce premium content that organically mentions your brand’s unique expertise."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "White-hat natural placements",
          text:
            "We run targeted outreach campaigns and cooperate with our extensive network of editors, journalists and bloggers to promote your content and earn you excellent mentions and backlinks."
        }
      ]
    };
  }
};
</script>
