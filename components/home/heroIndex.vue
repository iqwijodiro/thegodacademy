import myBtn from '~/components/buttons/myBtn.vue';
<template>
  <section class="hero d-flex justify-center align-end pb-12">
    <v-container class="pb-10 mb-10">
      <v-row>
        <v-col cols="12" md="5">
          <v-card flat color="transparent">
            <h1 class="hero__title mb-3">The God Academy</h1>
            <p class="hero__subtitle mb-3">Un lugar para conocer más a Dios</p>
            <v-card-actions class="mx-n2 px-0">
              <my-btn
                text="Quiero Formarme"
                destiny="/courses"
                btn-type="primary"
                class="ma-2"
              />
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import myBtn from '../buttons/myBtn.vue'
export default {
  components: { myBtn },
}
</script>

<style lang="scss" scoped>
.hero {
  min-height: 100vh;
  background-image: url(../../assets/images/hero_bg.webp);
  background-size: cover;
  background-position: 50% 50%;
  .hero__title {
    line-height: 1.1;
  }
  .hero__subtitle {
    font-size: 1.2rem;
    line-height: 1.5;
  }
}
</style>
