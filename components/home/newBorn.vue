<template>
  <div class="new-born">
    <section class="next-second">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" md="8">
            <h2 class="section__title-xl text-center mb-8">
              Este próximo segundo cambiará tu vida
            </h2>
            <div class="actions">
              <my-btn color="secondary" text="Un nuevo nacimiento" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="images">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" md="6">
            <div class="image__wrapper">
              <v-img :src="require('~/assets/images/hands.jpeg')" />
              <p class="text__mid text-center my-4">
                Adquiere los Nuestros Ebooks Gratuitos
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="6"></v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import MyBtn from '../buttons/myBtn.vue'
export default { components: { MyBtn } }
</script>

<style lang="scss" scoped>
.new-born {
  background-color: #000;
  min-height: 100vh;
  .section__title-xl {
    font-size: 4.6rem;
    line-height: 1.1;
  }
  .actions {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.6rem 1.2rem;
  }
}
</style>
