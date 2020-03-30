<template>
  <div>
    <section
      id="features"
      class=" px-3 pt-12"
    >
      <SectionHeader
        header="Features"
        sub-header="The Last UI Kit You'll Ever Need"
        text="With regular updates, dedicated support and an armada of components, there is a solution to any problem."
      />
      <div>
        <v-container
          id="highlighted-testimonial"
          class="pt-5 px-0 mb-n3"
          fluid
          tag="section"
        >

          <v-parallax
            contain
            src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
          >

            <v-overlay
              absolute
              class="px-3"
              opacity=".8"
            >

              <Welcome />
            </v-overlay>
          </v-parallax>
        </v-container>

      </div>

    </section>

  </div>

</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";

export default {
  components: {
    SectionHeader,
    Welcome: () => import("~/components/sections/Welcome")
  },
  data: () => ({
    isActive: false,
    features: [
      {
        src:
          "https://image.freepik.com/free-vector/programmer-working-computer_23-2147505689.jpg",
        header: "Easy to get started",
        text:
          "Maecenas vestibulum mollis diam. Etiam feugiat lorem non metus. Fusce pharetra convallis urna. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Duis leo. Phasellus accumsan cursus velit. Curabitur a felis in nunc fringilla tristique. Phasellus a est. Vestibulum dapibus nunc ac augue. Vestibulum facilisis, purus nec pulvinar iaculis, ligula mi congue nunc, vitae euismod ligula urna in dolor."
      },
      {
        src:
          "https://apps.shopifycdn.com/listing_images/f4a2a9d2237d6f9b289e9e427f6e3d82/key_benefit/4b0a488080d377ffd4f17a7528d59e00.png?height=240&width=320",
        header: "SEO Infrastructure",
        text:
          "Maecenas vestibulum mollis diam. Etiam feugiat lorem non metus. Fusce pharetra convallis urna. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Duis leo. Phasellus accumsan cursus velit. Curabitur a felis in nunc fringilla tristique. Phasellus a est. Vestibulum dapibus nunc ac augue. Vestibulum facilisis, purus nec pulvinar iaculis, ligula mi congue nunc, vitae euismod ligula urna in dolor."
      },
      {
        src:
          "https://cdn.pixabay.com/photo/2016/10/16/16/33/dual-screen-1745705_960_720.png",
        header: "Scalable Applications",
        text:
          "Maecenas vestibulum mollis diam. Etiam feugiat lorem non metus. Fusce pharetra convallis urna. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Duis leo. Phasellus accumsan cursus velit. Curabitur a felis in nunc fringilla tristique. Phasellus a est. Vestibulum dapibus nunc ac augue. Vestibulum facilisis, purus nec pulvinar iaculis, ligula mi congue nunc, vitae euismod ligula urna in dolor."
      }
    ]
  }),
  jsonld() {
    const items = this.features.map((item, index) => ({
      "@type": "ListItem",
      position: index + 1,
      item: {
        "@id": item.src,
        name: item.header,
        description: item.text
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
