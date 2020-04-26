<template>
  <div>
    <v-row align="center">
      <VuetifyLogo />
      <h5 class="ml-6">Copyright © 2020 Peninsula. All rights reserved <br> 615-915-1541 · Terms and Conditions / Privacy Policy</h5>

    </v-row>

  </div>

</template>
<script>
import VuetifyLogo from "~/components/VuetifyLogo.vue";
export default {
  components: {
    VuetifyLogo
  }
};
</script>

<style>
.shit {
  width: 180px;
  height: 90px;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
