<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <formGenerator />
    </v-content>
  </v-app>
</template>

<script>
import formGenerator from "@/components/formGenerator.vue";
export default {
  name: "App",

  components: {
    formGenerator
  },

  data: () => ({
    //
  })
};
</script>
