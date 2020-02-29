<template>
  <section
    id="pricing"
    class="px-3"
  >
    <section-header
      header="Plans"
      sub-header="Pricing"
      text="Choose any of the following plans to get started with. You can begin with the FREE plan to see our web application at first. You can always change your plan at any time."
    />

    <v-container
      mt-5
      pa-0
    >
      <v-row>
        <v-col
          cols="12"
          class="text-center mb-5"
        >
          <v-btn-toggle
            v-model="frequency"
            rounded
          >
            <v-btn
              max-height="40"
              min-width="50%"
            >
              Monthly
            </v-btn>
            <v-btn
              max-height="40"
              min-width="50%"
            >
              Yearly
            </v-btn>
          </v-btn-toggle>
        </v-col>
        <v-col
          v-for="(plan, i) in plans"
          :key="i"
          cols="12"
          md="4"
        >
          <v-card
            :elevation="i === 1 ? 12 : 0"
            :outlined="i !== 1"
            class="v-card--plan text-center pb-3"
          >
            <v-toolbar
              color="grey lighten-5"
              flat
            >
              <v-spacer />
              <div v-text="plan.name" />
              <v-spacer />
            </v-toolbar>

            <v-row>
              <v-col
                cols="12"
                class="v-card--plan__price pa-5"
              >
                <div
                  :class="i === 1 ? 'success--text' : ''"
                  class="d-inline-block"
                >
                  <sup>$</sup>
                  <span
                    class="display-3 font-weight-bold"
                    v-text="frequency ? plan.yearly : plan.monthly"
                  />
                </div>
                <span class="caption">
                  /{{ frequency ? 'yr' : 'mo' }}
                </span>
              </v-col>
            </v-row>
            <v-card-text class="mb-4">
              <div
                v-for="(feature, j) in plan.features"
                :key="j"
                v-text="feature"
              />
            </v-card-text>
            <v-card-text>
              <v-btn
                :color="i === 1 ? 'success' : 'primary'"
                depressed
                tile
              >
                Get Started
              </v-btn>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
  export default {
    data: () => ({
      frequency: 0,
      plans: [
        {
          name: 'Free',
          monthly: 0,
          yearly: 0,
          features: [
            '100+ Components',
            'Community Support',
            'Unlimited Projects'
          ]
        },
        {
          name: 'Personal',
          monthly: 50,
          yearly: 199,
          features: [
            '100+ Components',
            'Private Support',
            'Unlimited Projects'
          ]
        },
        {
          name: 'Premium',
          monthly: 250,
          yearly: 999,
          features: [
            'Issue Resolution Priority',
            'On-Demand Support',
            'Unlimited Projects'
          ]
        }
      ]
    })
  }
</script>

<style lang="sass">
  .v-card--plan
    &__price
      div
        vertical-align: text-bottom

        > sup
          vertical-align: super

        > span
          vertical-align: middle

        + span
          vertical-align: super
</style>
