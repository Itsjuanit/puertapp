<template>
  <div id="app" class="container mt-3 mb-5">
    <h2>Tabla de puertos del mundo</h2>
    <b-row class="mb-3">
      <b-col md="3">
        <b-form-input
          v-model="filter"
          type="search"
          id="filterInput"
          placeholder="Busqueda de puerto"
        ></b-form-input>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <b-table
          striped
          hover
          :items="puertos"
          :fields="fields"
          :current-page="currentPage"
          :per-page="perPage"
          :filter="filter"
        >
        </b-table>
        <b-pagination
          class="justify-content-center"
          pills
          v-model="currentPage"
          :total-rows="rows"
          :per-page="perPage"
          aria-controls="my-table"
        ></b-pagination>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  props: ["puertos"],
  name: "App",
  data() {
    return {
      filter: "",
      perPage: 15,
      currentPage: 5,
      fields: ["id", "name", "country", "continent", "coordinates"],
    };
  },
  computed: {
    rows() {
      return this.puertos.length;
    },
  },
};
</script>
