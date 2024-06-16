<template>
  <v-app id="inspire">
    <v-main>
      <v-toolbar flat color="#ff000000">
        <h1>Productos</h1>
        <v-spacer />
        <!-- <Button label="Ver lista de compras" /> -->

        <!-- Lista de productos -->
        <v-menu offset-y left>
          <template v-slot:activator="{ on, attrs }">
            <v-btn rounded color="primary" dark v-bind="attrs" v-on="on">
              Ver lista de compras
            </v-btn>
          </template>
          <v-list>
            <v-list-item>
              <v-list-item-avatar tile>
                <v-img
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title>Cafe Badilico </v-list-item-title>
                <v-list-item-subtitle>$ 5000 </v-list-item-subtitle>
              </v-list-item-content>
              <v-btn icon color="red">
                <v-icon>mdi-delete</v-icon>
              </v-btn>
            </v-list-item>
            <v-list-item>
              <v-list-item-avatar tile>
                <v-img
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title>Cafe Badilico </v-list-item-title>
                <v-list-item-subtitle>$ 5000 </v-list-item-subtitle>
              </v-list-item-content>
              <v-btn icon color="red">
                <v-icon>mdi-delete</v-icon>
              </v-btn>
            </v-list-item>
            <v-list-item>
              <v-list-item-avatar tile>
                <v-img
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title>Cafe Badilico </v-list-item-title>
                <v-list-item-subtitle>$ 5000 </v-list-item-subtitle>
              </v-list-item-content>
              <v-btn icon color="red">
                <v-icon>mdi-delete</v-icon>
              </v-btn>
            </v-list-item>
          </v-list>
        </v-menu>

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
  },
};
</script>
