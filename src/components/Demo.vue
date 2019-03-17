<template>
  <div class="hello">
    <Banner :position="position">Banner at {{position}}</Banner>
    <p>{{msg}}</p>
    <button @click="onTop">Top</button>
    <button @click="onBottom">Bottom</button>
  </div>
</template>

<script>
import Banner from "./Banner.vue";

export default {
  name: "Demo",
  props: {
    msg: String
  },
  data() {
    return {
      position: "top"
    };
  },
  components: {
    Banner
  },
  methods: {
    onTop() {
      this.position = "top";
    },
    onBottom() {
      this.position = "bottom";
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
button {
  border: 1px solid #000;
  margin: 10px;
  cursor: pointer;
  text-decoration: none;
}
</style>
