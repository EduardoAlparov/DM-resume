<template>
    <component
        :is="layout"
    >
        <slot/>
    </component>
</template>
<script>
const defaultLayout = 'AppLayoutDefault';

export default {
  name: 'AppLayout',
  computed: {
    layout() {
      const layout =  defaultLayout;
      return () => import(`@/layouts/${layout}.vue`);
    },
  },
}
</script>
