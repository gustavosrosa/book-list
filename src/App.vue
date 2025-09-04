<script setup>

import { ref, reactive } from 'vue';

// ref para primitivos (números, strings, dentre outros)
let count = ref(0);

// reactive para objetos (é uma convenção)
let courses = reactive([
  {
    title: "JavaScript"
  },
  {
    title: "React"
  },
  {
    title: "Vue"
  },
]);

let newCourse = {};

function increment() {
  count.value++;
}

</script>

<template>
  <div>

    <h1>{{ count }}</h1>
    <button @click="increment">Incrementar</button>

    <ul>
      <li v-for="course in courses" :key="course.title">{{ course.title }}</li>
    </ul>

    <br>

    <input type="text" v-model="newCourse.title">
    <button @click="courses.push(newCourse)">Adicionar</button>

  </div>
</template>

<style scoped></style>
