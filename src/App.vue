<script setup>
import NavHeader from "./components/NavHeader.vue";
import CardContainer from "./components/CardContainer.vue";
import Quote from "./components/Quote.vue"
</script>

<template>
  <div class="m-0 p-0 w-full flex flex-col justify-start items-center">
    <nav-header class="w-full"></nav-header>
    <quote></quote>
    <card-container class="max-w-3xl w-full"></card-container>
  </div>
</template>