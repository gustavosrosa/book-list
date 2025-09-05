<script setup>

  import BookProgress from './components/BookProgress.vue';
  import Books from './components/Books.vue';
  import { reactive } from 'vue';

  let books = reactive([
    {
      id: 1,
      title: "History of Europe",
      cover:
        "http://books.google.com/books/content?id=Pv1eUCKdP-QC&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api",
      isRead: true,
      isbn: "0-395-07157-8",
      author: "Daniel Trejo",
    },
    {
      id: 2,
      title: "Penguin Classics",
      cover:
        "http://books.google.com/books/content?id=MoS4BgAAQBAJ&printsec=frontcover&img=1&zoom=5&edge=curl&source=gbs_api",
      isRead: false,
      isbn: "0-395-07157-8",
      author: "Daniel Trejo, Jon Snow",
    },
    {
      id: 3,
      title: "Becoming",
      cover:
        "http://books.google.com/books/content?id=CWZw-4UGpJ8C&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api",
      isRead: false,
      isbn: "0-395-07157-8",
      author: "Daniel Trejo",
    },
    {
      id: 4,
      title: "Sonnets",
      cover:
        "http://books.google.com/books/content?id=eHqPaGHO2hIC&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api",
      isRead: false,
      isbn: "0-395-07157-8",
      author: "Daniel Trejo",
    },
  ]);

  function toggleIsRead(id) {
    books.forEach((book) => {
      if (id == book.id) {
        book.isRead = !book.isRead;
      }
    })
  }

</script>

<template>
  <div class="container">
    <h1>📖 Meus Livros</h1>
    <div class="header-btns">
      <button class="btn">
        Adicionar Livro +
      </button>
    </div>

    <div class="books-container">

      <Books @toggleIsRead="toggleIsRead" :books="books"/>

      <BookProgress :books="books"/>
      
    </div>
  </div>
</template>

<style scoped></style>
