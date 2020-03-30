<template>
  <div class="pt-6">
    <SectionHeader
      header="Services"
      sub-header="Areas of focus"
      text="Find the right solution for you."
    />
    <v-lazy
      v-model="isActive"
      :options="{
          threshold: .5
        }"
      min-height="200"
      transition="fade-transition"
    >
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
                    ></div>
                  </v-expand-transition>
                  <v-card-title v-text="card.title"></v-card-title>
                </v-img>
              </v-card>
            </v-hover>
          </v-col>
        </v-row>
      </v-container>
    </v-lazy>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    isActive: false,
    cards: [
      {
        title: "SEO",
        route: "seo",
        src: require("@/assets/seoservice.png"),
        flex: 6
      },
      {
        title: "Pay per Click",
        route: "payperclick",
        src: require("@/assets/enterprice.jpg"),
        flex: 6
      },

      {
        title: "E-commerce",
        route: "ecommerce",
        src: require("@/assets/magento.png"),
        flex: 6
      },
      {
        title: "Custom Web Development",
        route: "web-development",
        src: require("@/assets/webdev.png"),
        flex: 6
      }
    ]
  }),
  jsonld() {
    const items = this.cards.map((item, index) => ({
      "@type": "ListItem",
      position: index + 1,
      item: {
        "@id": item.src,
        name: item.title,
        url: item.src
      }
    }));
    return {
      "@context": "http://schema.org",
      "@type": "BreadcrumbList",
      itemListElement: items
    };
  }
};
</script>
