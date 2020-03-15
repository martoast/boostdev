<template>
  <v-card
    max-width="400"
    class="mx-auto"
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

            <v-item v-slot:default="{ active, toggle }">
              <v-card>
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

                <v-card-subtitle class="pb-0">{{item.position}}</v-card-subtitle>

              </v-card>

            </v-item>
          </v-col>
        </v-row>
      </v-item-group>
    </v-container>
  </v-card>
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
      },
      {
        name: "Alex Martos",
        src: "https://cdn.vuetifyjs.com/images/john.jpg",
        position: "CEO and BOSS man",
        content: ""
      }
    ],
    selected: []
  })
};
</script>
<style scoped>
.rounded-card {
  border-radius: 50px;
}
</style>
