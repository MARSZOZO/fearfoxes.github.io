<template>
  <div id="app">
    <vue-book-effects class="book-effects" :flip-duration="2000" :pages="pages"></vue-book-effects>
  </div>
</template>

<script>
import VueBookEffects from "vue-book-effects";
export default {
  name: "App",
  components: { VueBookEffects },
  data() {
    return {
      pages: [],
    };
  },
  mounted() {
    setTimeout(() => {
      this.pages = [
          null,
          require("@/assets/обложка.jpg"),
          require("@/assets/1.jpg"),
          require("@/assets/2.jpg"),
          require("@/assets/3.jpg"),
          require("@/assets/4.jpg"),
          require("@/assets/7.jpg"),
          require("@/assets/8.jpg"),
          require("@/assets/9.jpg"),
          require("@/assets/11.jpg"),
          require("@/assets/12.jpg"),
      ]
    }, 1)
  }
};
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}

#app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #333;
  color: #ccc;
  overflow: hidden;
}

.book-effects .viewport {
  width: 95vw;
  height: calc(100vh - 50px - 40px);
}

.book-effects .bounding-box {
  box-shadow: 0 0 20px #000;
}
</style>
