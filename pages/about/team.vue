<template>
  <div>
    <SectionHeader header="Boost Team" />
    <TeamItemGroup />
  </div>
</template>
<script>
import TeamItemGroup from "~/components/sections/TeamItemGroup";
export default {
  layout: "about",
  components: {
    TeamItemGroup,
    SectionHeader: () => import("~/components/SectionHeader")
  }
};
</script>
