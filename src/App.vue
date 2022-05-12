<template>
  <div>
    <!-- <h1>Hello, {{ name }} {{ surname }}!</h1>
    <p v-text="name"></p>
    <h1>List tutorial</h1>
    <ListComponent /> -->
    <!-- <ListConditionalLoopComponent /> -->
    <!-- <MethodsLessonComponent /> -->
    <!-- <EventsLessonComponent /> -->
    <!-- <FormLessonComponent /> -->
    <!-- <DirectivesLessonComponent /> -->
    <!-- <ComputedPropertiesLessonComponent /> -->
    <!-- <ComputedPropsVforComponent /> -->
    <ComputedSetterComponent />
  </div>
</template>

<script>
  // import ListComponent from './components/ListComponent.vue'
  // import ListConditionalLoopComponent from './components/ListConditionalLoopComponent.vue'
  // import MethodsLessonComponent from './components/MethodsLessonComponent.vue'
  // import EventsLessonComponent from './components/EventsLessonComponent.vue'
  // import FormLessonComponent from './components/FormLessonComponent.vue'
  // import DirectivesLessonComponent from './components/DirectivesLessonComponent.vue'
  // import ComputedPropertiesLessonComponent from './components/ComputedPropertiesLessonComponent.vue'
  // import ComputedPropsVforComponent from './components/ComputedPropsVforComponent.vue'
  import ComputedSetterComponent from './components/ComputedSetterComponent.vue'
export default {
  name: "App",
  components: {
    // ListComponent,
    // ListConditionalLoopComponent,
    // MethodsLessonComponent,
    // EventsLessonComponent,
    // DirectivesLessonComponent,
    // ComputedPropertiesLessonComponent
    // ComputedPropsVforComponent
    ComputedSetterComponent
  },
  data() {
    return {
      name: "Matijs",
      surname: "Lode",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
