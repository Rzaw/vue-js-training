<template>
  <h1>Basic component manipulation</h1>

  <GreetComponent firstname="Matijs" lastname="Lode" />
  <GreetComponent :firstname="first" :lastname="last" />
  <GreetComponent firstname="Anna" lastname="Lode" />
  <GreetComponent firstname="Teodors" lastname="Lode" />
</template>

<script>
import GreetComponent from "./GreetComponent.vue";
export default {
  name: "BasicComponentManipulationComponent",
  components: {
    GreetComponent,
  },
  data() {
      return {
          first: 'Matijs',
          last: 'Lode, but data from data prop'
      };
  }
};
</script>

<style>
</style>