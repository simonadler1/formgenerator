<template>
  <div>
    {{query}}
    <v-col class="d-flex" cols="12" sm="6">
      <v-radio-group v-model="radioGroup">
        <v-radio v-for="n in this.options" :key="n" :label="` ${n}`" :value="n"></v-radio>
      </v-radio-group>
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