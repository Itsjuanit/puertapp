<template>
  <div>
    <bootstrap-vue-datatable :puertos="puertos"></bootstrap-vue-datatable>
  </div>
</template>

<script>
import axios from "axios";
import BootstrapVueDatatable from "./components/BootstrapVueDatatable";
export default {
  name: "App",
  components: {
    BootstrapVueDatatable,
  },
  data() {
    return {
      puertos: [],
    };
  },
  methods: {
    getPorts() {
      const api = "http://apitest.cargofive.com/api/ports";
      axios.get(api).then((res) => {
        this.puertos = res.data.data;
      });
    },
  },
  mounted() {
    this.getPorts();
  },
};
</script>