<template>
  <div>
    <section id="home" class="pa-0">
      <welcome />

      <services />

      <features />

      <!-- <try-it /> -->
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      charset: "utf-8",
      title: "Digital Marketing Tijuana",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content: "Digital Marketing and SEO in Tijuana"
        }
      ]
    };
  },
  jsonld() {
    return {
      "@context": "http://schema.org",
      "@type": "LocalBusiness",
      LegalName: "Boost Media inc",
      name: "Boost Media Inc",
      telephone: "+16198885248",
      priceRange: "700-4500",
      description: "Experts in Ecommerce Stores that SELL!",
      url: "https://www.boostmediainc.com",
      logo: "https://imgur.com/ug3zA9V",
      address: {
        "@type": "PostalAddress",
        streetAddress: "900 Linton Blvd Suite 104",
        addressLocality: "Delray Beach",
        addressRegion: "FL",
        postalCode: "33444",
        addressCountry: "USA"
      },
      sameAs: ["https://www.facebook.com/boostmediainc"]
    };
  },

  components: {
    Demo: () => import("~/components/sections/Demo"),
    Features: () => import("~/components/sections/Features"),
    Services: () => import("~/components/sections/Services"),
    Testimonials: () => import("@/components/sections/Testimonials"),

    Pricing: () => import("~/components/sections/Pricing"),
    TryIt: () => import("~/components/sections/TryIt"),
    Welcome: () => import("~/components/sections/Welcome")
  },

  data: () => ({
    items: ["/static/server-parallax.png"],
    testimonials: [
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Nancy Swanson",
        title: "President, Springfield Country Club"
      },
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Jason Schraiber",
        title: "Mayor, Boca Raton"
      }
    ]
  }),

  computed: {
    cardFeatures() {
      return [];
    },
    listFeatures() {
      return [];
    }
  }
};
</script>
