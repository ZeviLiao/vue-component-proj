<template>
  <div class="hello">
    <div @click="showHide" class="drop-box gradient">change</div>

    <div v-if="isExpand">
      all
      <div>
        <ul>
          <li>aa</li>
          <li>bb</li>
          <li>cc</li>
        </ul>
      </div>
    </div>
    <div v-else>aa, bb, cc, aa, bb, cc, aa, bb, cc, </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      isExpand: false
    };
  },
  methods: {
    showHide() {
      this.isExpand = !this.isExpand;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.drop-box {
  // width: 30px;
  // height: 30px;
  display: inline-block;
  padding: 5px;
  background: pink;
  // float: right;
  position: absolute;
  right: 0;
}

.gradient {
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 0) 22%,
    rgba(255, 255, 255, 1) 69%
  );
  background: -moz-linear-gradient(
    90deg,
    rgba(255, 255, 255, 0) 22%,
    rgba(255, 255, 255, 1) 69%
  );
  background: -webkit-linear-gradient(
    90deg,
    rgba(255, 255, 255, 0) 22%,
    rgba(255, 255, 255, 1) 69%
  );
  background: -o-linear-gradient(
    90deg,
    rgba(255, 255, 255, 0) 22%,
    rgba(255, 255, 255, 1) 69%
  );
}

.hello {
  width: 200px;
  background: lightblue;
  position: relative;
  padding: 5px;
}
</style>
