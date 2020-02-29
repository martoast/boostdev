<template>
  <v-footer
    absolute
    app
    class="elevation-12"
    height="88"
  >
    <v-container
      class="py-0"
      fluid
    >
      <v-row
        align="center"
        class="fill-height"
        justify="start"
      >
        <div>
          <v-img src="/static/alpha-software-logo-dark.png" />
        </div>
        <v-spacer class="d-none d-md-block" />
        <div class="caption pr-md-12">
          &copy;2019. All rights reserved
        </div>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    computed: {
      categories () {
        return []
      }
    }
  }
</script>
