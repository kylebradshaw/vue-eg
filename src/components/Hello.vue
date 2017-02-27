<template>
  <div>
    <about-cmp></about-cmp>
    <router-link :to="{ path: '/about', query: { origin: 'page' }}">About Page</router-link>
    &nbsp;|&nbsp;
    <router-link :to="{ path: '/people' }">People</router-link>

  </div>
</template>

<script>
import About from './About/About';

export default {
  name: 'hello',
  components: {
    'about-cmp': About,
  },
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
