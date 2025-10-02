<script setup lang="ts">
import { ref } from 'vue'
import VueSelect from 'vue3-select-component'

const select1 = ref('')
</script>

<template>
  <h2>Option list not open when focusing with tab, or using arrow keys</h2>

  <p>First, focus this input:</p>
  <input placeholder="First input" />

  <p>Then, press tab to focus this select:</p>
  <VueSelect
    v-model="select1"
    :options="[
      { label: 'A Wizard of Earthsea', value: 'wizard_earthsea' },
      { label: 'Harry Potter and the Philosopher\'s Stone', value: 'harry_potter', disabled: true },
      { label: 'The Lord of the Rings', value: 'the_lord_of_the_rings' },
    ]"
  />

  <p>
    <strong>Expected behavior:</strong> the option list is open, or at least can ben open with arrow
    keys.
  </p>
  <p>
    <strong>Actual behavior:</strong> the option list stays hidden until you start typing in the
    search field.
  </p>
</template>
