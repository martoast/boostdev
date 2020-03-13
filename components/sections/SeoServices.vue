<template>
  <section
    id="services"
    class="py-5"
  >

    <v-container>
      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
        >
          <v-card outlined>
            <v-img
              src="https://www.lyfemarketing.com/blog/wp-content/uploads/2018/06/online-reputation-management-strategy.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            flat
            color="transparent"
          >
            <v-card-title>Reputation Management</v-card-title>

            <v-card-text>
              With 88% of consumers researching online before they buy - and consulting more than ten sources on average - it pays to make sure what they find is favorable to your brand.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
          order-md="2"
        >
          <v-card outlined>
            <v-img
              src="https://www.seocompetitors.com/wp-content/uploads/2019/10/regional-seo-services.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            color="transparent"
            flat
          >
            <v-card-title>Local & Regional SEO</v-card-title>

            <v-card-text>
              <p>
                Lorem ipsum dolor sit amet, ea mutat tation constituam per, mei error ocurreret definiebas ne. Te harum constituto inciderint his. Vis no delenit mediocritatem. His et debet possim perpetua, assum argumentum ne quo, constituto eloquentiam sea ne. Ne has ludus graecis fabellas.
              </p>

              <p>
                Ei est iriure partiendo, ius falli tritani accumsan ad, mea altera eripuit fierent ut. Te quem legere fastidii ius. Ei vis quod qualisque, ignota nemore cotidieque mea eu. Scripta labitur ei vel, mei case quidam corpora no, est dico sale utroque ne. Eu erroribus delicatissimi eum, ut quem veri tincidunt vim.
              </p>

              <p>
                Velit eruditi an est, cu eius graeci sed. Vel ei dolorem sapientem temporibus. No his omnes meliore maiestatis, mei iisque molestiae gubergren ex. Usu placerat liberavisse et, eam dicta blandit evertitur an. Ea vim fabellas indoctum maiestatis.
              </p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
        >
          <v-card outlined>
            <v-img
              src="https://www.roastbrief.com.mx/wp-content/uploads/2019/01/roastbrief-que-es-el-link-building-y-como-sacarle-provecho-para-tu-estrategia-seo-780x346.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            flat
            color="transparent"
          >
            <v-card-title>Link Building & Acquisition</v-card-title>

            <v-card-text>
              <p>
                Te dolor consul mei, etiam molestie indoctum usu ad, qui inermis eleifend an. Pro iriure alienum incorrupte ex, cu diceret moderatius mei. Te corrumpit posidonium sit, in cum nonumy utamur. Usu impedit patrioque vituperatoribus ei, cu voluptua nominati philosophia mel. Sea at legendos percipitur, nulla dicant convenire ne duo. Veniam epicuri vis cu, ea pri alii ceteros fierent.
              </p>
              <p>
                Te dolor consul mei, etiam molestie indoctum usu ad, qui inermis eleifend an. Pro iriure alienum incorrupte ex, cu diceret moderatius mei. Te corrumpit posidonium sit, in cum nonumy utamur. Usu impedit patrioque vituperatoribus ei, cu voluptua nominati philosophia mel. Sea at legendos percipitur, nulla dicant convenire ne duo. Veniam epicuri vis cu, ea pri alii ceteros fierent.
              </p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row
        align="center"
        justify="center"
        class="py-5 px-3"
      >
        <!-- <Testimonial :testimonial="testimonial" /> -->
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  metaInfo: {
    title: "Services",
    meta: [
      {
        name: "description",
        content: "Customized vue-cli templates for Vue and Vuetify"
      }
    ]
  },

  components: {
    Testimonial: () => import("@/components/Testimonial")
  },

  data: () => ({
    testimonial: {
      blurb:
        "With Alpha Construction managing all of our customer-facing services and ASCC, helping us monitor and understand building performance, Abocado is in great shape to create and release new products.",
      person: "Jay Oakrson",
      title: "CEO Abocado"
    }
  })
};
</script>
