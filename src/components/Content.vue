<template>
  <div class="content"></div>
</template>
<script>
import MoviceItem from "./MoviceItem";
export default {
  name: "Content",
  data() {
    return {};
  },
  props: {
    moviceList: {}
  },
  components: {
    MoviceItem
  }
};
</script>
<style lang="">
</style>
