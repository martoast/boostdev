<template>
  <div>
    <SectionHeader
      header="Example Pages"
      sub-header="Some of our Work"
    />
    <v-carousel
      :show-arrows="false"
      max-height="800px"
    >
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>

  </div>

</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: { SectionHeader },
  data() {
    return {
      items: [
        {
          src: require("~/assets/artoftravel.png")
        },
        {
          src: require("~/assets/ecommercestore.png")
        },
        {
          src: require("~/assets/store2.png")
        },
        {
          src: require("~/assets/webdev.png")
        }
      ]
    };
  }
};
</script>
