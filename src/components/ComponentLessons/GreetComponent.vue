<template>
  <p>Hello, {{firstname}} {{lastname}}</p>
</template>

<script>
export default {
  name: "GreetComponent",
  props: [
    'firstname', 'lastname'
  ],
  // data(){}
};
</script>

<style>
</style>