<template>
  <section class="top">
    <v-container>
      <h2 class="section__title text-center mb-14">Lo más Popular</h2>
      <v-row justify="center">
        <v-col
          v-for="course in courses"
          :key="course.title"
          cols="12"
          md="4"
          class="px-4 mx-0 mb-8"
        >
          <v-lazy
            v-model="isActive"
            :options="{ threshold: 0.5 }"
            transition="scroll-y-reverse-transition"
          >
            <course-card
              :img-link="course.imgSrc"
              width="100%"
              max-width="380"
              height="100%"
              min-height="600"
              :title="course.title"
              :subtitle="course.subtitle"
              :description="course.description"
            />
          </v-lazy>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import courseCard from '../cards/courseCard.vue'
export default {
  components: {
    courseCard,
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
          title: 'Cursos',
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
}
</style>
