<template>
  <v-app id="inspire">
    <v-main>
      <v-toolbar flat color="#ff000000">
        <h1>Productos</h1>
        <v-spacer />
        <!-- <Button label="Ver lista de compras" /> -->

        <!-- Lista de productos -->
        <Button label="Mis compras" color="primary" @eventClick="goShopping" />
        <Button
          label="Mis favoritos"
          color="primary"
          class="ml-3"
          @eventClick="goFavorites"
        />
        <Button
          label="Cerrar sesion"
          color="secondary"
          class="ml-3"
          @eventClick="sendForm"
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
      $nuxt.$router.push("signin");
    },
    goShopping() {
      $nuxt.$router.push("shopping");
    },
    goFavorites() {
      $nuxt.$router.push("favorites");
    },
  },
};
</script>
