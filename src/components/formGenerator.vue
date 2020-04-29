<template>
  <div>
    Question # {{questionsindex + 1}} of {{this.questions.length}}
    <component
      :is="this.questions[this.questionsindex].fieldType"
      v-bind="this.questions[this.questionsindex]"
    ></component>
    <v-progress-linear :value="progressbarvalue"></v-progress-linear>
    <v-btn v-if="this.questionsindex != 0" @click="BackButton()">Back</v-btn>
    <v-btn v-if="this.questionsindex != (this.questions.length -1)" @click="nextButton()">Next</v-btn>
  </div>
</template>

<script>
import textInput from "@/assets/formtemplates/textInput.vue";
import selectList from "@/assets/formtemplates/selectList.vue";
import selectRadio from "@/assets/formtemplates/selectRadio.vue";
export default {
  components: {
    textInput,
    selectList,
    selectRadio
  },
  data() {
    return {
      questionsindex: 0,
      questions: [
        {
          fieldType: "selectRadio",
          query: "How are you feeling today?",
          name: "feelingtoday",
          options: ["Great", "Okay", "Not Good", "Terrible"]
        },
        {
          fieldType: "selectList",
          name: "title",
          multi: false,
          query: "What is your title?",
          options: ["Ms", "Mr", "Dr", "Lord"]
        },
        {
          fieldType: "textInput",
          query: "What is your first name?",

          name: "firstName"
        },
        {
          fieldType: "textInput",
          query: "What is your last name?",
          name: "lastName"
        }
      ]
    };
  },
  computed: {
    progressbarvalue: function() {
      return ((this.questionsindex + 1) / this.questions.length) * 100;
    }
  },
  methods: {
    nextButton() {
      this.questionsindex++;
    },
    BackButton() {
      this.questionsindex--;
    }
  }
};
</script>

<style>
</style>