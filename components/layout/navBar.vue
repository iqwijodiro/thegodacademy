<template>
  <div id="navbar">
    <v-app-bar
      app
      elevate-on-scroll
      height="95px"
      min-height="70px"
      shrink-on-scroll
      scroll-threshold="500"
      tag="header"
      color="#000"
    >
      <v-container class="d-flex align-center justify-space-between">
        <v-app-bar-nav-icon class="pt-2">
          <nuxt-link to="/">
            <v-img
              :src="require('~/assets/images/logo-brand.png')"
              max-width="100%"
            />
          </nuxt-link>
        </v-app-bar-nav-icon>
        <!-- <v-spacer></v-spacer> -->
        <nav class="nav hidden-sm-and-down transparent">
          <v-row justify="space-around" class="pt-4">
            <!-- <v-col> -->
            <nuxt-link
              v-for="link in links"
              :key="link.title"
              :to="link.url"
              class="nav__link ma-4"
            >
              <h3>{{ link.title }}</h3>
            </nuxt-link>
            <!-- <v-col> -->
            <nuxt-link to="/" class="nav__link ma-4">
              <v-menu dark open-on-hover bottom offset-y>
                <template #activator="{ on, attrs }">
                  <h3 v-bind="attrs" v-on="on">
                    Formación
                    <v-icon color="#fff"> mdi-menu-down </v-icon>
                  </h3>
                </template>
                <v-list class="nav">
                  <v-list-item v-for="(droplink, i) in dropdown" :key="i">
                    <v-list-item-title>
                      <nuxt-link
                        :to="droplink.url"
                        class="nav__link nav__link-drop"
                      >
                        <h3>
                          {{ droplink.title }}
                        </h3>
                      </nuxt-link>
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-menu>
            </nuxt-link>
            <nuxt-link to="/contact" class="nav__link ma-4">
              <h3>Contáctanos</h3>
            </nuxt-link>
            <div class="d-flex justify-center align-center mx-5">
              <my-btn
                text="Ingresar"
                destiny="/login"
                color="primary"
                append-icon="mdi-login-variant"
              />
            </div>
          </v-row>
        </nav>
      </v-container>
    </v-app-bar>
  </div>
</template>

<script>
import myBtn from '~/components/buttons/myBtn.vue'
export default {
  components: { myBtn },
  data() {
    return {
      tabs: false,
      links: [
        {
          title: 'Home',
          url: '/',
        },
        {
          title: 'Nosotros',
          url: '/nosotros',
        },
      ],
      dropdown: [
        {
          title: 'Cursos',
          url: '/courses',
        },
        {
          title: 'Programas',
          url: '/programs',
        },
        {
          title: 'ForGroups',
          url: '/groups',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.nav {
  .nav__link,
  .nav__link.nav__link-drop {
    h3 {
      color: #fff !important;
    }
  }
  .nav__link.nav__link-drop {
    padding: 1rem;
    border-bottom: 1px solid #fff;
  }
}
</style>
