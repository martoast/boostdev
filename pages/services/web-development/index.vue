<template>
  <div>
    <section>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Great Websites Command Attention & Get Found<br />
            </h2>

            <p class="subtitle-1">
              We build user-centric websites increasing the ease of use for visitors to do what it is that brought them there, whether it's learn more about your products, submit an inquiry or make a purchase. We design with purpose with best-in-class SEO and UX optimization.
            </p>
            <p class="mb-5">
              Praesent porttitor, nulla vitae posuere iaculis, arcu nisl
              dignissim dolor, a pretium mi sem ut ipsum. Donec mollis hendrerit
              risus. Donec vitae sapien ut libero venenatis faucibus. In hac
              habitasse platea dictumst. Donec quam felis, ultricies nec,
              pellentesque eu, pretium quis, sem.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
              to="/contact"
            >
              Contact Us
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card class="hidden-sm-and-down">
              <v-img
                src="https://media-exp1.licdn.com/dms/image/C4D22AQEslxxFTNKWtg/feedshare-shrink_1280/0?e=1586995200&v=beta&t=ekMx0AU5zNltnIlwEjfa3uGgAxLT07HnMkF0cMXmiA8"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <WebDevSamples />
    </section>
    <section class="pt-12">
      <SectionHeader
        header="Example Work"
        sub-header="360 Renders"
      />
      <v-container pt-9>
        <div>
          <iframe
            allowfullscreen="true"
            title="panorama"
            scrolling="no"
            width="100%"
            height="700"
            src="https://kuula.co/share/7lcgK/collection/7fyMs"
            style="border: 0px;"
          ></iframe>
        </div>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="(highlight, i) in highlights"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="mx-n3"
              color="transparent"
              flat
            >
              <v-card-title v-text="highlight" />
              <v-card-text>
                Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Fusce id purus. Proin faucibus arcu quis ante. Nulla consequat massa quis enim. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Fusce a quam.
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
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
              <v-icon
                size="64"
                class="mb-3"
                v-text="icon"
              />
              <div
                class="display-2 font-weight-bold mb-2"
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
    <section>
      <WebDevBlog />
    </section>
  </div>
</template>
<script>
import WebDevSamples from "~/components/sections/WebDevSamples";
import WebDevBlog from "~/components/sections/WebDevBlog";
import SectionHeader from "~/components/SectionHeader";
export default {
  layout: "webdevLayout",
  head() {
    return {
      title: "Web Development in Tijuana",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Web Development Services in Tijuana."
        }
      ]
    };
  },

  components: { WebDevSamples, WebDevBlog, SectionHeader },

  data: () => ({
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
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
