<script setup>

    const props = defineProps(['books']);

</script>

<template>
    <div class="books-list">
        <div v-for="book in books" :key="book.isbn" class="book">
          <div class="book-cover">
            <img :src="book.cover" />

            <button>
              <i class="fa-solid fa-eye"></i>
              <span>Ainda não li</span>
            </button>
          </div>
          <div class="book-details">
            <p class="book-author">{{ book.author}} </p>
            <h3 class="book-title">{{ book.title }}</h3>
            <p><i class="fa-solid fa-hashtag icon"></i>{{ book.isbn }}</p>
          </div>
        </div>
      </div>
</template>