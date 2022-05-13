<template>
    <h1>Watcher Lesson</h1>
    <h2>Volume tracker</h2>
    <p>Current volume - {{volume}}</p>
    <div>
        <button @click="volume += 2">UP</button>
        <button @click="volume -= 2">DOWN</button>
    </div>
</template>

<script>
export default {
  name: "WatchersComponent",
  data() {
      return {
          volume: 0
      }
  },
  watch: {
      volume(newValue, oldValue) {
          if (newValue > oldValue && newValue === 16){
              alert("Listening on loud volumes for long period of time will damage your ears");
          }
      }
  }
};
</script>

<style>
</style>