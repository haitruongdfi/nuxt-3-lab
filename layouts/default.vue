<template>
  <div>
    <AppHeader />
    <h2>Route: {{ $route.name }}</h2>
    <slot />
    <AppFooter />
  </div>
</template>
<script setup>
// const route = useRoute();
// console.log("current name", route.name);
</script>
