<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <!--v-toolbar-title>Page title</v-toolbar-title-->
      <site-title :title="title"></site-title>
    <v-spacer/>
    </v-app-bar>
      <v-navigation-drawer app v-model="drawer">
        <v-slide-item>
          <v-list-item-title class="title">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            Subtext1
          </v-list-item-subtitle>
          <v-list-item-subtitle>
            Subtext2
          </v-list-item-subtitle>
        </v-slide-item>
        <site-menu></site-menu>
      </v-navigation-drawer>
    <v-content>
      <router-view>
      </router-view>
    </v-content>
      <site-footer :footer="footer"></site-footer>
  </v-app>
</template>

<script>
import SiteTitle from '@/views/site/title'
import SiteMenu from '@/views/site/menu'
import SiteFooter from '@/views/site/footer'

export default {
  components: { SiteTitle, SiteMenu, SiteFooter },
  name: 'App',
  data () {
    return {
      drawer: false,
      items: [],
      title: '나의 타이틀입니다.',
      footer: '나의 푸터입니다.'
    }
  }
}
</script>
