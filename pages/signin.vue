<template>
  <v-form>
    <Input label="Nombre de usuario" />
    <Input label="Contraseña" />
    <Button label="Iniciar sesion" @eventClick="signin" />
    <Button label="Crear cuenta" @eventClick="sendForm" />
  </v-form>
</template>

<script>
export default {
  methods: {
    sendForm() {
      $nuxt.$router.push("signup");
    },
    signin() {
      $nuxt.$router.push("products");
    },
  },
};
</script>
