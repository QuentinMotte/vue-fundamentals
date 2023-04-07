<template>
  <button type="button" @click="onClickAge">Update Age Event</button>
  <button type="button" @click="ageChangeFN(3)">Update Age CB</button>
  <p>The user is {{ age }} years old</p>
  <p>{{ ageDouble }}</p>
</template>
<script>
export default {
  name: "User",
  props: {
    age: {
      type: Number,
      required: true,
      // default: 20,
      // validator(value) {
      //   return value < 130;
      // },
    },
    ageChangeFN: Function,
  },
  emits: ["age-change"],
  computed: {
    ageDouble() {
      return this.age * 2;
    },
  },
  methods: {
    onClickAge() {
      this.$emit("age-change", 3);
    },
  },
};
</script>
