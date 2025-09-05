<script setup>

    import { reactive } from 'vue'

    let newBook = reactive({
        title: "",
        cover: "",
        isRead: false,
        isbn: "",
        author: "",
    });

</script>

<template>
    <h1>📖 Adicionar Livro</h1>

    <div class="header-btns">
        <button class="btn" @click="$emit('closeAddBook')">
            Fechar x
        </button>
    </div>

    <form class="add-form" @submit.prevent="$emit('addBook', newBook)">

        <div class="form-control">
            <label>Título</label>
            <input required type="text" name="text" placeholder="Adicione o título" v-model="newBook.title" />
        </div>
        <div class="form-control">
            <label>Capa</label>
            <input required type="text" name="cover" placeholder="Adicione o link da imagem de capa"
                v-model="newBook.cover" />
        </div>
        <div class="form-control">
            <label>Autor</label>
            <input type="text" name="author" placeholder="Adicione o autor" v-model="newBook.author" />
        </div>
        <div class="form-control">
            <label>ISBN#</label>
            <input type="text" name="isbn" placeholder="Adicione o ISBN" v-model="newBook.isbn" />
        </div>
        <div class="form-control form-control-check">
            <input type="checkbox" name="readIt" id="readIt" v-model="newBook.isRead" />
            <label for="readIt">Já li o livro</label>
        </div>

        <button type="submit" class="btn btn-block">Salvar livro</button>
    </form>


</template>