<template>
  <div>
    <v-app-bar
      v-scroll="onScroll"
      color="rgba(13, 3, 29, .95)"
      :flat="!isScrolling"
      app
    >
      <VuetifyLogo />

      <v-spacer />
      <div class="hidden-md-and-up">
        <v-toolbar-items>
          <v-btn
            to="/contact"
            dark
            color="success"
            class="mr-12"
          >
            Contact Us
          </v-btn>
          <v-icon
            @click.stop="drawer = !drawer"
            dark
          >mdi-menu</v-icon>
        </v-toolbar-items>
      </div>
      <div class="hidden-sm-and-down">
        <v-toolbar-items>
          <v-btn
            v-for="(item, i) in items"
            :key="i"
            :active-class="!isScrolling ? 'primary--text' : undefined"
            :to="item.to"
            text
            dark
          >
            <span v-text="item.text" />
          </v-btn>
        </v-toolbar-items>
      </div>
    </v-app-bar>
    <div>
      <v-navigation-drawer
        v-model="drawer"
        :right="right"
        temporary
        fixed
        src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
      >
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="title">
                Boost Media Inc
              </v-list-item-title>
              <v-list-item-subtitle>
                Digital Marketing
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-divider></v-divider>
          <v-list-item
            v-for="item in Menuitems"
            :key="item.title"
            link
          >
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </div>
  </div>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    VuetifyLogo
  },
  data: () => ({
    isScrolling: false,

    clipped: false,
    drawer: false,
    fixed: false,
    miniVariant: false,
    right: true,
    rightDrawer: false,
    title: "Vuetify.js",
    Menuitems: [
      { title: "Home", icon: "mdi-home-city", to: "/" },
      { title: "SEO", icon: "dashboard", to: "/services/seo/" },
      {
        title: "Web Development",
        icon: "dashboard",
        to: "/services/web-development/"
      },
      { title: "E-commerce", icon: "dashboard", to: "/services/ecommerce/" },
      {
        title: "Paid Advertizing",
        icon: "dashboard",
        to: "/services/payperclick/"
      },
      {
        title: "Social Media",
        icon: "dashboard",
        to: "/services/socialmedia/"
      },
      { title: "Contact Us", icon: "dashboard", to: "/contact" }
    ]
  }),
  computed: {
    items() {
      return [
        {
          to: "/",
          text: "Home"
        },
        {
          to: "/services/",
          text: "Services"
        },
        {
          to: "/projects",
          text: "Projects"
        },
        {
          to: "/contact",
          text: "Contact"
        }
      ];
    }
  },

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
