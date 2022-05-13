<template>
  <h1>Watcher Lesson</h1>
  <h2>Volume tracker</h2>
  <p>Current volume - {{ volume }}</p>
  <div>
    <button @click="volume += 2">UP</button>
    <button @click="volume -= 2">DOWN</button>
  </div>

  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />

  <div class="movie-list">
      <div>
          <h2>List of movies</h2>
          <ul>
              <li v-for="move in movieList" :key="move"><span>{{move}}</span></li>
          </ul>
      </div>
      <div class="movie-list-input">
          <input type="text" v-model="movie" />
          <button @click="submitMovie">Add</button>
      </div>
  </div>

</template>

<script>
export default {
  name: "WatchersComponent",
  data() {
    return {
      volume: 0,
      movie: "Hello",
      movieInfo: {
          title: '',
          actor: ''
      },
      movieList: []
    };
  },
  methods: {
      submitMovie(){
          this.movieList.push(this.movie);
          this.movie = '';
      }
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening on loud volumes for long period of time will damage your ears"
        );
      }
    },
    movie: {
      handler(newValue) {
        console.log("Calling API with new value - " + newValue);
      },
      immediate: true,
    },
    movieInfo: {
        handler(newValue){
            console.log(`Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`);
        },
        deep: true
    }
  },
};
</script>

<style scoped>
    .movie-list {
        display: flex;
        margin-top: 1rem;
    }
    .movie-list-input{
        margin-top: 1.5rem;
        margin-left: 1rem;
    }
</style>