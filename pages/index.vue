<template>
  <div>
    <section
      id="home"
      class="pa-0"
    >

      <About />
      <!-- <Features /> -->
      <Features2 />

      <Stats />
      <DemoContact2 />

      <services />
      <div>
        <SectionHeader sub-header="Contact Us" />
      </div>
      <!--
          <div
        >
          <SectionHeader
            header="Boost Team"
            sub-header="Meet our Team"
            text="At Boost we have built a strong core team of experts ready to help your business take full advantage of digital verticles."
          />
          <TeamItemGroup />
      </div> -->

      <!-- <features /> -->

      <!-- <try-it /> -->
      <About2 />
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
      image: "https://imgur.com/ug3zA9V",
      description: "Data Driven, Results Oriented Digital Marketing.",
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
  },

  components: {
    Demo: () => import("~/components/sections/Demo"),
    Features: () => import("~/components/sections/Features"),
    Services: () => import("~/components/sections/Services"),
    Testimonials: () => import("@/components/sections/Testimonials"),
    About: () => import("@/components/sections/About"),
    Features: () => import("@/components/sections/Features"),
    About2: () => import("@/components/sections/About2"),
    Features2: () => import("@/components/sections/Features2"),
    Stats: () => import("@/components/sections/Stats"),
    DemoContact2: () => import("~/components/sections/DemoContact"),
    TeamItemGroup: () => import("~/components/sections/TeamItemGroup"),
    SectionHeader: () => import("~/components/SectionHeader"),

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
