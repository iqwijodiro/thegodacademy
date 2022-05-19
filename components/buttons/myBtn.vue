<template>
  <v-btn
    nuxt
    depressed
    :to="destiny"
    class="myBtn rounded-xl"
    :color="btnType"
    @click.prevent="action"
  >
    <slot name="preppendIcon">
      <v-icon> {{ preppendIcon }}</v-icon>
    </slot>
    <div class="mx-2 btn__text">{{ text }}</div>
    <slot name="appendIcon">
      <v-icon> {{ appendIcon }}</v-icon>
    </slot>
  </v-btn>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    destiny: {
      type: String,
      default: '/',
    },
    btnType: {
      type: String,
      required: true,
    },
    action: {
      type: Function,
      default: () => [],
    },
    iconName: {
      type: String,
      default: '',
    },
    preppendIcon: {
      type: String,
      default: '',
    },
    appendIcon: {
      type: String,
      default: '',
    },
  },
}
</script>

<style lang="scss" scoped>
.myBtn {
  color: #373737 !important;
  background-color: $green-primary !important;
  padding: 1.5rem 1.2rem !important;
  // border-radius: 100px;
  // -webkit-border-radius: 100px;
  // -moz-border-radius: 100px;
  // -ms-border-radius: 100px;
  // -o-border-radius: 100px;
  &:hover {
    background-color: $green-hover !important;
    color: #fff !important;
  }
  .btn__text {
    font-size: 1.1rem;
    text-transform: none !important;
    font-weight: 600 !important;
    letter-spacing: normal;
  }
}
</style>
