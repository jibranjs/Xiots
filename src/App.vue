<script setup>

import BasicButton from './components/BasicComponent/BasicButton.vue';
const headingId = "color";
const okay = false;
</script>

<template>
  <header>
    <div>
      <h1 :class="headingId"> {{ okay ? 'Yes' : 'No' }}</h1>
      <BasicButton>Testing</BasicButton>
    </div>
  </header>

</template>

<style>
.color{
  color: #0F8FFF;
}
</style>

