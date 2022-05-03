<template>
  <div>
    <h1>Conditional looping</h1>
    <h2>List of strings</h2>
    <p>This lesson showed me how to conditionally render a list. We tried to add v-if in same line as v-for, but compiler did noot like that. So we had to create template tag and add v-for on template tag, then on tag were we wanted our data, added v-if tag.</p>
    <ol>
      <template v-for="(name, index) in listNames" :key="index">
        <li v-if="name === 'Matijs' || name == 'Teodors'">{{name}}</li>
      </template>
    </ol>

    
  </div>
</template>

<script>
export default {
  name: "ListConditionalLoopComponent",
  data() {
    return {
      listNames: ["Matijs", "Anna", "Teodors", "Sāra"],
      fullNames: [
        { first: "Matijs", last: "Lode" },
        { first: "Anna Estere", last: "Lode" },
        { first: "Teodors Dailis", last: "Lode" },
        { first: "Sāra Rita", last: "Lode" },
      ],
      actors: [
        {
          name: "Christian Bale",
          movies: ["Batman", "The Prestige"],
        },
        {
          name: "Di Caprio",
          movies: ["Titanic", "Inception"],
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>