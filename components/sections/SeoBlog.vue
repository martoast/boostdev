<template>
  <v-lazy
    v-model="isActive"
    :options="{
          threshold: .5
        }"
    min-height="200"
    transition="fade-transition"
  >
    <v-card class="mx-auto">
      <v-container fluid>
        <v-row dense>
          <v-col
            v-for="card in cards"
            :key="card.title"
            :cols="card.flex"
          >
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
                    <v-card-subtitle
                      class="pb-0 white--text"
                      v-text="card.author"
                    ></v-card-subtitle>

                    <v-card-text class="white--text--primary">
                      <div>{{card.content}}</div>
                    </v-card-text>

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
  </v-lazy>

</template>
<script>
export default {
  data: () => ({
    isActive: false,
    cards: [
      {
        title: "How Nuxt solves the SEO problems",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src: "https://miro.medium.com/max/4288/1*vqGPNd14IEKABWxpJTfNsw.jpeg",
        flex: 6,
        link:
          "https://blog.logrocket.com/how-nuxt-js-solves-the-seo-problems-in-vue-js/"
      },
      {
        title: "Favorite road trips",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src:
          "https://www.paldesk.com/wp-content/uploads/2019/08/ecommerce-guide-how-to-start-an-ecommerce-business-1024x439.png",
        flex: 6,
        link:
          "https://www.paldesk.com/ecommerce-guide-introduction-how-to-start-an-ecommerce-business/"
      },
      {
        title: "Best airlines",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src:
          "https://s3.amazonaws.com/cdn.wp.m4ecmx/wp-content/uploads/2015/05/31143018/Qu%C3%A9-es-el-eCommerce-compressor.jpg",
        flex: 6,
        link: "https://marketing4ecommerce.mx/que-es-el-ecommerce/"
      },
      {
        title: "Blog post 4",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6,
        link:
          "https://medium.com/vue-mastery/best-practices-for-nuxt-js-seo-32399c49b2e5"
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
        alternativeHeadline: "SEO Experts",
        genre: "seo",
        keywords: "seo sales b2b ecommerce shopify magento development coding",
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
