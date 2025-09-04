<script setup>

import { ref, reactive } from 'vue';
import Progress from './components/Progress.vue';

// ref para primitivos (números, strings, dentre outros)
let count = ref(0);

// reactive para objetos (é uma convenção)
let courses = reactive([
  {
    title: "JavaScript",
    done: true,
  },
  {
    title: "React",
    done: false,
  },
  {
    title: "Vue",
    done: true,
  },
]);

let newCourse = { done: false };

function increment() {
  count.value++;
}

function addCourse() {
  courses.push(newCourse);
  newCourse = { done: false };
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
    <button @click="addCourse()">Adicionar</button>

    <Progress :courses="courses"></Progress>

  </div>
</template>

<style scoped></style>
