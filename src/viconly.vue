
<template>
  <div
    :style="{ fontSize: size + 'rem', color }"
    class="viconly-icon-container"
  >
    <i
      :class="{
        icbo: bold,
        ['iconly-' + icon]: true,
      }"
    ></i>
  </div>
</template>

<script>
import "@/iconly/style.css";
export default /*#__PURE__*/ {
  name: "Viconly", // vue component name
  props: {
    icon: {
      type: String,
      required: true,
      default: "Home",
    },
    color: {
      type: String,
      default: "#ffffff",
    },
    bold: {
      type: Boolean,
      default: false,
    },
    size: {
      type: String,
      default: "0.6",
    },
  },
};
</script>

<style scoped>
.viconly-icon-container {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
