<template>
  <div class="index">
    <hero-index />
    <versicle-sect />
    <top-courses />
    <stay-Connected />
  </div>
</template>

<script>
import heroIndex from '~/components/home/heroIndex.vue'
import VersicleSect from '~/components/home/versicleSect.vue'
import TopCourses from '~/components/home/topCourses.vue'
import StayConnected from '~/components/home/stayConnected.vue'
export default {
  name: 'HeroIndex',
  components: {
    heroIndex,
    VersicleSect,
    TopCourses,
    StayConnected,
  },
}
</script>
