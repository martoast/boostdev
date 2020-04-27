<template>
  <div>
    <v-card
      width="100vh"
      class="mx-auto"
      flat
    >
      <v-container class="pa-1">
        <v-item-group
          v-model="selected"
          multiple
        >
          <v-row>
            <v-col
              v-for="(item, i) in team"
              :key="i"
              cols="12"
              md="6"
            >

              <v-hover
                v-slot:default="{ hover }"
                close-delay="200"
              >
                <v-item v-slot:default="{ active, toggle }">
                  <v-card
                    @click="trigger(item)"
                    flat
                    :elevation="hover ? 16 : 2"
                  >
                    <v-row justify="center">
                      <v-avatar size="150">
                        <img
                          :src="item.src"
                          alt="John"
                          @click="toggle"
                        >
                      </v-avatar>

                    </v-row>

                    <v-card-title>{{item.name}}</v-card-title>

                    <v-card-subtitle>{{item.position}}</v-card-subtitle>

                  </v-card>

                </v-item>
              </v-hover>

            </v-col>
          </v-row>
        </v-item-group>
      </v-container>
    </v-card>
    <div>
      <v-row justify="center">
        <v-dialog
          v-model="dialog"
          max-width="350"
        >

          <v-card>
            <v-row
              justify="center"
              class="pt-6"
            >
              <v-avatar size="150">
                <img :src="this.selected.src">
              </v-avatar>

            </v-row>
            <v-card-title class="headline">{{this.selected.name}}</v-card-title>
            <v-card-subtitle class="pt-1">{{this.selected.position}}</v-card-subtitle>
            <v-card-text>Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.</v-card-text>
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
export default {
  data: () => ({
    team: [
      {
        name: "Alex Martos",
        src: "https://cdn.vuetifyjs.com/images/john.jpg",
        position: "Group Director, SEO & Digital Content",
        content: ""
      },
      {
        name: "Alex Martos",
        src: "https://avatars0.githubusercontent.com/u/9064066?v=4&s=460",
        position: "CEO and BOSS man",
        content: ""
      },
      {
        name: "John Leider",
        src: "https://randomuser.me/api/portraits/men/85.jpg",
        position: "CEO and BOSS man",
        content: ""
      },
      {
        name: "Jane Smith",
        src: "https://randomuser.me/api/portraits/women/81.jpg",
        position: "CEO and BOSS man",
        content: ""
      },
      {
        name: "Sandra Adams",
        src: "https://randomuser.me/api/portraits/women/85.jpg",
        position: "CEO and BOSS man",
        content: ""
      },
      {
        name: "Alex Martos",
        src: "https://cdn.vuetifyjs.com/images/john.jpg",
        position: "CEO and BOSS man",
        content: ""
      }
    ],
    selected: { name: "", src: "", position: "", content: "" },
    dialog: false
  }),
  methods: {
    trigger(item) {
      console.log(item);
      this.dialog = true;
      this.selected.name = item.name;
      this.selected.src = item.src;
      this.selected.position = item.position;
    }
  }
};
</script>
<style scoped>
.rounded-card {
  border-radius: 50px;
}
</style>
