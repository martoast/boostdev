<template>
  <section
    id="demo"
    class="primary darken-2 white--text"
  >
    <v-container>
      <v-row>
        <v-col
          v-for="([icon, number, name], i) in experiences"
          :key="i"
          cols="6"
          md="3"
        >
          <div class="text-center">
            <v-icon
              size="44"
              color="white"
              class="mb-3"
              v-text="icon"
            />
            <div
              class="display-1 font-weight-bold mb-2"
              v-text="number"
            />
            <div
              class="text-uppercase"
              v-text="name"
            />
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {
  data: () => ({
    experiences: [
      ["mdi-vuejs", "Vue"],
      ["mdi-facebook", "Facebook"],
      ["mdi-amazon", "Amazon"],
      ["mdi-google", "Google"]
    ]
  })
};
</script>
