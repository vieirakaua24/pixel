<script setup>

import { ref } from "vue";

import Card from "./Card.vue";

import axios from "axios";


const imagens = ref([]);

async function carregarImagens() {

  const res = await axios.get("https://picsum.photos/v2/list?page=2&limit=10");

  imagens.value = res.data;

  console.log(res);

}

carregarImagens();

</script>

<template>

  <section>

    <h2>Inspire-se</h2>

    <section class="cards">

      <Card v-for="img in imagens" :imagem="img.download_url" />

    </section>

  </section>

</template>

<style scoped lang="scss">

.cards {

  display: flex;

  flex-wrap: wrap;

  gap: 1rem;

}

</style>