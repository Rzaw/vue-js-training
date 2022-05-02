<template>
  <div>
    <h2>List of strings</h2>
    <ol>
      <li v-for="(name, index) in listNames" :key="index">{{name}}</li>
    </ol>

    <h2>List of objects</h2>
    <ul>
      <li v-for="(name, index) in fullNames" :key="index">{{name.first}} {{name.last}}</li>
    </ul>

    <h2>List of arrays</h2>
    <div v-for="(actor, index) in actors" :key="index">
      <h3>{{actor.name}}</h3>
      <h4>Movies</h4>
      <ul>
        <li v-for="(movie, index) in actor.movies" :key="index">
          {{movie}}
        </li>
      </ul>
    </div>
    <h2>List of object properties</h2>
    <ul>
      <li v-for="(value, key, index) in fullNames[0]" :key="index">
        Key: {{key}}; Value: {{value}};
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ListComponent",
  data() {
    return {
      listNames: ["Matijs", "Anna", "Teodors", "Sāra"],
      fullNames: [
        {first: 'Matijs', last: 'Lode'},
        {first: 'Anna Estere', last: 'Lode'},
        {first: 'Teodors Dailis', last: 'Lode'},
        {first: 'Sāra Rita', last: 'Lode'}
        ],
        actors: [
          {
            name: 'Christian Bale',
            movies: ['Batman', 'The Prestige']
          },
          {
            name: 'Di Caprio',
            movies: ['Titanic', 'Inception']
          }]
    };
  },
};
</script>

<style scoped>
</style>