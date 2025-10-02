<script setup lang="ts">
import BadPositionWithTeleport from './BadPositionWithTeleport.vue'
import KeyboardFocus from './KeyboardFocus.vue'
</script>

<template>
  <KeyboardFocus />
  <hr />
  <BadPositionWithTeleport />
</template>

<style>
body {
  padding: 2rem;
}

p {
  width: 100%;
  max-width: 100%;
}
</style>
