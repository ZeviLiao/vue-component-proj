<template>
  <div>
    hello
    {{ value }}
    <button @click="handleAddOne">+1</button>
  </div>
</template>

<script>
export default {
  props: ["value"],
  data() {
    return {};
  },
  methods: {
    handleAddOne() {
      let val = this.value + 1;
      this.$emit("onAdd", val);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>