<template>
  <h1>Home Component {{ "20 + 20".length }}</h1>
  <h2>Email: {{ email }}</h2>
  <h2>mobile: {{ mobile }}</h2>
  <h2>Name: {{ getName("samir sadek") }}</h2>

  <h2>---------Event Click---------</h2>

  <p>{{ count }}</p>
  <button v-on:click="test()">Increment</button>
  <button v-on:click="test2()">Decrement</button>
  <br />
  <br />
  <h2>----Two Way Binding--------</h2>
  <input type="text" v-model="count" />
  <h2>{{ count }}</h2>
  <br />
  <br />
  <h2>----Get Input Value--------</h2>
  <input type="text" placeholder="Enter Email" v-model="inputEmail" />
  <br />
  <br />
  <input type="password" placeholder="Enter password" v-model="inputPass" />
  <br />
  <br />
  <button type="button" v-on:click="getInputValue()">Get Value</button>
  <h2>----Get Checkbox and Radio btn Value--------</h2>
  <h3>Tools</h3>

  <input type="checkbox" value="c" id="c" v-model="tools" />
  <label for="c">C</label>

  <input type="checkbox" value="c++" id="c++" v-model="tools" />
  <label for="c++">C++</label>

  <input type="checkbox" value="Javascript" id="Javascript" v-model="tools" />
  <label for="Javascript">Javascript</label>

  <h4>Who are you?</h4>
  <input type="radio" value="student" id="student" v-model="who" /><label for="student"
    >Student</label
  >
  <input type="radio" value="developer" id="developer" v-model="who" /><label
    for="developer"
    >Developer</label
  >

  <p>Selected Tools: {{ tools }}</p>
  <p>I Am a {{ who }}</p>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      email: "samirsadek@1009.com",
      inputEmail: null,
      inputPass: null,
      mobile: 1020,
      who: null,
      count: 0,
      tools: [],
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
    getInputValue() {
      console.log("Values", this.inputEmail, this.inputPass);
    },
  },
};
</script>
<style scoped>
h1 {
  color: brown;
}
</style>
