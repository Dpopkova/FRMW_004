<template>
  <div id="app">
    <input placeholder="Основание" v-model="base" />
    <p><input placeholder="Степень" v-model="power" /> </p>

    <list-item
      v-for="index in Number(power)"
      :key="index"
      :power="Number(index)"
      :base="Number(base)"
    />
  </div>
</template>

<script>
import ListItem from "./components/ListItem.vue";

export default {
  name: "App",
  components: {
    ListItem
  },
  data: () => ({
    power: "",
    base: ""
  })
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: black;
  margin-top: 30px;
}
</style>
