

<template>
  <div id="app">
    <div v-for="(icon, index) in icons" :key="index">
      <viconly v-bind="icon" />
      <mark v-text="getStyle(icon)"></mark>
      <span> {{ icon.name }}</span>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import Viconly from "@/viconly.vue";

export default Vue.extend({
  name: "ServeDev",
  components: {
    Viconly,
  },
  data() {
    return {
      icons: [
        {
          name: "Heart",
          bulk: true,
          color: "black",
          size: "8rem",
        },
        {
          name: "Home",
          color: "black",
          size: "8rem",
        },
        {
          name: "Home",
          broken: true,
          color: "black",
          size: "8rem",
        },
        {
          name: "Home",
          bold: true,
          color: "black",
          size: "8rem",
        },
      ],
    };
  },
  methods: {
    getStyle(icon) {
      let notStyleKeys = ["name", "color", "size"];
      for (let key of Object.keys(icon)) {
        if (!notStyleKeys.includes(key)) {
          return key;
        }
      }
    },
  },
});
</script>

<style scoped>
#app {
  height: 90vh;
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  justify-content: space-around;
  align-items: center;
  padding: 0 10rem;
}
#app div {
  text-align: center;
}
</style>
