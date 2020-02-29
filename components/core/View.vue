<template>
  <v-content class="white pt-0">
    <router-view />
  </v-content>
</template>

<script>
  export default {
    metaInfo () {
      return {
        titleTemplate: '%s — Alpha Theme'
      }
    }
  }
</script>
