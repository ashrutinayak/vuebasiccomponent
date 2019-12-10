<template>
  <div>
    <ul>
      <li v-for="Titles in title" :key="Titles">
        <a href="www.google.com">{{ Titles }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: ["Home", "about", "contact"]
    };
  }
};
</script>

<style scoped>
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
