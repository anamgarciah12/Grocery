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
          <v-col v-for="(product, i) in products" :key="i" cols="4">
            <v-card>
              <v-img height="250" :src="product.photo"></v-img>
              <v-card-title>{{ product.name }}</v-card-title>
              <v-card-subtitle>$ {{ product.price }}</v-card-subtitle>
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
  data() {
    return {
      products: [
        {
          photo:
            "https://http2.mlstatic.com/D_NQ_NP_870691-MLU74543047648_022024-O.webp",
          name: "Computador Gamer Lenovo",
          price: "4.945.000",
        },
        {
          photo:
            "https://http2.mlstatic.com/D_NQ_NP_855678-MLU70082561247_062023-O.webp",
          name: "Computador Portatil Dell Core I5",
          price: "1.953.600",
        },
        {
          photo:
            "https://http2.mlstatic.com/D_NQ_NP_984848-MLA48644126914_122021-O.webp",
          name: "Portátil HP 255 G7",
          price: "1.550.000",
        },
      ],
    };
  },
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
