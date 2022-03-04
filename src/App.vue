<template>
  <section id="welcome" class="overflow-hidden">
    <v-app-bar flat class="bar">
      <strong class="ml-3" large>
        <v-icon right x-large color="white" style="color: white !important">
          mdi-ferry
        </v-icon>
        PuertApp
      </strong>
    </v-app-bar>
    <v-row no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/port.jpg')" height="100vh" />
      </v-col>
      <v-col class="align-content-space-between layout wrap" cols="12" md="6">
        <v-row lign="center" justify="center">
          <div class="text">
            <base-text>
              Desde Cargofive se envio un desafio el cual era consumir una API,
              para mostrar una tabla de diferentes puertos alrededor de todo el
              mundo. En la misma se agregaron diferentes tipos filtros. El
              "deploy" del Proyecto se ha realizado en VERCEL.
            </base-text>
          </div>
        </v-row>
      </v-col>
    </v-row>
    <div>
      <Datatable :puertos="puertos" />
    </div>
    <div>
      <Footer />
    </div>
  </section>
</template>

<script>
import axios from "axios";
import Datatable from "./components/Datatable";
import Footer from "./components/Footer";
export default {
  name: "App",
  components: {
    Datatable,
    Footer,
  },
  data() {
    return {
      puertos: [],
    };
  },
  methods: {
    getPorts() {
      const api = "https://apitest.cargofive.com/api/ports";
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
<style scoped>
.bar {
  background-color: #1a237e !important;
  color: #fff;
}
.text {
  max-width: 50%;
  max-height: 600px !important;
  margin-top: 50% !important;
  margin-left: 50px !important;
}
@media screen and (max-width: 600px) {
  .text {
    display: none;
  }
}

@media screen and (max-width: 320px) {
  .text {
    display: none;
  }
}
</style>