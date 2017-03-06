<template>
  <div>
    <h2> People | Pets </h2>
    <button @click="clicked">CLICK ME</button>
    <ul>
      <li v-if="show === 'people'" v-for="person in people" :style="{backgroundColor: person.color}">
        {{person.name}}, {{person.age}}
      </li>
      <li v-if="show === 'pets'" v-for="pet in pets" :style="{backgroundColor: pet.color}">
        {{pet.name}}, {{pet.age}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'people',
    methods: {
      clicked() {
        this.show = (this.show === 'people') ? 'pets' : 'people';
      },
    },
    data() {
      return {
        show: 'people',
        pets: [
          {
            name: 'Minette',
            age: 6,
            color: 'orange',
          },
          {
            name: 'Porter',
            age: 5,
            color: 'black',
          },
          {
            name: 'MJ',
            age: 10,
            color: 'maroon',
          },
        ],
        people: [
          {
            name: 'Jacqueline',
            age: '40',
            color: 'purple',
          },
          {
            name: 'Penelope',
            age: '44',
            color: 'pink',
          },
          {
            name: 'Max',
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
