<template>
  <div>
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
            <v-card-title v-text="highlight.title" />
            <v-card-text v-text="highlight.description">

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
      {
        title: "On-page SEO Optimization",
        description: "Boost traffic and grow organic rankings."
      },
      {
        title: "Targeted Keyword Research",
        description: "The very foundation of your digital marketing strategy."
      },
      {
        title: "SEO Content Writing",
        description: "Compelling, well-optimized content."
      },
      {
        title: "Trusted Link Building & PR",
        description: "Link building powered by a 12-point quality checklist."
      },
      {
        title: "Page Speed",
        description: "Optimize the performance of your website."
      },
      {
        title: "Local SEO",
        description:
          "Dominate local search and consistently outrank your competition."
      }
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
