<template>
  <section
    id="features"
    class=" px-3 pt-12"
  >
    <SectionHeader
      header="Features"
      sub-header="The Last UI Kit You'll Ever Need"
      text="With regular updates, dedicated support and an armada of components, there is a solution to any problem."
    />

    <v-container
      :mt-5="$vuetify.breakpoint.mdAndUp"
      :pt-5="$vuetify.breakpoint.mdAndUp"
      px-0
      pb-0
    >
      <v-row
        v-for="(feature, i) in features"
        :key="i"
        :class="[$vuetify.breakpoint.mdAndUp && 'my-5']"
        align="center"
        :style="{
          flexDirection: $vuetify.breakpoint.mdAndUp && i === 1 ? 'row-reverse' : 'row'
        }"
      >
        <v-col
          cols="12"
          md="6"
          class="hidden-sm-and-down"
        >
          <v-sheet
            max-width="400"
            class="mx-auto"
          >
            <v-img
              width="100%"
              height="300"
              color="grey"
              :src="feature.src"
            />
          </v-sheet>
        </v-col>
        <v-col
          cols="12"
          md="6"
        >
          <h3
            class="headline font-weight-regular mb-3 mt-2"
            v-text="feature.header"
          />
          <p
            class="body-1 font-weight-light"
            v-text="feature.text"
          />
        </v-col>
        <v-col
          v-if="i !== features.length - 1"
          cols="12"
          class="py-5 hidden-sm-and-down"
          order-xs="4"
        >
          <v-divider />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";

export default {
  components: {
    SectionHeader
  },
  data: () => ({
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
  })
};
</script>
