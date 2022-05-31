<template>
  <section class="top">
    <v-container>
      <h2 v-animate-on-scroll class="section__title text-center mb-14">
        Lo más Popular
      </h2>
      <v-row justify="center">
        <v-col cols="12" class="px-4 mx-0 mb-8">
          <vue-horizontal responsive class="horizontal__wrapper mx-auto py-10">
            <course-card
              v-for="(course, i) in courses"
              :key="i"
              :img-link="course.imgSrc"
              width="100%"
              max-width="380"
              :title="course.title"
              :subtitle="course.subtitle"
              :description="course.description"
            />
          </vue-horizontal>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import VueHorizontal from 'vue-horizontal'
import courseCard from '../cards/courseCard.vue'
export default {
  components: {
    courseCard,
    VueHorizontal,
  },
  data() {
    return {
      isActive: false,
      courses: [
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'Cursos',
          subtitle: 'Formacion por temas',
          description:
            'Mobirise is an easy website builder. Just drop site elements to your page, add content and style it to look the way you like.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'Programas',
          subtitle: 'Formacion por estudios',
          description:
            'You dont have to code to create your own site. Select one of available themes in the Mobirise Site Maker.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
        {
          imgSrc: require('~/assets/images/logo_brand_card_square.png'),
          title: 'For Groups',
          subtitle: 'Formacion para Grupos',
          description:
            'Select the theme that suits you. Each theme in the Mobirise Website Software contains a set of unique blocks.',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.top {
  min-height: 80vh;
  background-color: #fff;
  h2 {
    color: #383838;
  }
  .horizontal__wrapper {
    min-height: 600px;
    // width: 100%;
    // max-width: 1300px;
    // display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
