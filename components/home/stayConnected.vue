<template>
  <div class="sharing">
    <section class="video">
      <v-container>
        <h2 class="section__title text-center mb-12" style="height: 100px">
          Mantente Conectado
        </h2>
        <v-row align="center">
          <v-col cols="12" md="6" class="py-0 px-4">
            <div class="video__wrapper">
              <iframe
                src="https://www.youtube.com/embed/kLjnDzJh4_U?rel=0&amp;showinfo=0&autoplay=1&loop=0"
                frameborder="0"
                allowfullscreen
                width="800"
                height="600"
                class="video__item embedded-video"
                style="height: 400px"
              ></iframe>
            </div>
            <p class="video__description text-center text__mid pt-2 mb-4">
              Bienvenido a Theo Academy
            </p>
          </v-col>
          <v-col cols="12" md="6" class="py-0 px-4">
            <div class="text__wrapper pa-8">
              <h3
                class="section__subtitle text__special mb-4 font-weight-regular"
              >
                <strong>
                  Descubre la Transformación del Ser desde una perspectiva
                  Bíblica.
                </strong>
              </h3>
              <p class="text__lg">
                Estudiemos juntos el indudable valor de las escrituras en el
                proceso de nuestra transformación interna, caminando hacia la
                mente de Cristo
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="share">
      <v-container>
        <v-row justify="center">
          <v-col cols="12">
            <div class="social__list d-flex justify-center align-center">
              <a
                href="https://facebook.com"
                class="icon__wrapper d-flex justify-center align-center"
              >
                <v-icon light size="30" color="#fff" class="ma-0">
                  fab fa-facebook-f
                </v-icon>
              </a>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.sharing {
  background-color: $green-primary;
  .video__description {
    color: #383838;
  }
  .text__wrapper {
    .section__subtitle {
      color: #383838;
      font-weight: bold !important;
    }
    .text__lg {
      color: #383838;
    }
  }
  .share {
    .icon__wrapper {
      background-color: rgba($color: #1778f2, $alpha: 0.85);
      border-radius: 50% / 50%;
      display: inline-block;
      height: 55px;
      width: 55px;
      padding: 0;
      text-align: center;
      line-height: 55px;
      transition: background-color 0.2s ease-in;
      &:hover {
        background-color: #1778f2;
      }
    }
  }
}
</style>
