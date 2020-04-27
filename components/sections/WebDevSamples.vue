<template>
  <div>
    <SectionHeader
      header="Example Pages"
      sub-header="Check out some of our work!"
    />
    <v-card class="mx-auto">

      <v-container fluid>
        <v-row dense>
          <v-col
            v-for="card in items"
            :key="card.title"
            cols=6
          >
            <v-card @click="trigger(card)">
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
    <div>
      <v-row justify="center">
        <v-dialog v-model="dialog">

          <v-card>
            <v-row
              justify="center"
              class="pt-6"
            >

              <img :src="this.selected.src">

            </v-row>
            <v-card-title class="headline">Title</v-card-title>
            <v-card-subtitle class="pt-1">Subtitle</v-card-subtitle>
            <v-card-text>{{this.selected.description}}</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn
                color="green darken-1"
                text
                @click="dialog = false"
              >Close</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-row>
    </div>

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
          src: require("~/assets/artoftravel.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        },
        {
          src: require("~/assets/ecommercestore.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        },
        {
          src: require("~/assets/eazypos.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        },
        {
          src: require("~/assets/ferrominio.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        },
        {
          src: require("~/assets/construction.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        },
        {
          src: require("~/assets/delacosta.png"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
        }
      ],
      selected: { name: "", src: "", description: "" },
      dialog: false
    };
  },
  methods: {
    trigger(item) {
      console.log(item);
      this.dialog = true;
      this.selected.name = item.name;
      this.selected.src = item.src;
      this.selected.description = item.description;
    }
  }
};
</script>
