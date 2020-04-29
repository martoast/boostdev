<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="Local SEO Services"
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
          title: "Local SEO strategy",
          route: "/services/seo/onpage",
          text:
            "There’s so much more to local SEO than just listing your company on Google My Business. From locally relevant on-page SEO to neighborhood pages and customer reviews, we put together a comprehensive, actionable strategy for you."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/seo/keywords",
          title: "Hyper-personalized user experience",
          text:
            "A cleverly optimized local website speaks to the needs of customers and turns you into local authority. Our optimization process covers everything from the blog and internal linking to NAP info, long-tail optimization and much more."
        },
        {
          icon: "mdi-chart-line",
          route: "/services/seo/content",
          title: "Drive traffic & sales",
          text:
            "Whether you run a brick-and-mortar store or a digital business, all that matters at the end of the day is qualified traffic that can translate into sales and happy customers. We show you the exact steps to win customers in your area and build a professional presence in search."
        }
      ]
    };
  }
};
</script>
