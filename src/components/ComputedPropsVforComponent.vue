<template>
  <h1>Computed Properties with v-for lesson</h1>
<p>Issue can be already seen for inlining v-if closure vs computed property</p>
  <h2>List with v-if inside of loop</h2>
  <ul>
    <li v-for="item in items" :key="item.id">
      <span v-if="item.price > 100">{{ item.title }}</span>
    </li>
  </ul>

  <h2>List from computed property</h2>
  <ul>
      <li v-for="item in getExpensiveItems" :key="item.id">
        {{item.title}}
      </li>
  </ul>
</template>

<script>
export default {
  name: "ComputedPropsVforComponent",
  data() {
    return {
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
    };
  },
  computed: {
    getExpensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
  },
};
</script>

<style>
</style>