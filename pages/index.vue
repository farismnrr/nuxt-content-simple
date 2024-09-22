<script setup lang="ts">
const { data } = await useAsyncData("home", () => queryContent("/").findOne());
</script>
<template>
    <div>
        <h1>{{ data.title }}</h1>
        <p>{{ data.description }}</p>
    </div>
</template>
