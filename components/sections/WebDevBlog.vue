<template>
  <div>
    <SectionHeader
      header="Find out the latest News!"
      sub-header="Latest in Web Development"
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
                  :elevation="hover ? 16 : 2"
                >
                  <v-img
                    class="white--text align-end"
                    max-height="300px"
                    :src="card.src"
                  >

                  </v-img>
                  <v-card-title v-text="card.title"></v-card-title>

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
  components: {
    SectionHeader: () => import("~/components/SectionHeader")
  },
  data: () => ({
    isActive: false,
    cards: [
      {
        title: "React VS Vue: Which is better for 2020?",
        author: "By Patricia Neil - Oct 3, 2019",
        content:
          "Javascript frameworks along with HTML and CSS have become an integral part of the front-end development of every contemporary software project...",
        src: require("@/assets/vuevsreact.png"),
        flex: 6,
        link:
          "https://medium.com/@patricianeil248/react-vs-vue-which-is-better-for-2020-c484f22c67a8"
      },
      {
        title: "32 Tips For Every Web Developer In 2020",
        author: "By Simon Holdorf - May 21, 2019",
        content:
          "2019 is over, and it was a year with a lot of challenges and opportunities for developers like you and me. There’s a lot to learn and master ... ",
        src: require("@/assets/coding.jpeg"),
        flex: 6,
        link:
          "https://medium.com/better-programming/32-tips-for-every-web-developer-in-2020-782fd6554f0d"
      },
      {
        title:
          "7 WordPress tips and best practices to make your sites shine in 2020",
        author: "By Morgan Smith — November 30, 2019",
        content:
          "A new year means a new opportunity to discover WordPress tips and best practices to make your best websites yet!",
        src: require("@/assets/wordpresstips.jpg"),
        flex: 6,
        link:
          "https://getflywheel.com/layout/wordpress-tips-best-practices-2020/"
      },
      {
        title: "A Guide To The Options For WordPress Theme Development",
        author: "By Rachel McCollin - March 13, 2013",
        content:
          " The overriding conclusion from the session was that there isn’t a one-size-fits-all answer and that the best method depends on the needs of the website and the capabilities of the developer...",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6,
        link:
          "https://www.smashingmagazine.com/2013/03/a-guide-to-wordpress-theme-options/"
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
