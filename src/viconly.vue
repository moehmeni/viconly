
<template>
  <div
    :style="{ fontSize: size + 'rem', color }"
    class="viconly-icon-container"
  >
    <i
      v-if="!bulk"
      :class="{
        icbo: bold,
        icli: light,
        ['iconly-' + icon]: true,
      }"
    >
    </i>
    <span v-else :class="{ ['iconlyBulk-' + icon]: true }">
      <span class="path1"></span>
      <span class="path2"></span>
    </span>
  </div>
</template>

<script>
import "@/iconly/style.css";
import "@/iconly/bulk-style.css";
export default /*#__PURE__*/ {
  name: "Viconly", // vue component name
  props: {
    icon: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: "#ffffff",
    },
    bold: {
      type: Boolean,
      default: false,
    },
    light: {
      type: Boolean,
      default: false,
    },
    bulk: {
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
[class^="iconlyBulk-"],
[class*=" iconlyBulk-"] {
  position: relative;
}
[class^="iconlyBulk-"] .path2,
[class*=" iconlyBulk-"] .path2 {
  position: absolute;
  right: 0;
}
</style>
