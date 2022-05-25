<template>
  <section class="welcome bg-dark">
    <v-container>
      <v-row justify="center" align="center">
        <v-col cols="12" md="6" class="px-3">
          <div v-animate-on-scroll class="text__wrapper font-light px-sm-8">
            <h2 class="section__title mb-4">Bienvenidos a The God Academy</h2>
            <p class="text__lg mb-8">
              Disfruta este breve material que te cuenta un poco de los que
              somos, lo que hacemos y como anhelamos aportar a tu crecimiento
              espiritual. Creemos que se abrirán tus ojos espirituales y el
              conocimiento de Dios cambiará tu vida para siempre.
            </p>
          </div>
        </v-col>
        <v-col cols="12" md="6" class="px-3">
          <div v-animate-on-scroll class="video__wrapper px-sm-8 text-center">
            <iframe
              src="https://www.youtube.com/embed/kLjnDzJh4_U?rel=0&amp;showinfo=0&autoplay=1&loop=0"
              frameborder="0"
              allowfullscreen
              loading="lazy"
              width="1280"
              height="720"
              class="video__item embedded-video mt-14 mt-sm-0"
              style="height: 305px"
            ></iframe>
            <p class="text__mid mt-2">Ezequiel 11:19-20</p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.welcome {
  color: #fff;
}
</style>
