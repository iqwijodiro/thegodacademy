<template>
  <div class="d-flex justify-center align-center mx-5">
    <v-btn :to="destiny" class="myBtn" :color="btnType" @click.prevent="action">
      <v-icon v-if="preppendIcon"> {{ iconName }} </v-icon>
      <div v-else-if="iconName === ''">{{ text }}</div>
      <v-icon v-else> {{ iconName }} </v-icon>
    </v-btn>
  </div>
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
  background-color: $green-primary !important;
  font-size: 1.1rem;
  color: #252525 !important;
  text-transform: none !important;
  font-weight: 400 !important;
  padding: 1.5rem 1.2rem !important;
  letter-spacing: normal;
  border-radius: 100px;
  -webkit-border-radius: 100px;
  -moz-border-radius: 100px;
  -ms-border-radius: 100px;
  -o-border-radius: 100px;
  &:hover {
    background-color: #00a89a !important;
    color: #fff !important;
  }
}
</style>
