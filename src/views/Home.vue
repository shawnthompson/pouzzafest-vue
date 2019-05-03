<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>Pouzzafest 2019</h1>
    <ul>
    <li v-for="band in bands" :key="band.id">
      {{ band }}
    </li>
    </ul>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
import data from "../data/data.json";
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  // components: {
  //   HelloWorld
  // },
  computed: {
    bands() {
      return data.bands.map((item) => {
        return item.bandName;
      })
    }
  }
};
</script>
<style scoped lang="scss">
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
