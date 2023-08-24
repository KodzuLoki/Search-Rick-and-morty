<template>
  <div class="container">
    <!-- Img como titulo -->
    <img v-bind:src="require('./assets/logo-rick-and-morty.png')" alt="">
    <!-- LLamada de componentes -->
    <FilterByStatus />
    <FilterByName />
    <ListCharacters />
    <Pagination />
    <!-- Fin llamada de componentes -->
  </div>
</template>

<script>
require('@/assets/r&m.png')
import ListCharacters from "@/components/ListCharacters";
import FilterByStatus from "@/components/FilterByStatus";
import FilterByName from '@/components/FilterByName.vue';
import Pagination from '@/components/Pagination.vue';
export default {
  name: "App",
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName,
    Pagination,
  },
};
</script>

<style lang="scss">
:root {
  --background-body: #24282f;
  --background-card: #7216eb;
  --text-white: #fff;
  --text-gray: #ffffff;
  --text-orange: #09a746;
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  background-color: var(--background-body);
  background-image:url('~@/assets/r&m.png');
  background-size: contain;
  backdrop-filter: initial;
  color: var(--text-white);
  font-family: "segoe UI", Verdana, Geneva, Tahoma, sans-serif;
}
h1 {
  margin-bottom: 2rem;
  text-align: center;
}
.container {
  width: 980px;
  max-width: 90%;
  margin: 2rem auto;
}
img {
  width: 100%;
}
</style>
