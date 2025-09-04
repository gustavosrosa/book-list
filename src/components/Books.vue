<script setup>

    const props = defineProps(['books']);

</script>

<template>
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
</template>