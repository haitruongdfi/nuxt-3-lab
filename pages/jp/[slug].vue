<template>
  <h2>Path: {{ $route.params }}</h2>
  <div
    dfi-career-detail-page-container=""
    dfi-career-detail-page-container-bg=""
    class="image sd"
  >
    <!-- <pre>{{ data.body }}</pre> -->
    <div v-for="item in data.body" v-if="data.body">
      <h2>{{ item.title }}</h2>
      <p v-for="p in item.content">
        {{ p }}
      </p>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
const route_content = "/jp/" + route.params.slug;
const { data } = await useAsyncData("jp", () =>
  queryContent(route_content).findOne()
);
</script>
