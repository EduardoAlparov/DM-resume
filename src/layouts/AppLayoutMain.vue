<template>
  <div class="app-layout-main">
    <AppLayoutHeader />

    <slot class="slot-class"/>
  </div>
</template>
<script>
import AppLayoutHeader from './AppLayoutHeader.vue';
export default {
  name: "AppLayoutMain",
  components: {
    AppLayoutHeader
  },
}
</script>
<style lang="scss" scoped>
.app-layout-main {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.slot-class {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}
</style>
