<template>
  <div id="msg">
    <!-- <p>{{msg}}</p> -->
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <h2 v-for="msges in msg" :key="msges">{{msges}}</h2>
  </div>
</template>

<script>
export default {
  props: ["msg"],
  data() {
    return {
      //   msg: ["Hello vue!!!!!!!!!!!!!!!", "Good Morning", "Testing"]
    };
  },
  //   Life cycle hook
  beforeCreate() {
    alert("BeforeCreate");
  },
  created() {
    alert("Created");
  },
  beforeMount() {
    alert("BeforeMount");
  },
  mounted() {
    alert("Mounted");
  },
  beforeUpdate() {
    alert("BeforeUpdate");
  },
  update() {
    alert("Update");
  }
};
</script>

<style scoped>
h2 {
  display: block;
}
ul {
  list-style-type: none;
  background: #222;
  padding: 10px;
}

li {
  display: inline-block;
  margin: 0 10px;

  color: #aaa;
}

a {
  color: #42b983;
}
footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 97%;
  background: #222;
  color: #aaa;
  text-align: center;
  margin: 10px;
  padding: 10px;
}
</style>
