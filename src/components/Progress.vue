<script setup>
    const props = defineProps(['courses']);
</script>

<template>
    <div>
        {{ courses.length }}
    </div>
</template>