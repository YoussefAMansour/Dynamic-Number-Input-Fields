<template>
  <VRow>
    <VCol cols="12" md="1">
      <VLabel>Add Input</VLabel>
      <VBtn variant="outlined" @click="showSelect = !showSelect">Bulk Hash</VBtn>
    </VCol>

    <!-- Conditional VSelect for choosing the number -->
    <VCol cols="12" md="2" v-if="showSelect">
      <VLabel>Number of Input</VLabel>
      <VSelect
          v-model="selectedNumber"
          :items="numbers"
          clearable
          placeholder="3"/>
    </VCol>

    <!-- Dynamically generated number input fields based on the selected number -->

    <VCol cols="12" md="2" v-for="index in inputFieldsCount" :key="index">
      <VLabel>Input Number {{ index }}</VLabel>
      <VTextField
          v-model="inputValues[index - 1]"
          placeholder="3.1415"
          type="number"
      />
    </VCol>

    <!-- Display the array of inputs -->
    <VCol cols="12" md="12">
      <p>Entered Values: {{ JSON.stringify(inputValues.filter(value => value !== '')) }}</p>
    </VCol>
  </VRow>
</template>

<script setup>
import {ref, watch} from 'vue'

const showSelect = ref(false)
const selectedNumber = ref(null)
const numbers = ref(Array.from({length: 10}, (_, i) => i + 1))
const inputValues = ref([])
const inputFieldsCount = ref(0)

watch(selectedNumber, newValue => {
  inputFieldsCount.value = Number.isInteger(newValue) && newValue > 0 ? newValue : 0
  if (newValue === null) {
    inputValues.value = []
  }
})
</script>