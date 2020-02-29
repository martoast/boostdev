<template>
  <section
    id="try-it"
    class="grey lighten-3 px-3"
  >
    <SectionHeader
      header="Check it out"
      sub-header="Get Started Today"
      text="Sign up for free and become one of the millions of people around the world who have fallen in love with TheSaaS."
    />

    <v-card
      outlined
      class="pa-4 mx-auto"
      max-width="500"
    >
      <v-form>
        <v-text-field
          outlined
          label="Name"
        />
        <v-text-field
          outlined
          label="Email"
        />
        <v-btn
          color="success"
          block
          depressed
          large
          tile
        >
          Sign up
        </v-btn>
      </v-form>
    </v-card>
  </section>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  }
};
</script>
