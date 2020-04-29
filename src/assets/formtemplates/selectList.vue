<template>
  <div>
    {{query}}
    <v-col class="d-flex" cols="12" sm="6">
      <v-select :items="this.options"></v-select>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "SelectList",
  props: ["multi", "options", "name", "label", "query"]
};
</script>

<style>
</style>