<template>
  <v-navigation-drawer
    class="yellow lighten-1"
    v-model="isopendrawer"
    :mini-variant="miniVariant"
    app
    floating
    :permanent="isopendrawer"
  >
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: {
    drawer: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    isopendrawer() {
      return this.drawer
    }
  },
  data() {
    return {
      clipped: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-cart-outline',
          title: 'Cart',
          to: '/cart'
        },
        {
          icon: 'mdi-heart',
          title: 'Wishlist',
          to: '/wishlist'
        }
      ],
      miniVariant: false
    }
  }
}
</script>

<style></style>
