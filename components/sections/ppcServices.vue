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
          title: "Google Search Ads",
          route: "/services/seo/onpage",
          text:
            "We help you capture direct, qualified traffic from Google Search Network with well-optimized ads that stand out in search engine results pages."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "Google Shopping Ads",
          text:
            "We have expertise in helping eCommerce businesses promote their products to the right audiences at a lower cost. Learn those tweaks that get people to fill their shopping carts."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "Google Remarketing Services",
          text:
            "Intelligent retargeting keeps your brand on top of your customers’ minds and boosts ROI of your PPC campaign. We help you with the right setup and budget distribution."
        }
      ]
    };
  }
};
</script>
