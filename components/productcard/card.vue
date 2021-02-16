<template>
  <v-card 
    :loading="loading"
    class="mx-auto my-12 mr-5 text-xs-center"
    max-width="250"
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <nuxt-link :to="{ path: `/productdetail`}">
    <v-img
      link
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>
    </nuxt-link>
    <v-card-title>Cafe Badilico</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ml-4">
          4.5 (413)
        </div>
      </v-row>

      <div class="my-4 subtitle-1">
        $ • Italian, Cafe
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card-actions>
       <v-btn
        class="ma-2"
        color="orange darken-2"
      >
        <v-icon
          dark
          left
        >
          mdi-cart
        </v-icon>ADD
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
    }),

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    //  async productdetail() { 
    //       this.$router.push(`/productdetail`);
    // },
    },
  }
</script>

<style></style>
