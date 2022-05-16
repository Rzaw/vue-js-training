<template>
  <h1>Basic component manipulation</h1>

  <GreetComponent firstname="Matijs" lastname="Lode" />
  <GreetComponent :firstname="first" :lastname="last" />
  <GreetComponent firstname="Anna" lastname="Lode" />
  <GreetComponent firstname="Teodors" lastname="Lode" />
  <ArticleComponent title="Hello" :likes="3" :isPublished="true"/>
</template>

<script>
import GreetComponent from "./GreetComponent.vue";
import ArticleComponent from "./ArticleComponent.vue";
export default {
  name: "BasicComponentManipulationComponent",
  components: {
    GreetComponent,
    ArticleComponent
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