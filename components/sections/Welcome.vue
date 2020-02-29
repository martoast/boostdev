<template>
  <section id="welcome">
    <section-header
      header="Welcome"
      sub-header="No Front-end Experience Required"
      text="Find out why Vuetify is the #1 Material Library for the Vue Framework."
    />

    <v-container
      :pt-5="$vuetify.breakpoint.mdAndUp"
      px-0
      pb-0
    >
      <v-img
        max-width="600"
        height="400"
        class="mx-auto"
        :class="$vuetify.breakpoint.mdAndUp ? 'mb-5' : ''"
        contain
        src="/static/welcome-monitor.png"
      />

      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <v-row
            class="pa-0 ma-0 text-center text-sm-left"
            justify="center"
            tag="section"
          >
            <v-col>
              <v-icon
                :color="feature.color"
                size="56"
                v-text="feature.icon"
              />
            </v-col>
            <v-col
              cols="12"
              md="10"
            >
              <h3
                class="title font-weight-regular mb-3 mt-2"
                v-text="feature.header"
              />
              <p
                class="body-1 font-weight-light"
                v-text="feature.text"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
  export default {
    data: () => ({
      features: [
        {
          icon: 'mdi-cellphone-link',
          color: 'blue-grey',
          header: 'Responsive',
          text: "Whether it's desktop, tablet or mobile, your application will just work, right out of the box."
        },
        {
          icon: 'mdi-cogs',
          color: 'indigo',
          header: 'Customizable',
          text: 'Each component comes packed full of customization features that allow you to handle any use-case.'
        },
        {
          icon: 'mdi-material-design',
          color: 'teal',
          header: 'UI Kit',
          text: 'Built with Material Design, each component is built precisely to match the specification.'
        },
        {
          icon: 'mdi-brush',
          color: 'red lighten-2',
          header: 'Design',
          text: 'Easily built a custom designed application from the ground up, no prior experience required.'
        },
        {
          icon: 'mdi-widgets',
          color: 'deep-purple accent-4',
          header: 'Long-term Support',
          text: 'Feel confident in the life-span of your product with major version long-term support.'
        },
        {
          icon: 'mdi-forum',
          color: 'green',
          header: 'Support',
          text: 'Stuck? Take advantage of our active community full of developers just like you.'
        }
      ]
    })
  }
</script>
