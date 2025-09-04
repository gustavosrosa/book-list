<script setup>
    import { computed } from 'vue';

    const props = defineProps(['courses']);

    const coursesDone = computed(() => {
        // Precisa usar o props no script, no template nao precisa
        return props.courses.filter((course) => course.done).length;
    });
</script>

<template>
    <div>
        {{ `${coursesDone} cursos completos de um total de ${courses.length}` }}
    </div>
</template>