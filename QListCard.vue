<template>
  <ul>
    <li
      v-for="card in cards"
      :key="card.id"
    >
      <slot :card="card" />
    </li>
  </ul>
</template>

<script lang="ts" setup>
import { defineProps } from 'vue';

// Definindo as propriedades do componente
defineProps<{
  cards: { 
    id: string; // A propriedade id deve ser do tipo string
    courseName: string;
    rating: number;
    fullPrice: string;
    offeredPrice: string;
    discount: string;
    kind: string;
    level: string;
    iesLogo: string;
    iesName: string;
  }[];
}>();
</script>

<style scoped>
/* Adicione estilos aqui, se necessário */
</style>
