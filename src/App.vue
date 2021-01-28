<template>
  <div>
    <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
    <h2 v-for="fullName in fullNames" :key="fullName">
      {{ fullName.first }} {{ fullName.last }}
    </h2>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h4 v-for="movie in actor.movies" :key="movie">{{ movie }}</h4>
    </div>
    <h2 v-for="(value, key, index) in myInfo" :key="value">
      {{ key }} {{ index }} {{ value }}
    </h2>
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
