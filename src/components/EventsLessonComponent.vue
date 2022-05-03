<template>
  <div>
    <h1>Events lesson</h1>
    <p>{{ name }}</p>
    <button @click="changeName('Anna')">Hello</button>

    <h2>Counter</h2>
    <p>Current: {{counter}}</p>
    <button @click="increment()">+</button>
    <button @click="decrement()">-</button>

  </div>
</template>

<script>
export default {
  name: "EventsLessonComponent",
  data() {
    return {
      name: "Matijs",
      counter: 0
    };
  },
  methods: {
      changeName(nameToBeChanged){
          this.name = nameToBeChanged
      },
      increment(){
          this.counter++;
      },
      decrement()
      {
          this.counter--;
      }
  },
};
</script>

<style>
</style>