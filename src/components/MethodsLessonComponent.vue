<template>
  <h1>Method lesson</h1>
  <p>Calling add method: {{ addThreeNumbers(2, 4, 9) }}</p>
  <p>Multiply method: {{ multiply(5) }}</p>
</template>

<script>
export default {
  name: "MethodsLessonComponent",
  data() {
    return {
      baseMultiplier: 5,
    };
  },
  methods: {
    addThreeNumbers(a, b, c) {
      // if (Number.isInteger(a)) // Should add number check
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
  },
};
</script>

<style>
</style>