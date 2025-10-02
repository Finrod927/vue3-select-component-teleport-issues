<script setup lang="ts">
import { ref } from 'vue'
import VueSelect from 'vue3-select-component'

const select1 = ref('')
</script>

<template>
  <h2>With teleport="body" and a scrolled page, the list is not correctly positionned</h2>

  <p>Scroll down a "little" to show the VueSelect components</p>
  <div style="height: 600px" />

  <p>1. Open this select, everything is fine:</p>
  <VueSelect
    v-model="select1"
    :options="[
      { label: 'A Wizard of Earthsea', value: 'wizard_earthsea' },
      { label: 'Harry Potter and the Philosopher\'s Stone', value: 'harry_potter', disabled: true },
      { label: 'The Lord of the Rings', value: 'the_lord_of_the_rings' },
    ]"
  />

  <p>
    2. Open this select with `teleport="body"`, the position of the list is wrong, you have to
    scroll up to find it:
  </p>
  <VueSelect
    v-model="select1"
    :options="[
      { label: 'A Wizard of Earthsea', value: 'wizard_earthsea' },
      { label: 'Harry Potter and the Philosopher\'s Stone', value: 'harry_potter', disabled: true },
      { label: 'The Lord of the Rings', value: 'the_lord_of_the_rings' },
    ]"
    teleport="body"
  />

  <p><strong>Expected behavior:</strong> the option list is open, at the correct position.</p>
  <p>
    <strong>Actual behavior:</strong> the option list is open, but at its position if the page was
    not scrolled.
  </p>

  <div style="height: 600px" />
</template>
