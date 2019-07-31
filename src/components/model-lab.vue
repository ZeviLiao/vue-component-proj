<template>
  <div>
    <model-com v-model="pvalue" v-on:onAdd="handleUpdate" />
    {{pvalue}}
  </div>
</template>

<script>
import ModelCom from "./model-com";
export default {
  data() {
    return {
      pvalue: 0
    };
  },
  methods: {
    handleUpdate(val) {
      this.pvalue = val;
    }
  },
  components: {
    ModelCom
  }
};
</script>

<style lang="scss" scoped>
</style>