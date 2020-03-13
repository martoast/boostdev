<template>
  <div>
    <section>
      <v-container>
        <v-row>
          <v-col cols="12" md="6">
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Bringing world class Shopping to Tijuana<br />
            </h2>

            <p class="subtitle-1">
              The meta description tag serves the function of advertising copy.
              It draws readers to a website from the SERP, and thus is a very
              visible and important part of search marketing. Crafting a
              readable, compelling description using important keywords can
              improve the click-through rate for a given webpage. To maximize
              click-through rates on search engine result pages, it's important
              to note that Google and other search engines bold keywords in the
              description when they match search queries. This bold text can
              draw the eyes of searchers, so you should match your descriptions
              to search terms as closely as possible.
            </p>
            <p class="mb-5">
              Praesent porttitor, nulla vitae posuere iaculis, arcu nisl
              dignissim dolor, a pretium mi sem ut ipsum. Donec mollis hendrerit
              risus. Donec vitae sapien ut libero venenatis faucibus. In hac
              habitasse platea dictumst. Donec quam felis, ultricies nec,
              pellentesque eu, pretium quis, sem.
            </p>

            <v-btn outlined color="primary" class="px-5" large>
              Read More
            </v-btn>
          </v-col>
          <v-col cols="12" md="5" offset-md="1">
            <v-card>
              <v-img src="https://picsum.photos/510/300?random" height="500">
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <SeoFeatures />
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="([icon, number, name], i) in experiences"
            :key="i"
            cols="6"
            md="3"
          >
            <div class="text-center">
              <v-icon size="64" class="mb-3" v-text="icon" />
              <div class="display-2 font-weight-bold mb-2" v-text="number" />
              <div class="text-uppercase" v-text="name" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section>
      <SeoBlog />
    </section>
  </div>
</template>
<script>
import SeoFeatures from "~/components/sections/SeoFeatures.vue";
import SeoBlog from "~/components/sections/SeoBlog.vue";
export default {
  metaInfo() {
    return {
      title: "Boost Development SEO",
      content: "Experts in SEO and SERP"
    };
  },
  layout: "service",

  components: { SeoFeatures, SeoBlog },

  data: () => ({
    experiences: [
      ["mdi-vuejs", "Vue"],
      ["mdi-vuetify", "Vuetify"],
      ["mdi-aws", "AWS"],
      ["mdi-server-security", "Security"]
    ]
  }),

  computed: {}
};
</script>
