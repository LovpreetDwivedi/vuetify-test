<template>
  <v-app>
      <template>
        <headerhome />
      </template>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
      <template>
        <footerhome />
      </template>
  </v-app>
</template>

<script>
import headerhome from '~/components/header/header.home.vue'
import footerhome from '~/components/footer/footer.home.vue'
import sideMenu from '~/components/sidemenu/sidemenu.vue'

export default {
  data() {
    return {}
  },
  components: {
    headerhome,
    footerhome,
    sideMenu
  }
}
</script>
