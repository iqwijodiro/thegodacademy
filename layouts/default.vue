<template>
  <v-app>
    <nav-bar />
    <v-main class="ma-0 px-0">
      <Nuxt />
    </v-main>
    <my-footer />
  </v-app>
</template>

<script>
import NavBar from '~/components/layout/navBar'
import MyFooter from '~/components/layout/MyFooter'
export default {
  name: 'DefaultLayout',
  components: {
    NavBar,
    MyFooter,
  },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<style lang="scss" scoped>
body {
  background-color: #000;
}
</style>
