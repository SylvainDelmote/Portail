<script setup>
import { computed } from 'vue';

const props = defineProps(
  {
    color: {
      type: String,
      default: 'warning',
    },

    icon: {
      type: String,
      default: 'print',
    },
    title: {
      type: String,
      default: 'Titre',
    },
    caption: {
      type: String,
      default: 'Soustitre',

    }
    ,

  },
);
const bgColor = computed(() => `bg-${props.color}`);

</script>

<template>

  <q-card bordered class="baseCard shadow-2 q-pa-lg" :class="bgColor"  to="/index">
    <q-card-section horizontal >
      <q-card-section  >
        <q-icon  :name="props.icon"  size="xl" />
      </q-card-section>
      <q-card-section>
        <div class="text-h6">{{ props.title }} </div>
        <div class="text-overline "> {{ props.caption }} </div>
      </q-card-section>
    </q-card-section>
    <q-separator spaced dark inset   />
    <q-card-actions horizontal >
      <q-btn flat > <q-icon name="bookmark" /> </q-btn>
      <q-btn flat > <q-icon name="expand_circle_down" /> </q-btn>
    </q-card-actions>
  </q-card>

</template>

<style scoped lang="scss">
.baseCard{
 border-radius: 3px;
  cursor: pointer;
  opacity: 0.9;
  min-width: 300px;

}
.baseCard:hover{
  opacity: 1;
}

</style>
