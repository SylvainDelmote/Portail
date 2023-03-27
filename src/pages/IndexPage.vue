<script setup>
import BaseGrid from 'src/components/BaseGrid.vue';
import BaseCard from 'src/components/Cards/BaseCard.vue';
import data from '../data/apps.json';
</script>

<template>
  <q-page padding class="flex flex-center">
    <div class="glassCard">
     <BaseGrid :child-component= BaseCard  :iterable="data"  />
     </div>
  </q-page>
</template>

<style>
.glassCard{
background: rgba(255, 255, 255, 0.16);
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 5.5px );
-webkit-backdrop-filter: blur( 5.5px );
border-radius: 10px;
border: 1px solid rgba( 255, 255, 255, 0.18 );
}

</style>
