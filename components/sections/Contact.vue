<template>
  <section
    id="contact"
    class="py-5"
  >
    <!-- <SectionHeader
      header="Work with Boost"
      sub-header="Contact Us"
    /> -->

    <v-container>
      <v-row>
        <v-col
          xs12
          md6
        >
          <Netlify />
        </v-col>

        <v-col
          cols="12"
          md="6"
        >
          <v-container
            fluid
            pa-0
          >
            <v-row>
              <v-col
                cols="12"
                md="6"
                class="pa-0"
              >
                <v-card-title>Mailing Address</v-card-title>
                <v-card-text>
                  <div>2620 Amternest Parkway</div>
                  <div>El Paso TX 79938</div>
                  <div>United States</div>
                </v-card-text>
              </v-col>

              <v-col
                cols="12"
                md="6"
                class="pa-0"
              >
                <v-card-title>Contact Info</v-card-title>
                <v-card-text>
                  <div>+1 (321) 383-4531</div>
                  <div>
                    <a href="#">contact@alphaconstruction.com</a>
                  </div>
                  <div>
                    <a href="#">@alphaconstruction</a>
                  </div>
                </v-card-text>
              </v-col>

              <v-col cols="12">
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6996653.320726327!2d-104.56654057311077!3d31.100430144601546!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x864070360b823249%3A0x16eb1c8f1808de3c!2sTexas!5e0!3m2!1sen!2sus!4v1563207206020!5m2!1sen!2sus"
                  width="100%"
                  height="400"
                  frameborder="0"
                  style="border:0"
                  allowfullscreen
                />
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
import Netlify from "~/components/sections/netlify-form.vue";
export default {
  data() {
    return {
      select: null,
      items: [
        "Ecommerce",
        "Website",
        "SEO",
        "Marketing",
        "Everything digial!",
        "Idk, lets talk."
      ]
    };
  },

  components: {
    SectionHeader,
    Netlify
  }
};
</script>
