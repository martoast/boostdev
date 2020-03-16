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
      "@type": "LocalBusiness",
      LegalName: "Boost Media inc",
      name: "Boost Media Inc",
      telephone: "+16198885248",
      priceRange: "700-4500",
      image: "https://imgur.com/ug3zA9V",
      description: "Experts in Ecommerce Stores that SELL!",
      url: "https://www.boostmediainc.com",
      logo: "https://imgur.com/ug3zA9V",
      address: {
        "@type": "PostalAddress",
        streetAddress: "José Clemente Orozco 10093",
        addressLocality: "Tijuana",
        addressRegion: "B.C.",
        postalCode: "22010",
        addressCountry: "MX"
      },
      sameAs: [
        "https://www.facebook.com/boostmediainc",
        "https://www.instagram.com/boostmediainc"
      ]
    };
  }
};
</script>
