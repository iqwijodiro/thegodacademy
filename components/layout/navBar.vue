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
      class="pt-3"
    >
      <v-container>
        <v-row class="d-flex justify-space-between align-center">
          <v-toolbar-title>
            <nuxt-link to="/">
              <v-img
                :src="require('~/assets/images/logo-brand.png')"
                max-width="140"
                min-width="50"
              />
            </nuxt-link>
          </v-toolbar-title>
        </v-row>
      </v-container>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style lang="scss" scoped></style>
