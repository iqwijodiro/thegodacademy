<template>
  <section class="contact path">
    <v-container>
      <div class="text__wrapper font-light text-center">
        <h2 class="section__title">Contáctanos</h2>
        <h3 class="text__special mt-2">Y con gusto te atenderemos</h3>
      </div>
      <v-row>
        <v-col cols="12" md="6">
          <v-card
            flat
            class="d-flex flex-column justify-center align-center pa-12"
          >
            <v-icon size="80" color="#766eff" class="mb-8">
              mdi-email-outline
            </v-icon>
            <h4 class="card__title">Email</h4>
            <p class="text__mid">We will reply you as soon as possible</p>
          </v-card>
        </v-col>
        <v-col cols="12" md="6"></v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.contact.path {
  background-color: #232323;
  min-height: 70vh;
}
</style>
