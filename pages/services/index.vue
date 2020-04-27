<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="Explore our Services"
          header="See why Boost Media has the right Digital Marketing solutions for you"
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
              :to="route"
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
              <v-btn>Explore Service</v-btn>
            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
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
          icon: "mdi-google",
          title: "SEO services",
          route: "/services/seo",
          text:
            "Our proven, repeatable SEO optimization process results in a strong and meaningful action plan to land your website high in organic search results."
        },
        {
          icon: "mdi-cellphone-link",
          route: "/services/web-development/",
          title: "Web Development",
          text:
            "While other agencies depend on fixed Website builders and templates that are a pain to customize, at Boost we work with the latest in web development technology to bring our clients the designs that they want to see!"
        },
        {
          icon: "mdi-account-multiple-outline",
          route: "/services/leadgeneration",
          title: "Lead Generation",
          text:
            "The foundation of our lead generation services is data predictive analysis driven by data. Our performance is the result of a strategy crafted around your target audience, search engine optimization strategies and your ROI."
        },
        {
          icon: "mdi-cash",
          route: "/services/ppc",
          title: "Pay per Click",
          text:
            "We help you capture direct, qualified traffic from Google Search Network with well-optimized ads that stand out in search engine results pages."
        },
        {
          icon: "mdi-cart-outline",
          route: "/services/ecommerce",
          title: "E-commerce",
          text:
            "Shopify, WordPress, BigCommerce, Magento, WooCommerce, Wix,Squarespace and more – we can work with eCommerce platforms ofyour choice."
        },
        {
          icon: "mdi-code-tags",
          route: "/services/seo",
          title: "Enterprice Software",
          text:
            "With our SEO services, you can turn on the power of search to maximize your inbound lead gen and scale your revenue and brand to where it belong."
        }
      ]
    };
  }
};
</script>
