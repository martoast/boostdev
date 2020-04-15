<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="Explore our SEO strategy"
          header="Need SEO Services to Scale Inbound Lead Gen?"
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
          icon: "mdi-account-group-outline",
          title: "On-page Optimization",
          route: "/services/seo/onpage",
          text: "Boost traffic and grow organic rankings."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/keywords",
          title: "Targeted Keyword Research",
          text: "The very foundation of your digital marketing strategy."
        },
        {
          icon: "mdi-cellphone-link",
          route: "/services/seo/content",
          title: "SEO Content Writing",
          text: "Compelling, well-optimized content."
        },
        {
          icon: "mdi-cellphone-link",
          route: "/services/seo/linkbuilding",
          title: "Trusted Link Building & PR",
          text: "Link building powered by a 12-point quality checklist."
        },
        {
          icon: "mdi-cellphone-link",
          route: "/services/seo/pagespeed",
          title: "Page Speed",
          text: "Optimize the performance of your website."
        },
        {
          icon: "mdi-cellphone-link",
          route: "/services/seo/localseo",
          title: "Local SEO",
          text:
            "Dominate local search and consistently outrank your competition."
        }
      ]
    };
  }
};
</script>
