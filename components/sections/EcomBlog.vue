<template>
  <v-card class="hidden-sm-and-down">
    <v-container fluid class="mx-auto">
      <v-row dense>
        <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
          <v-hover v-slot:default="{ hover }">
            <v-card :elevation="hover ? 16 : 2">
              <a :href="card.link">
                <v-img
                  :src="card.src"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="350px"
                  :href="card.link"
                >
                  <v-card-title v-text="card.title"></v-card-title>
                  <v-expand-transition>
                    <div
                      v-if="hover"
                      class="d-flex transition-fast-in-fast-out white darken-2 v-card--reveal display-3 white--text"
                      style="height: 100%;"
                    ></div>
                  </v-expand-transition>
                </v-img>
              </a>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Magento Vs. Shopify",
        src: require("@/assets/shopify-vs-magento.jpg"),
        flex: 6,
        link:
          "https://www.aalpha.net/blog/know-the-difference-between-magento-and-shopify/"
      },
      {
        title: "Ecommerce Intro Guide",
        src: require("@/assets/howtostartecommerce.png"),
        flex: 6,
        link:
          "https://www.paldesk.com/ecommerce-guide-introduction-how-to-start-an-ecommerce-business/"
      },
      {
        title: "Best airlines",
        src: require("@/assets/what-is-ecommerce.jpg"),
        flex: 6,
        link: "https://marketing4ecommerce.mx/que-es-el-ecommerce/"
      },
      {
        title: "25 Ecommerce Tips for 2020",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6,
        link: "https://www.oberlo.com/blog/25-ecommerce-tips"
      }
    ]
  }),
  jsonld() {
    const items = this.cards.map((item, index) => ({
      "@type": "ListItem",
      position: index + 1,
      item: {
        "@id": item.link,
        name: item.title
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
