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
    class="course__card mx-4 my-5 pb-3 d-flex flex-column justify-space-between"
  >
    <figure class="overflow-hidden">
      <v-img
        :src="imgLink"
        height="200px"
        class="mb-2 img-course white--text align-end pb-3"
        :alt="name"
      >
      </v-img>
    </figure>
    <v-card-title class="card-title my-2" tag="h2">
      {{ title }}
    </v-card-title>
    <v-card-subtitle class="text-card" tag="h3">
      {{ subtitle }}
    </v-card-subtitle>
    <v-card-text tag="p">
      {{ description }}
    </v-card-text>
    <div class="centrar mt-2">
      <v-btn class="minibtn mt-3" @click="selectCourse(course)">
        Start now
      </v-btn>
    </div>
  </v-card>
</template>
<script>
export default {
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
    filter: grayscale(50%);
    transition: all 0.4s ease-in-out;
  }
  &:hover {
    // opacity: 1;
    transition: all 0.4s ease-in-out;
    transform: translateY(-5px);
    .img-course {
      filter: none;
    }
  }
  .minirow div {
    font-size: 1rem !important;
    color: #2b2b2b;
    // &:nth-child(1) {
    //     border-right: 2px solid $gray-light;
    // }
  }
}
</style>
