<template>
  <div>
    <h1>Events lesson</h1>
    <p>{{ name }}</p>
    <button v-on:click="name = 'Anna'">Hello</button>

    <h2>Counter</h2>
    <p>Current: {{counter}}</p>
    <button v-on:click="increment()">+</button>
    <button v-on:click="decrement()">-</button>

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