<template>
  <v-footer class="footer">
    <v-card class="flex footer" flat tile>
      <v-card-title class="teal">
        <v-icon right x-large color="white" style="color: white !important">
          mdi-ferry
        </v-icon>
        <strong class="subheading" style="color: white">PuertApp</strong>
        <v-spacer></v-spacer>
        <v-btn
          elevation="2"
          outlined
          rounded
          color="white"
          href="https://portfolio-itsjuanit.vercel.app/"
          target="_blank"
          style="color: white"
          >Itsjuanit</v-btn
        >
      </v-card-title>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style>
.footer {
  background-color: #1a237e !important;
}
</style>