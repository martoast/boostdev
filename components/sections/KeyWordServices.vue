<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="SEO Keyword Research Services"
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
          title: "SEO keyword research",
          route: "/services/seo/onpage",
          text:
            "We dive deep into your niche to uncover queries your target audience uses. We identify high-volume and long-tail keywords, analyze your competition and the industry content to compile a list of queries that will convert."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "Keyword mapping",
          text:
            "We match your business keywords with your website’s landing pages and blog content to build a robust SEO and keyword architecture. We identify missing assets and help you create and weave them into your website’s structure."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "Keyword tracking",
          text:
            "We monitor your rankings and organic growth on an ongoing basis. A full and empowering picture of your positions in search across the board. Taking SEO action has never been so easy."
        }
      ]
    };
  }
};
</script>
