<template>
  <div>
    <!-- <h1>Hello, {{ name }} {{ surname }}!</h1>
    <p v-text="name"></p>
    <h1>List tutorial</h1>
    <ListComponent /> -->
  </div>
</template>

<script>
import ListComponent from './components/ListComponent.vue'
export default {
  name: "App",
  components: {
    ListComponent
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
