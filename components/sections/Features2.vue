<template>
  <div>
    <section
      id="features"
      class="grey lighten-3"
    >

      <v-container class="text-center">
        <SectionHeader
          header="Included with each service"
          sub-header="What you can expect from us"
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
              >
              </v-card-text>
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
          title: "Dedicated account manager for each client",
          text:
            "We recognize that as a business owner you do not have time to study the best Digital marketing strategies for your businesss. That is why we assing a dedicated expert to guide you through every step of the way to your online success."
        },
        {
          icon: "mdi-chart-line",
          title: "Clear and concise reporting",
          text:
            "Every month we provide you with easy to understand reporting on the status of the strategy we are exhecuting. You will know exactly what has been worked on and how it has impacted your online precense."
        },
        {
          icon: "mdi-cellphone-link",
          title: "Cross platform optimized",
          text:
            "Our team of trained software engineers will build you a platform that is optimized for all platforms and screen sizes. We build you a platform equipt to maximize your outreach and drive up sales."
        }
      ]
    };
  }
};
</script>
