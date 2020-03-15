<template>
  <div>
    <Contact />
  </div>
</template>
<script>
export default {
  layout: "contactLayout",
  components: {
    SectionHeader: () => import("~/components/SectionHeader"),
    Contact: () => import("~/components/sections/Contact")
  },
  metaInfo: {
    title: "Contact Us",
    meta: [
      {
        name: "description",
        content: "Countact us today!"
      }
    ]
  },
  jsonld() {
    return {
      "@context": "http://schema.org",
      "@type": "Coporation",
      LegalName: "Boost Media inc",
      description: "Experts in Ecommerce Stores that SELL!",
      url: "https://www.boostmediainc.com",
      logo: "LOGO URL HERE",
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
  }
};
</script>
