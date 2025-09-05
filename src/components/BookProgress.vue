<script setup>
import { computed } from 'vue';

   const props = defineProps(['books']);

   const booksRead = computed(() => {
    return props.books.filter((book) => book.isRead).length;
   });
</script>

<template>
     <div class="books-read">
        <label for="progress">Seu progresso</label>
        <br>
        <progress value="50" max="100"></progress>
        <p>{{ `${booksRead} de ${books.length} livros lidos` }}</p>
    </div>
</template>