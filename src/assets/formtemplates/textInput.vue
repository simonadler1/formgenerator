<template>
  <div>
    <v-col cols="12" sm="6" md="3">
      {{query}}
      <v-text-field :name="this.name" outlined></v-text-field>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "textInput",
  props: ["placeholder", "name", "query"]
};
</script>

<style>
</style>