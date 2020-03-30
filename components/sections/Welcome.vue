<template>
  <section id="welcome">

    <v-container
      :pt-5="$vuetify.breakpoint.mdAndUp"
      px-0
      pb-0
    >
      <!-- <v-img
        max-width="600"
        height="400"
        class="mx-auto"
        :class="$vuetify.breakpoint.mdAndUp ? 'mb-5' : ''"
        contain
        src="https://www.jing.fm/clipimg/detail/40-408123_software-development-clipart-identity-application-maintenance.png"
      /> -->

      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <v-row
            class="pa-0 ma-0 text-center text-sm-left"
            justify="center"
            tag="section"
          >
            <v-col>
              <v-icon
                :color="feature.color"
                size="56"
                v-text="feature.icon"
              />
            </v-col>
            <v-col
              cols="12"
              md="10"
            >
              <h3
                class="title font-weight-regular mb-3 mt-2"
                v-text="feature.header"
              />
              <p
                class="body-1 font-weight-light"
                v-text="feature.text"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    features: [
      {
        icon: "mdi-cellphone-link",
        color: "blue-grey",
        header: "Responsive",
        text:
          "Whether it's desktop, tablet or mobile, your application will just work, right out of the box."
      },
      {
        icon: "mdi-account-multiple",
        color: "indigo",
        header: "Dedicated account manager for each account",
        text: "Tdf"
      },
      {
        icon: "mdi-material-design",
        color: "teal",
        header: "On-staff experts in marketing, design & development",
        text:
          "Built with Material Design, each component is built to scale. Smooth interface across all screen sizes."
      },
      {
        icon: "mdi-chart-bar",
        color: "red lighten-2",
        header: "Clear and concise reporting",
        text:
          "Our team of experts will design the perfect UI for your application."
      },
      {
        icon: "mdi-trophy-variant",
        color: "yellow",
        header: "Proven Performance",
        text:
          "Feel confident in the life-span of your product with major version long-term support."
      },
      {
        icon: "mdi-google",
        color: "red",
        header: "Elite partner status with Google, Facebook and more",
        text:
          "Is your store or web app not getting any traffic? Optimizing for Google ranking factors is essential in the success of any online presence."
      }
    ]
  })
};
</script>
