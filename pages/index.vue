<template>
  <div class="index">
    <hero-index />
    <versicle-sect />
    <top-courses />
  </div>
</template>

<script>
import heroIndex from '~/components/home/heroIndex.vue'
import VersicleSect from '~/components/home/versicleSect.vue'
import TopCourses from '~/components/home/topCourses.vue'
export default {
  name: 'HeroIndex',
  components: {
    heroIndex,
    VersicleSect,
    TopCourses,
  },
}
</script>
