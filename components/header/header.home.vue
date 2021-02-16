<template>
  <div>
    <v-app-bar color="yellow lighten-1" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer></v-spacer>
      <v-toolbar-title>{{ title }}</v-toolbar-title>
      <v-spacer />
      <v-col cols="12" md="5">
        <v-text-field
          flat
          hide-details
          solo
          label="Search "
          placeholder="search"
        ></v-text-field>
      </v-col>
      <v-btn
          flat
          color="yellow lighten-1"
          hide-details
          @click="search()"
          solo>
          <v-icon>mdi-yeast</v-icon>
        </v-btn>
      <v-menu
        offset-y
        origin="center center"
        class="elelvation-1"
        transition="scale-transition"
      >
        <template>
          <v-btn icon text slot="activator" v-on="on">
            <v-badge color="red" overlap>
              <span slot="badge">3</span>
              <v-icon medium>mdi-bell</v-icon>
            </v-badge>
          </v-btn>
        </template>
      </v-menu>
      <v-menu offset-y origin="center center" transition="scale-transition">
        <template v-slot:activator="{ on }">
          <v-btn icon large text slot="activator" v-on="on">
            <v-avatar size="30px">
              <img :src="'https://cdn.vuetifyjs.com/images/lists/2.jpg'" :alt="'username'" />
            </v-avatar>
          </v-btn>
        </template>
      </v-menu>
    </v-app-bar>
    <sidemenu :drawer="drawer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      searching: false,
      drawer: true,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'LOgo',
    }
  },
  methods:{
     async search() { 
          this.$router.push(`/search`);
    },
    }

}
</script>

<style></style>
