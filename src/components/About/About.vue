<template>
  <div>
    <h2>THIS IS THE ABOUT {{origin}}</h2>
    <router-link v-if="origin == 'PAGE'" :to="{ path: '/' }">Go back</router-link>
  </div>
</template>

<script>
  export default {
    name: 'about',
    data() {
      return {
        origin: '',
      };
    },
    mounted() {
      this.origin = (this.$route.query.origin) ? 'PAGE' : 'COMPONENT';
    },
  };
</script>
