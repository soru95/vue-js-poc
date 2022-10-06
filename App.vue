<template>
  <div id="app">
    <h1>Custom Vue.js Select Component</h1>
    <CustomSelect
      :options="['go', 'python', 'rust', 'javascript']"
      :default="'go'"
      class="select"
      @input="alert(displayToKey($event))"
    />
  </div>
</template>

<script>
import CustomSelect from "./components/CustomSelect.vue";

export default {
  components: {
    CustomSelect,
  },
};
</script>

<style lang="scss">
*,
*::before,
*::after {
  box-sizing: border-box;
}

#app {
  max-width: 400px;
  margin: 0 auto;
  line-height: 1.4;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

h1 {
  text-align: center;
}
</style>