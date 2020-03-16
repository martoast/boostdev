<template>
  <div>
    <SectionHeader
      header="Example Pages"
      sub-header="Sample Landing Pages"
    />
    <v-card class="mx-auto">

      <v-container fluid>
        <v-row dense>
          <v-col
            v-for="card in items"
            :key="card.title"
            cols=6
          >
            <v-card>
              <v-img
                :src="card.src"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                max-height="600px"
              >
                <v-card-title v-text="card.title"></v-card-title>
              </v-img>

            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>

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
          src: require("~/assets/eazypos.png")
        },
        {
          src: require("~/assets/ferrominio.png")
        },
        {
          src: require("~/assets/construction.png")
        },
        {
          src: require("~/assets/delacosta.png")
        }
      ]
    };
  }
};
</script>
