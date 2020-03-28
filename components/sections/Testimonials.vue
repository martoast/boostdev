<template>
  <div class="pt-12">

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
    <v-container class="hidden-sm-and-down">
      <div class="hidden-sm-and-down">
        <SectionHeader
          header="Testimonials"
          sub-header="Read what some of our clients had to say!"
          text="Boost is trusted by clients internationaly."
        />
      </div>
      <v-row>
        <v-col
          v-for="(testimonial, i) in testimonials"
          :key="i"
          cols="12"
          md="6"
        >
          <testimonial :testimonial="testimonial" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  components: {
    Testimonial: () => import("@/components/Testimonial"),
    SectionHeader: () => import("@/components/SectionHeader"),
    Welcome: () => import("~/components/sections/Welcome")
  },
  data: () => ({
    testimonials: [
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Nancy Swanson",
        title: "President, Springfield Country Club"
      },
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Jason Schraiber",
        title: "Mayor, Boca Raton"
      }
    ],
    highlightedTestimonial: {
      blurb:
        "The complexities and challenges AlphaConstruction successfully overcame on our behalf includes substantial permit obstacles, coordination and selection support of all design and finish materials, and the diffculty of integrating existing and new structures.",
      person: "Joe Malonagi",
      title: "General Manager, Springfield Tower"
    }
  })
};
</script>
