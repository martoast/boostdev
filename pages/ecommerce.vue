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
              We use the best platforms around!<br />
            </h2>

            <p class="subtitle-1">
              Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec
              vitae orci sed dolor rutrum auctor. Proin pretium, leo ac
              pellentesque mollis, felis nunc ultrices eros, sed gravida augue
              augue mollis justo. Lorem ipsum dolor sit amet, consectetuer
              adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy
              id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu
              pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum
              ullamcorper mauris at ligula.
            </p>
            <p class="mb-5">
              Praesent porttitor, nulla vitae posuere iaculis, arcu nisl
              dignissim dolor, a pretium mi sem ut ipsum. Donec mollis hendrerit
              risus. Donec vitae sapien ut libero venenatis faucibus. In hac
              habitasse platea dictumst. Donec quam felis, ultricies nec,
              pellentesque eu, pretium quis, sem.
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
      <EcomFeatures />
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="([icon, number, name], i) in experiences"
            :key="i"
            cols="6"
            md="3"
          >
            <div class="text-center">
              <v-icon
                size="64"
                class="mb-3"
                v-text="icon"
              />
              <div
                class="display-2 font-weight-bold mb-2"
                v-text="number"
              />
              <div
                class="text-uppercase"
                v-text="name"
              />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section>
      <Blog />
    </section>
  </div>
</template>
<script>
import Blog from "~/components/sections/EcomBlog.vue";
import EcomFeatures from "~/components/sections/EcomFeatures.vue";
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

  components: { Blog, EcomFeatures },

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
