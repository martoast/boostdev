<template>
  <div>
    <section>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              We help Ecommerce companies drive more business.<br />
            </h2>

            <p class="subtitle-1">
              Shopify, WordPress, BigCommerce, Magento, WooCommerce, Wix,
              Squarespace and more – we can work with eCommerce platforms of
              your choice.
            </p>
            <p class="mb-5">
              Our goal is to set you up with an actionable plan on how to
              increase online sales coming from organic search. This is exactly
              what will help your store thrive in the long term.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
              to="/contact"
            >
              Contact Us
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card class="hidden-sm-and-down">
              <v-img
                src="https://www.aalpha.net/wp-content/uploads/2020/03/magento-gif.gif"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section>
      <DemoContact />
    </section>

    <section>
      <EcommerceServices />
    </section>

    <!-- <section>
      <Features2 />
    </section> -->
    <section>
      <EcomFeatures />
    </section>

    <section>
      <EcommerceVideoSheet />
    </section>

    <section>
      <Blog />
    </section>
  </div>
</template>
<script>
import Blog from "~/components/sections/EcomBlog.vue";
import Features2 from "~/components/sections/Features2.vue";
import EcomFeatures from "~/components/sections/EcomFeatures.vue";
import EcommerceServices from "~/components/sections/EcommerceServices.vue";
import DemoContact from "~/components/sections/DemoContact.vue";
import EcommerceVideoSheet from "~/components/sections/EcommerceVideoSheet.vue";
export default {
  head() {
    return {
      title: "Ecommerce Services in Tijuana",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Ecommerce and CRM services in Tijuana"
        }
      ]
    };
  },
  metaInfo() {
    return {
      title: ""
    };
  },
  layout: "ecommerce",

  components: {
    Blog,
    EcomFeatures,
    Features2,
    DemoContact,
    EcommerceServices,
    EcommerceVideoSheet
  },

  data: () => ({
    experiences: [
      ["mdi-vuejs", "Vue"],
      ["mdi-vuetify", "Vuetify"],
      ["mdi-aws", "AWS"],
      ["mdi-server-security", "Security"]
    ]
  }),

  computed: {},
  jsonld() {
    return {
      "@context": "http://schema.org",
      "@type": "Service",
      name: "Boost Development",
      serviceType: "Ecommerce",
      areaServed: [
        {
          "@type": "City",
          name: "Toronto",
          "@id": "https://en.wikipedia.org/wiki/Toronto"
        },
        {
          "@type": "City",
          name: "Aurora",
          "@id": "https://en.wikipedia.org/wiki/Aurora,_Ontario"
        },
        {
          "@type": "City",
          name: "Oshawa",
          "@id": "https://en.wikipedia.org/wiki/Oshawa"
        }
      ],
      audience: "http://www.wikidata.org/entity/Q131524",
      description: "Experts in Ecommerce Stores that SELL!",
      contactPoint: {
        "@type": "ContactPoint",
        contactType: "customer support",
        telephone: "[+1-619-888-5248]",
        email: "info@elite-strategies.com"
      },
      address: {
        "@type": "PostalAddress",
        streetAddress: "900 Linton Blvd Suite 104",
        addressLocality: "Delray Beach",
        addressRegion: "FL",
        postalCode: "33444",
        addressCountry: "USA"
      }
    };
  }
};
</script>
