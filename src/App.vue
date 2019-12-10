<template>
  <div>
    <app-header v-bind:name="name" v-on:changename="updatename($event)"></app-header>
    <app-msg v-bind:msg="msg"></app-msg>
    <app-footer v-bind:name="name"></app-footer>
  </div>
</template>

<script>
import Titles from "./component/header.vue";
import footer from "./component/footer.vue";
import msg from "./component/dashboard.vue";
export default {
  components: { "app-header": Titles, "app-footer": footer, "app-msg": msg },
  data() {
    return {
      msg: ["Hello vue!!!!!!!!!!!!!!!", "Good Morning", "Testing"],
      name: "Demo"
    };
  },
  methods: {
    updatename: function(nameupdate) {
      this.name = nameupdate;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#msg {
  align-content: center;
}
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
