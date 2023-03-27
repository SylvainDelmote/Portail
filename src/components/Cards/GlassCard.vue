<script setup>
const props = defineProps({
  childComponent: Object,
});
</script>

<template>
  <q-card class="glassCard">
    <component :is =props.childComponent />
  </q-card>

</template>

<style>

.glassCard{
background: rgba( 255, 255, 255, 0.25 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 5.5px );
-webkit-backdrop-filter: blur( 5.5px );
border-radius: 10px;
border: 1px solid rgba( 255, 255, 255, 0.18 );
}

</style>
