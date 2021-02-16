<template>
<div>
  <banner/>
   <v-row class="mt-5">
    <v-col>
        <template>
          <slider />
          <slider />
          <slider />
        </template>
    </v-col>
  </v-row>
</div>
</template>

<script>


import banner from '~/components/banner/banner'
import slider from '~/components/slider/slider'
export default {
  components: {
    slider,
    banner,
  }
}
</script>

<style></style>
