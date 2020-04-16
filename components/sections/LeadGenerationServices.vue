<template>
  <div>
    <section id="features" class="grey lighten-3 pt-8">
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
            <v-card class="py-8 px-4" color="grey lighten-5" flat>
              <v-theme-provider dark>
                <div>
                  <v-avatar color="primary" size="88">
                    <v-icon large v-text="icon"></v-icon>
                  </v-avatar>
                </div>
              </v-theme-provider>

              <v-card-title
                class="justify-center font-weight-black text-uppercase"
                v-text="title"
              ></v-card-title>

              <v-card-text class="subtitle-1" v-text="text"> </v-card-text>
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
          title: "Lead generation campaigns",
          route: "/services/leadgeneration",
          text:
            "Boost will Setup a lead generation campaign on your behalf after understanding your complete business model."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/web-development",
          title: "Streamline Sales Funnel",
          text:
            "The traffic that is generated from your campaign will land on the landing pages that are designed by our dedicated developers and designers."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo",
          title: "SEO Ranking",
          text:
            "Probably the most important aspect of successfully selling product is how you position it. Regardless of how good your product is, the top ranking products on google will generate the most sales."
        }
      ]
    };
  }
};
</script>
