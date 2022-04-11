<script>
import Vue from 'vue';
import Viconly from '@/viconly.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    Viconly
  }
});
</script>

<template>
  <div id="app">
    <viconly />
  </div>
</template>
