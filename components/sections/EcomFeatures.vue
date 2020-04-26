<template>
  <div>
    <v-container>
      <SectionHeader
        header="Included with each service"
        sub-header="What makes us stand out from the rest"
      />
      <v-row>
        <v-col
          v-for="(highlight, i) in highlights"
          :key="i"
          cols="12"
          md="4"
        >
          <v-card
            class="mx-n3"
            color="transparent"
            flat
          >
            <v-card-title v-text="highlight.title" />
            <v-card-text v-text="highlight.description" />

          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: { SectionHeader },
  data: () => ({
    highlights: [
      {
        title: "Mobile Shopping Optimized",
        description:
          "Over the years web development for ecommerce has evolved alot since the introduction of mobile shopping. We team of experts build your store using the lastest technology to ensure you are mobile shopping optimized."
      },
      {
        title: "Full-range SEO for Ecommerce",
        description:
          "We deliver a full-circle eCommerce SEO strategy: from keyword research, website architecture and on-page optimization to content marketing and link building. It’s a comprehensive, granular action plan focused on growing rankings for high-intent keywords."
      },
      {
        title: "All Ecommerce platforms",
        description:
          "Shopify, WordPress, BigCommerce, Magento, WooCommerce, Wix, Squarespace and more – we can work with eCommerce platforms of your choice."
      },
      {
        title: "Evergreen high-quality traffic",
        description:
          "Your paid traffic is a faucet that ceases to deliver results as soon as you turn it off. We double down on organic growth that will get you to the top positions  you rightfully deserve, while also adding paid acquisition campaigns to the mix."
      },
      {
        title: "Well-optimized Ecommerce content",
        description:
          "Content is one of the pillars of SEO for eCommerce websites. From product descriptions to landing pages and blog posts, your website needs to speak to your target audience. We cater to all of your content needs to deliver just that."
      },
      {
        title: "Backend hardening",
        description:
          "Our team of experts have experience building ecommerce stores of all shapes and sizes. We will take care of your backend security, so you can get back to running your business."
      }
    ]
  }),
  jsonld() {
    const items = this.highlights.map((item, index) => ({
      "@type": "ListItem",
      position: index + 1,
      item: {
        "@id": item.title,
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
