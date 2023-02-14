<template>
  <form class="form-contact">
    <TitleContact />
    <div class="form-contact__inputs">
      <InputContact label="Nom" type="text" placeholder="Votre nom" v-model="name" />
      <InputContact label="Email" type="email" placeholder="Votre email" v-model="email" />
      <InputContact label="Message" type="textarea" placeholder="Votre message" v-model="message" />
    </div>
    <ButtonSubmit label="Envoyer" />
  </form>
</template>

<script>
import TitleContact from '@/atoms/TitleContact.vue'
import InputContact from '@/atoms/InputContact.vue'
import ButtonSubmit from '@/atoms/ButtonSubmit.vue'

export default {
  name: 'FormContact',
  components: {
    TitleContact,
    InputContact,
    ButtonSubmit,
  },
  data() {
    return {
      name: '',
      email: '',
      message: '',
    }
  },
  methods: {
    onSubmit() {
      // Code exécuté lorsque le formulaire est soumis
    },
  },
}
</script>

<style scoped>
.form-contact {
  max-width: 400px;
  margin: 0 auto;
}

.form-contact__inputs {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
}
</style>