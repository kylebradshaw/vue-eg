<template>
  <div>
    <h2>THIS IS THE ABOUT {{origin}}</h2>
    <router-link v-if="origin" to="Hello">Go Home</router-link>
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
      this.origin = (this.$router.query.origin) ? 'PAGE' : 'COMPONENT';
      this.origin = 'WAT?!';
    },
  };
</script>
