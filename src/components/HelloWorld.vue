<template>
  <div class="hello">
    <h1 v-once>{{ msg }}</h1>
    <span v-bind:title="message">
      Hover your mouse over me for a few seconds to see my dynamically bound
      title!
    </span>
    <br />
    <span v-if="seen">Now you see me</span>
    <br />
    <div>
      <input v-model="newCat" />
      <button v-on:click="addKitty">
        + ADD
      </button>
      <br />
      <button v-on:click="count++">You clicked me {{ count }} times.</button>
      <br />
      <ul>
        <li v-for="(cat, index) in cats" :key="index">{{ cat.name }}</li>
      </ul>
    </div>
    <br />
    <div id="app">
      <p>{{ message2 }}</p>
      <button v-on:click="reverseMessage">Reverse Message</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      message: "You loaded this page on " + new Date().toLocaleString(),
      seen: true,
      message2: "Hello Vue.js!",
      count: 0,
      cats: [{ name: "chat" }, { name: "petitchat" }, { name: "paté" }],
    };
  },
  methods: {
    reverseMessage: function() {
      this.message2 = this.message2
        .split("")
        .reverse()
        .join("");
    },
    addKitty: function() {
      return this.cats.push(this.newCat);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 20px 0 0;
}
</style>
