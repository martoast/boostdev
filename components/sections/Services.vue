<template>
  <div>
    <SectionHeader
      header="Services"
      sub-header="Areas of focus"
      text="Find the right solution for you."
    />

    <v-container
      fluid
      class="mx-auto pt-6 pb-6"
    >
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :to="card.route"
              :elevation="hover ? 16 : 2"
            >

              <v-img
                :src="card.src"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="300px"
              >
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out white darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%;"
                  >

                  </div>
                </v-expand-transition>
                <v-card-title v-text="card.title"></v-card-title>
              </v-img>

            </v-card>
          </v-hover>

        </v-col>
      </v-row>
    </v-container>

  </div>

</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    cards: [
      {
        title: "SEO",
        route: "spa",
        src:
          "https://www.milesweb.in/blog/wp-content/uploads/2017/05/seo-hosting-know-hosting-can-affect-websites-seo.png",
        flex: 6
      },
      {
        title: "Enterprice Software",
        route: "enterprice",
        src:
          "https://baktmarketing.com/wp-content/uploads/2019/12/web-development-services-1024x684.jpg",
        flex: 6
      },

      {
        title: "E-commerce",
        route: "ecommerce",
        src:
          "https://www.acumensoftwaredesign.com/wp-content/uploads/2018/06/acumen-magento-1024x518.png",
        flex: 6
      },
      {
        title: "Custom Web Development",
        route: "webapp",
        src:
          "https://www.montanabranding.com/wp-content/uploads/2017/04/montana-custom-website-development-web-developer-agency.jpg.png",
        flex: 6
      }
    ]
  })
};
</script>
