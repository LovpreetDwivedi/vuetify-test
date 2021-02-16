<template>
  <v-row>
    <v-card class="mt-3">
      <v-col class="text-right">
      <v-btn text color="primary"> View More </v-btn>
    </v-col>
    <v-col>
      <v-slide-group class="pa-4" active-class="success"   show-arrows-on-hover>
        <template v-slot:prev="{ on, attrs }">
      <v-btn
        color="yellow lighten-1"
        fab
        small
        v-bind="attrs"
        v-on="on"
      > <v-icon>mdi-chevron-left</v-icon> </v-btn>
    </template>
    <template v-slot:next="{ on, attrs }">
      <v-btn
        color="yellow lighten-1"
        v-bind="attrs"
        fab
        small
        v-on="on"
      > <v-icon>mdi-chevron-right</v-icon></v-btn>
    </template>
        <v-slide-item v-for="data in 20" :key="data">
          <product class="ma-4" :cardData="{}" />
        </v-slide-item>
      </v-slide-group>
    </v-col>
    </v-card>
  </v-row>
</template>

<script>
import product from '~/components/productcard/card'
export default {
  name: 'slider',
  components: {
    product
  },
  props: {
    data: {
      type: Array,
      required: true,
      default: []
    },
    isViewMore: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style></style>
