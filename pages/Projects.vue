<template>
  <div class="pt-12">
    <WebDevSamples />
    <div>
      <Contact />

    </div>

  </div>

</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
import WebDevSamples from "~/components/sections/WebDevSamples.vue";
import Contact from "~/components/sections/Contact.vue";
export default {
  layout: "services",
  data() {
    return {
      select: null,
      items: [
        "Ecommerce",
        "Website",
        "SEO",
        "Marketing",
        "Everything digial!",
        "Idk, lets talk."
      ]
    };
  },

  components: {
    SectionHeader,
    WebDevSamples,
    Contact
  }
};
</script>
