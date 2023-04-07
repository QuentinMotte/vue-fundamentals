<template>
  <p v-if="age >= 25">{{ msg }}</p>
  <p v-else>You must be 25years or older to view this message</p>
</template>

<script>
export default {
  name: "Greeting",
  props: ["age"],
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
};
</script>

<style scoped lang="scss">
p:hover {
  color: darken($color: #cc4444, $amount: 15%);
}
</style>
