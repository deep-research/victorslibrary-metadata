<template lang="pug">
  h1 {name}
</template>

<script lang="ts">
  export let name: string = 'hello world';
</script>

<style lang="scss">
  h1 {
    color: $custom-color;
  }
</style>
