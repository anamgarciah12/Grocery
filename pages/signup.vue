<template>
  <v-form>
    <Input label="Nombre de usuario" />
    <Input label="Nombre completo" />
    <Input label="Contraseña" />
    <Button label="Registrarse" @eventClick="sendForm" />
    <Button label="Ya tengo una cuenta" @eventClick="sendForm" />
  </v-form>
</template>

<script>
export default {
  methods: {
    sendForm() {
      $nuxt.$router.push("signin");
    },
  },
};
</script>
