<script setup>
const runtimeConfig = useRuntimeConfig(); // load everything in nuxt.config.ts
const appConfig = useAppConfig(); // load everything in app.config.ts
console.log(runtimeConfig.apiSecret);
</script>
<template>
  <Title>Nuxt 3 Lab</Title>
  <Meta name="description" content="Description for page" />

  <h1>{{ appConfig.title }}</h1>
  <p>{{ appConfig.theme.colors.primary }}</p>
  <p>{{ runtimeConfig.public.apiBase }}</p>
  <div>
    <h1>ホームページへようこそ</h1>

    <AppAlert> This is an auto-imported component </AppAlert>
  </div>
  <div>
    <ContentDoc path="/sample-rtf" />
    <ContentDoc path="/another-sample-for-content" />
  </div>
</template>
