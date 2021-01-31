<template>
  <div>
    <!-- <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
    <h2 v-for="fullName in fullNames" :key="fullName">
      {{ fullName.first }} {{ fullName.last }}
    </h2>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h4 v-for="movie in actor.movies" :key="movie">{{ movie }}</h4>
    </div>
    <h2 v-for="(value, key, index) in myInfo" :key="value">
      {{ key }} {{ index }} {{ value }}
    </h2> -->
    <h2>{{ add(10, 15, 13) }}</h2>
    <h2>Multiply Method: {{ multiply(7) }}</h2>
    <h2>{{ name }}</h2>
    <button v-on:click="changeName('Superman'), increment(1)">
      Change Name
    </button>
    <h2>{{ count }}</h2>
    <button @click="increment(1)">Increment by 1</button>
    <button @click="decrement(1)">Decrement by 1</button>
    <button @click="increment(5)">Increment by 5</button>
    <button @click="decrement(5)">Decrement by 5</button>
  </div>
</template>

<script>
export default {
  name: "App",
  // components: {
  //   HelloWorld,
  // },
  data() {
    return {
      count: 0,
      name: "Hamed",
      baseMultiplier: 5,
      num: "hello",
      display: true,
      show: false,
      names: ["Hamed", "Kazeem", "Idris"],
      fullNames: [
        { first: "Hamed", last: "Jimoh" },
        { first: "Kazeem", last: "Raheem" },
        { first: "Jamiu", last: "Saka" },
      ],
      actors: [
        { name: "Di Caprio", movies: ["Titanic", "Wolf of Wall Street"] },
        { name: "Dwayne Johnson", movies: ["Lion King", "Inception"] },
      ],
      myInfo: {
        name: "Hameed",
        role: "Frontend Developer",
        stack: "ReactJS",
      },
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return this.baseMultiplier * num;
    },
    increment(num) {
      return (this.count += num);
    },
    decrement(num) {
      return (this.count -= num);
    },
    changeName(name) {
      return (this.name = name);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.italics {
  font-style: italic;
}

.soldout {
  color: red;
}
.new {
  color: cyan;
}
</style>
