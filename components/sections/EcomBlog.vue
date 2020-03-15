<template>
  <div>

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
        class="mx-auto"
      >
        <v-row dense>
          <v-col
            v-for="card in cards"
            :key="card.title"
            :cols="card.flex"
          >
            <v-hover v-slot:default="{ hover }">
              <a :href="card.link">
                <v-card
                  class="mx-auto"
                  max-width="400"
                  :elevation="hover ? 16 : 2"
                >
                  <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="card.src"
                  >
                    <v-card-title v-text="card.title"></v-card-title>
                  </v-img>

                  <v-card-subtitle
                    class="pb-0"
                    v-text="card.author"
                  ></v-card-subtitle>

                  <v-card-text class="text--primary">
                    <div>{{card.content}}</div>

                  </v-card-text>

                  <v-card-actions>

                    <v-btn
                      color="orange"
                      text
                    >
                      Read More
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </a>

            </v-hover>

          </v-col>
        </v-row>
      </v-container>
    </v-lazy>
  </div>

</template>
<script>
export default {
  data: () => ({
    isActive: false,
    cards: [
      {
        title: "Magento Vs. Shopify",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src: require("@/assets/shopify-vs-magento.jpg"),
        flex: 6,
        link:
          "https://www.aalpha.net/blog/know-the-difference-between-magento-and-shopify/"
      },
      {
        title:
          "Ecommerce Guide – Introduction & How to Start an Ecommerce Business?",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "Let’s walk down the e-commerce memory lane to get a full understanding of online shopping.  Learn how to improve your eCommerce business with the help of the eCommerce guide... ",
        src: require("@/assets/howtostartecommerce.png"),
        flex: 6,
        link:
          "https://www.paldesk.com/ecommerce-guide-introduction-how-to-start-an-ecommerce-business/"
      },
      {
        title: "Qué es el eCommerce: definición modelos y ventajas",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "hablamos del eCommerce constantemente. Pero ¿qué implica? ¿Cuáles son sus variantes? ¿Qué tecnologías son necesarias para el eCommerce?",
        src: require("@/assets/what-is-ecommerce.jpg"),
        flex: 6,
        link: "https://marketing4ecommerce.mx/que-es-el-ecommerce/"
      },
      {
        title: "25 Ecommerce Tips for 2020",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6,
        link: "https://www.oberlo.com/blog/25-ecommerce-tips"
      }
    ]
  }),
  jsonld() {
    const items = this.cards.map((item, index) => ({
      "@type": "Article",
      position: index + 1,
      item: {
        "@id": item.link,
        headline: item.title,
        alternativeHeadline: "Ecommerce Experts",
        genre: "Ecommerce",
        keywords: "seo sales b2b ecommerce shopify magento",
        wordcount: "1120",
        url: item.link,
        mainEntityOfPage: {
          "@type": "WebPage",
          "@id": "https://google.com/article"
        },
        description: "We love to do stuff to help people and stuff",
        articleBody:
          "You can paste your entire post in here, and yes it can get really really long."
      }
    }));
    return {
      "@context": "http://schema.org",
      "@type": "Article",
      itemListElement: items
    };
  }
};
</script>
