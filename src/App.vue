<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <v-toolbar-title>Page title</v-toolbar-title>
    <v-spacer/>
    <v-btn icon to="/about">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>
      <v-navigation-drawer app v-model="drawer">
        test
      </v-navigation-drawer>
    <v-content>
      <router-view>

      </router-view>
    </v-content>
      <v-footer app color="primary" dark absolute>
        <v-spacer></v-spacer>
        <div>&copy; {{ new Date().getFullYear() }}</div>
      </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      drawer: false
    }
  }
}
</script>
