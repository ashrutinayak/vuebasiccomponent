<template>
  <div>
    <ul>
      <li v-for="Titles in title" :key="Titles">
        <a href="www.google.com">{{ Titles }}</a>
      </li>
    </ul>
    <h3 v-on:click="changename()">{{name}}</h3>
  </div>
</template>

<script>
import { bus } from "../main";
export default {
  props: ["name"],
  data() {
    return {
      title: ["Home", "about", "contact"]
    };
  },
  methods: {
    changename: function() {
      //   this.$emit("changename", "Testing Demo");
      this.name = "Testing";
      bus.$emit("changename", "Testing");
    }
  }
};
</script>

<style scoped>
h3 {
  text-align: center;
}
ul {
  list-style-type: none;
  background: #222;
  padding: 10px;
}

li {
  text-align: center;
  display: inline-block;
  margin: 0 10px;

  color: #aaa;
}

a {
  color: #42b983;
}
</style>
