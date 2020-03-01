<template>
  <section
    id="home"
    class="pa-0"
  >

    <welcome />

    <services />

    <features />

    <pricing />

    <try-it />
  </section>
</template>

<script>
export default {
  metaInfo() {
    return {
      title: ""
    };
  },

  components: {
    Demo: () => import("~/components/sections/Demo"),
    Features: () => import("~/components/sections/Features"),
    Services: () => import("~/components/sections/Services"),

    Pricing: () => import("~/components/sections/Pricing"),
    TryIt: () => import("~/components/sections/TryIt"),
    Welcome: () => import("~/components/sections/Welcome")
  },

  data: () => ({
    items: ["/static/server-parallax.png"]
  }),

  computed: {
    cardFeatures() {
      return [];
    },
    listFeatures() {
      return [];
    },
    testimonials() {
      return [];
    }
  }
};
</script>
