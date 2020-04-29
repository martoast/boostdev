<template>
  <div>
    <section
      id="features"
      class="grey lighten-3"
    >
      <v-container class="text-center">
        <SectionHeader
          header="Boost E-commerce Services"
          sub-header="Industry-leading eCommerce services"
        />

        <v-row>
          <v-col
            v-for="({ icon, title, text }, i) in features"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="py-12 px-4"
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
              > </v-card-text>
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
  data() {
    return {
      features: [
        {
          icon: "mdi-account-group-outline",
          title: "SEO for eCommerce",
          text:
            "We deliver a full-circle eCommerce SEO strategy: from keyword research, website architecture and on-page optimization to content marketing and link building. It’s a comprehensive, granular action plan focused on growing rankings for high-intent keywords."
        },
        {
          icon: "mdi-chart-line",
          title: "High-quality traffic",
          text:
            "Your paid traffic is a faucet that ceases to deliver results as soon as you turn it off. We double down on organic growth that will get you to the top positions  you rightfully deserve, while also adding paid acquisition campaigns to the mix."
        },
        {
          icon: "mdi-cellphone-link",
          title: "eCommerce content",
          text:
            "Content is one of the pillars of SEO for eCommerce websites. From product descriptions to landing pages and blog posts, your website needs to speak to your target audience. We cater to all of your content needs to deliver just that."
        }
      ]
    };
  }
};
</script>
