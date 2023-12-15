<template>
  <h1>Home Component {{ "20 + 20".length }}</h1>
  <h2>Email: {{ email }}</h2>
  <h2>mobile: {{ mobile }}</h2>
  <h2>Name: {{ getName("samir sadek") }}</h2>

  <h2>---------Event Click---------</h2>

  <p>{{ count }}</p>
  <button v-on:click="test()">Increment</button>
  <button v-on:click="test2()">Decrement</button>

  <h2>----Two Way Binding--------</h2>
  <input type="text" v-model="count" />
  <h2>{{ count }}</h2>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      email: "samirsadek@1009.com",
      mobile: 1020,
      count: 0,
      getName: function (a) {
        return a;
      },
    };
  },
  methods: {
    getData() {
      return {
        name: "samir",
        email: this.email,
      };
    },
    test() {
      this.count = this.count + 1;
    },
    test2() {
      this.count = this.count - 1;
    },
  },
};
</script>
<style scoped>
h1 {
  color: brown;
}
</style>
