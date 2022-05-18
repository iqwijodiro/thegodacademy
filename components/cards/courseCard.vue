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
      <v-img :src="imgLink" height="200px" class="ma-0 pa-0" :alt="title">
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
      <my-btn text="Start Now" destiny="/courses" btn-type="primary" />
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
  // opacity: 0.75;
  .img-course {
    width: 100%;
    height: 100%;
    // filter: grayscale(50%);
    transition: all 0.4s ease-in-out;
  }
  &:hover {
    // opacity: 1;
    cursor: pointer;
    transition: all 0.4s ease-in-out;
    // transform: translateY(-5px);
    // .img-course {
    //   // filter: none;
    // }
  }
  .card__wrapper {
    height: 300px;
    .card__title {
      font-family: $title-font;
      font-size: 3rem;
      font-weight: 700;
      line-height: 1;
    }
    .card__subtitle {
      font-size: 1.2rem;
      color: #bbb;
      font-weight: 400;
    }
    .card__text {
      font-size: 1.2rem;
      font-weight: 400;
    }
  }
}
</style>
