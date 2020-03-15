<template>
  <div>
    <Contact />
  </div>
</template>
<script>
export default {
  components: {
    SectionHeader: () => import("~/components/SectionHeader"),
    Contact: () => import("~/components/sections/Contact")
  }
};
</script>
