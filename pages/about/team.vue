<template>
  <div>
    <SectionHeader
      header="Services"
      sub-header="Areas of focus"
      text="Find the right solution for you."
    />
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
