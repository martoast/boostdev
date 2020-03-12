<template>
  <div>
    <v-parallax
      height="300"
      src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-1 font-weight-thin mb-4">
            {{ title }}
          </h1>
          <h4 class="subheading">{{ subtitle }}</h4>
        </v-col>
      </v-row>
    </v-parallax>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: "Experts In Ecommerce",
    subtitle: "Specialists in Online Stores that SELL"
  }),
  jsonld() {
    return {
      "@context": "https://schema.org",
      "@type": "Organization",
      "@name": "Boost Development",
      "@contactPoint": {
        "@type": "ContactPoint",
        "@contactType": "customer support",
        "@telephone": "[+1-619-888-5248]",
        "@email": "info@elite-strategies.com"
      },
      "@address": {
        "@type": "PostalAddress",
        "@streetAddress": "900 Linton Blvd Suite 104",
        "@addressLocality": "Delray Beach",
        "@addressRegion": "FL",
        "@postalCode": "33444",
        "@addressCountry": "USA"
      }
    };
  }
};
</script>
