<script setup>
let books = [
  {
    id: 1,
    title: "History of Europe",
    cover:
      "https://printpress.cmsmasters.net/default/wp-content/uploads/sites/11/2019/05/printpress-product-6-540x861.jpg",
    isRead: true,
    isbn: "0-395-07157-8",
    author: "Daniel Trejo",
  },
  {
    id: 2,
    title: "Penguin Classics",
    cover:
      "https://printpress.cmsmasters.net/default/wp-content/uploads/sites/11/2019/05/printpress-product-2-540x861.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Daniel Trejo, Jon Snow",
  },
  {
    id: 3,
    title: "Becoming",
    cover:
      "https://printpress.cmsmasters.net/default/wp-content/uploads/sites/11/2019/05/printpress-product-7-540x861.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Daniel Trejo",
  },
  {
    id: 4,
    title: "Sonnets",
    cover:
      "https://printpress.cmsmasters.net/default/wp-content/uploads/sites/11/2019/05/printpress-product-5-540x861.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Daniel Trejo",
  },
]
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
      <div class="books-list">
        <div class="book">
          <div class="book-cover">
            <img
              src="https://printpress.cmsmasters.net/default/wp-content/uploads/sites/11/2019/05/printpress-product-7-540x861.jpg" />

            <button>
              <i class="fa-solid fa-eye"></i>
              <span>Ainda não li</span>
            </button>
          </div>
          <div class="book-details">
            <p class="book-author">Daniel Trejo</p>
            <h3 class="book-title">History of Europe</h3>
            <p><i class="fa-solid fa-hashtag icon"></i> 0-395-07157-8</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
