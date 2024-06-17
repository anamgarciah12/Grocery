<template>
  <v-app id="inspire">
    <v-main>
      <v-toolbar flat color="#ff000000">
        <h1>Mis favoritos</h1>
        <v-spacer />
        <!-- <Button label="Ver lista de compras" /> -->

        <!-- Lista de productos -->
        <Button label="Mis compras" color="primary" @eventClick="sendForm" />
        <Button label="Productos" class="ml-3" @eventClick="goProducts" />

        <Button
          label="Cerrar sesion"
          color="secondary"
          class="ml-3"
          @eventClick="logout"
        />
      </v-toolbar>
      <v-container>
        <v-row>
          <v-col v-for="n in 6" :key="n" cols="4">
            <v-card>
              <v-img
                height="250"
                src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
              ></v-img>
              <v-card-title>Cafe Badilico</v-card-title>
              <v-card-subtitle>$ 5000</v-card-subtitle>
              <v-card-actions>
                <Button :block="true" label="Agregar a la lista de compras" />
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  methods: {
    sendForm() {
      $nuxt.$router.push("shopping");
    },
    logout() {
      $nuxt.$router.push("signin");
    },
    goProducts() {
      $nuxt.$router.push("products");
    },
  },
};
</script>
