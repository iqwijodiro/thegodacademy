<template>
  <section class="top py-14">
    <v-container>
      <h2 class="text-center mb-14">Lo más Popular</h2>
      <v-row justify="center">
        <v-col v-for="course in courses" :key="course.title" cols="12" md="4">
          <course-card
            :img-link="course.imgSrc"
            width="100%"
            max-width="350"
            height="100%"
            :title="course.title"
            :subtitle="course.subtitle"
            :description="course.description"
          />
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
      courses: [
        {
          imgSrc:
            'https://r.mobirisesite.com/204435/assets/images/recurso-1logos-a-fondo-696x696.png?v=1NO9d3',
          title: 'Cursos',
          subtitle: 'Formacion por temas',
          description:
            'Mobirise is an easy website builder. Just drop site elements to your page, add content and style it to look the way you like.',
        },
        {
          imgSrc:
            'https://r.mobirisesite.com/204435/assets/images/recurso-1logos-a-fondo-696x696.png?v=1NO9d3',
          title: 'Cursos',
          subtitle: 'Formacion por temas',
          description:
            'You dont have to code to create your own site. Select one of available themes in the Mobirise Site Maker.',
        },
        {
          imgSrc:
            'https://r.mobirisesite.com/204435/assets/images/recurso-1logos-a-fondo-696x696.png?v=1NO9d3',
          title: 'Cursos',
          subtitle: 'Formacion por temas',
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
    font-family: $title-font;
    color: #242424;
    font-weight: bold;
    font-size: 3rem;
  }
}
</style>
