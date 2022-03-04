<template>
  <v-app>
    <v-main>
      <v-container>
        <h2>Tabla de puertos</h2>
        <v-row>
          <v-col md="3">
            <v-text-field
              v-model="search"
              append-icon="mdi-magnify"
              label="Busqueda de puertos"
              single-line
              hide-details
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-data-table
              :headers="headers"
              :items="puertos"
              :items-per-page="5"
              :search="search"
              class="elevation-1"
            >
            </v-data-table>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "Datatable",
  props: ["puertos"],
  data() {
    return {
      search: "",
      headers: [
        { text: "Número de ID", value: "id" },
        { text: "Nombre", value: "name" },
        { text: "País", value: "country" },
        { text: "Continente", value: "continent" },
        { text: "Coordenadas", value: "coordinates" },
      ],
    };
  },
};
</script>