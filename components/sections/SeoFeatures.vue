<template>
  <div>
    <v-container>
      <v-row>
        <v-col v-for="(highlight, i) in highlights" :key="i" cols="12" md="4">
          <v-card class="mx-n3" color="transparent" flat>
            <v-card-title v-text="highlight.title" />
            <v-card-text>
              Vestibulum ante ipsum primis in faucibus orci luctus et ultrices
              posuere cubilia Curae; Fusce id purus. Proin faucibus arcu quis
              ante. Nulla consequat massa quis enim. Aenean tellus metus,
              bibendum sed, posuere ac, mattis non, nunc. Fusce a quam.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data: () => ({
    highlights: [
      { title: "PWA Technology", description: "asdgasdgasdfgadsfg" },
      { title: "Structured Data", description: "asdgasdgasdfgadsfg" },
      { title: "Google Page Speed", description: "asdgasdgasdfgadsfg" },
      { title: "Key Words Optimization", description: "asdgasdgasdfgadsfg" },
      { title: "Server Side Rendering", description: "asdgasdgasdfgadsfg" },
      { title: "Backend hardening", description: "asdgasdgasdfgadsfg" }
    ]
  }),
  jsonld() {
    const items = this.highlights.map((item, index) => ({
      "@type": "ListItem",
      position: index + 1,
      item: {
        "@id": item.title,
        name: item.title
      }
    }));
    return {
      "@context": "http://schema.org",
      "@type": "BreadcrumbList",
      itemListElement: items
    };
  }
};
</script>
