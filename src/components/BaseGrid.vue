<script setup>
const props = defineProps({
  childComponent: Object,
  iterable: Array,
});

// eslint-disable-next-line no-console
console.log(props.iterable.length);

</script>

<template>
<q-page class='q-pa-lg'>
  <div class="flex wrap q-gutter-lg justify-center">
    <div v-for="item in props.iterable" :key="item.id">
      <component :is="props.childComponent" v-bind="item" />
  </div>
  </div>
</q-page>
</template>
