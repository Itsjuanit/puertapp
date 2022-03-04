<template>
  <div>
    <Vuetify :puertos="puertos"></Vuetify>
  </div>
</template>

<script>
import axios from "axios";
import Vuetify from "./components/Vuetify";
export default {
  name: "App",
  components: {
    Vuetify,
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