<template>
  <span class="supprt-icon" :class="iconCls"></span>
</template>
<script>
export default {
  name: "support-icon",
  props: {
    size: {
      type: Number
    },
    type: {
      type: Number
    }
  },
  computed: {
    iconCls() {
      const classMap = [
        "decrease",
        "discount",
        "special",
        "invoice",
        "guarantee"
      ];
      return `icon-${this.size} ${classMap[this.type]}`;
    }
  }
};
</script>
<style lang="stylus" scoped>
@import '~common/stylus/mixin'
.support-ico
  display inline-block
  background-repeat no-repeat
</style>