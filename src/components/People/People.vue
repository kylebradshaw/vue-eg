<template>
  <div>
    <h2> People </h2>
    <ul>
      <li v-for="person in people" :style="{backgroundColor: person.color}">
        {{person.name}}, {{person.age}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'people',
    data() {
      return {
        people: [
          {
            name: 'Jacque',
            age: '40',
            color: 'purple',
          },
          {
            name: 'Penelope',
            age: '44',
            color: 'pink',
          },
          {
            name: 'Jordi',
            age: '40',
            color: 'green',
          },
        ],
      };
    },
  };
</script>

<style lang="scss" scoped>
ul {
  width: 300px;
  margin: 0 auto;
  padding: 0;
  li {
    color: #fff;
    font-weight: bold;
    list-style: none;
  }
}
</style>
