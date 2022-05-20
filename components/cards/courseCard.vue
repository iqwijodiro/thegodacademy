<template>
  <v-card
    :max-height="maxHeight"
    :max-width="maxWidth"
    :min-height="minHeight"
    :min-width="minWidth"
    :width="width"
    :height="height"
    flat
    light
    class="course__card"
  >
    <figure>
      <v-img
        loading="lazy"
        :src="imgLink"
        height="200px"
        class="ma-0 pa-0"
        :alt="title"
      >
      </v-img>
    </figure>
    <div class="card__wrapper px-8 pt-8">
      <h2 class="card__title mb-2 pa-0">
        <strong>
          {{ title }}
        </strong>
      </h2>
      <h3 class="card__subtitle mt-1 mb-2 mx-0 pa-0">
        {{ subtitle }}
      </h3>
      <p class="card__text pa-0 my-4">
        {{ description }}
      </p>
    </div>
    <div class="px-8 pb-8">
      <my-btn text="Start Now" destiny="/courses" color="primary" />
      <!-- @click="selectCourse(course)" -->
    </div>
  </v-card>
</template>
<script>
import myBtn from '../buttons/myBtn.vue'
export default {
  components: { myBtn },
  props: {
    width: {
      type: String,
      default: '',
    },
    height: {
      type: String,
      default: '',
    },
    minWidth: {
      type: String,
      default: '',
    },
    minHeight: {
      type: String,
      default: '',
    },
    maxWidth: {
      type: String,
      default: '',
    },
    maxHeight: {
      type: String,
      default: '',
    },
    imgLink: {
      type: String,
      default: '',
      required: true,
    },
    title: {
      type: String,
      default: '',
      required: true,
    },
    subtitle: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      course: {},
    }
  },
}
</script>

<style lang="scss" scoped>
.course__card {
  .card__wrapper {
    height: 300px;
  }
}
</style>
