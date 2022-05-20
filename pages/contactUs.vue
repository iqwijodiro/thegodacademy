<template>
  <div class="contact">
    <hero-contact />
    <social-contact />
    <contact-path />
  </div>
</template>

<script>
import heroContact from '~/components/contactUs/heroContact.vue'
import SocialContact from '~/components/contactUs/socialContact.vue'
import ContactPath from '~/components/contactUs/contactPath.vue'
export default {
  components: { heroContact, SocialContact, ContactPath },
}
</script>

<style></style>
