<template>
  <div>
    <SectionHeader
      header="Find out the latest News!"
      sub-header="Latest in Paid Advertizing"
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
                    height="200px"
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
        title: "Pay per Click Guide",
        author: "By Susana Galvano - May 21, 2019",
        content:
          "The terms PPC includes text-format, banner display, or video format advertisements...",
        src: require("@/assets/PPC3.jpg"),
        flex: 6,
        link: "https://www.wordstream.com/pay-per-click"
      },
      {
        title: "How Does Pay-Per-Click (PPC) Work on Google?",
        author: "By Dan Baum - February 18th, 2019",
        content:
          "The first goal for every inbound marketer is to get their site to rank high on Google’s search engine results pages (SERPs)... ",
        src: require("@/assets/ppc.jpg"),
        flex: 6,
        link:
          "https://www.impactbnd.com/blog/how-does-pay-per-click-work-on-google"
      },
      {
        title: "PPC vs. SEO: What's Best For Your Business?",
        author: "By Jason Parks - Abril 12, 2018",
        content:
          "A question we frequently receive is, Should I invest in PPC or SEO?",
        src: require("@/assets/what-is-ecommerce.jpg"),
        flex: 6,
        link: "https://www.entrepreneur.com/article/311355"
      },
      {
        title: "Pay-Per-Click Marketing: Everything You Need to Know About PPC",
        author: "By Ana Gotter - December 28, 2018",
        content:
          "To understand the concept of Magento and Shopify platforms better, let us analyze this example:",
        src: require("@/assets/ppc2.jpg"),
        flex: 6,
        link:
          "https://www.disruptiveadvertising.com/ppc/pay-per-click-ppc-marketing/"
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
