<script lang="ts" setup>
import { computed } from 'vue'
import type { PropType } from 'vue'
import type { Animal } from '../types'
import { calculateAgeInYears } from '../composables/helpers'

const props = defineProps({
  animals: {
    type: Array as PropType<Array<Animal>>,
    required: true,
  },
})

const animalsSortedByName = computed(() => props.animals.slice().sort((animalA, animalB) => animalA.weight - animalB.weight))
</script>

<template>
  <table class="table-auto">
    <thead>
      <tr>
        <th>Index</th>
        <th>Species</th>
        <th>Gender</th>
        <th>Age (yrs)</th>
        <th>Weight (kg)</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="({ id, species, gender, birthdate, weight }, animalIndex) in animalsSortedByName" :key="id" class="hover:bg-gray-200">
        <td>{{ animalIndex + 1 }}</td>
        <td>{{ species }}</td>
        <td>{{ gender }}</td>
        <td>{{ birthdate }}</td>
        <td>{{ weight }}</td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
table {
  @apply text-left
}

td {
  @apply w-40
}

tr {
  @apply border-b-2
}
</style>
