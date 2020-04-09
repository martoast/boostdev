<template>
  <div>
    <section class="grey lighten-3">
      <v-container>

        <SectionHeader
          sub-header="Why Our SEO Keyword Research Services?"
          header="Mastering Organic Growth"
        />
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            cols="12"
            md="5"
            offset-xl="1"
          >

            <div class="ma-12">
              <v-row justify="center">
                <h2 class="mb-4 headline">
                  Our SEO Keyword Research Process<br />
                </h2>

                <p class="subtitle-1">
                  As an SEO and keyword research company, we rely on the industry-leading SEO software to conduct rigorous and detailed keyword research.
                  The tools we work with include Ahrefs, Google Keyword Planner, SEMRush, MozPro and others.
                  We look closely at your competition to identify organic keywords they rank for as well as SEO strategies they implement. We compare how your website stacks up to these strategies and identify areas for improvement.
                </p>

                <v-btn
                  outlined
                  color="#BF9B2A"
                  class="px-5"
                  x-large
                  to="/contact"
                >
                  Contact us
                </v-btn>

              </v-row>

            </div>

          </v-col>

          <v-col
            cols="12"
            md="5"
          >

            <div align="center">
              <v-container>

                <iframe
                  style="top:55px; left:0; bottom:0; right:0; height: 400px; border:none; margin:0; padding:0; z-index:999999;"
                  src="https://player.vimeo.com/video/404896466"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                  width="100%"
                ></iframe>

              </v-container>

            </div>

          </v-col>
        </v-row>
      </v-container>
    </section>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: { SectionHeader },
  data() {
    return {};
  }
};
</script>
