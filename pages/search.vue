<template>
  <v-row>
      <template>
        <v-container fluid>
          <v-row>
            <v-col v-for="card in 20" :key="card" :cols="3">
              <product/>
            </v-col>
          </v-row>
        </v-container>
      </template>
  </v-row>
</template>

<script>
import product from '~/components/productcard/card'

export default {
  components: {
    product,
  }
}
</script>

<style></style>
