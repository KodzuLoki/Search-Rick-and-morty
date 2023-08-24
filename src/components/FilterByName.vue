<template>
  <div class="search">
    <input
      type="text"
      placeholder="Introduzca un nombre"
      v-model="name"
      @keyup="filter()"
    />
  </div>
</template>
<script>
import { useStore } from "vuex";
import { ref } from "vue";
export default {
  setup() {
    const store = useStore();
    const name = ref("");

    const filter = () => {
      store.dispatch("filterByName", name.value);
    };
    return {
      name,
      filter,
    };
  },
};
</script>
<style lang="scss">
.search {
  width: 400px;
  margin: 2rem auto 0;
  input {
    height: 53px;
    width: 400px;
    border: none;
    border-radius: 10px;
    padding: 0 0.5rem;
    background: linear-gradient(
      43deg,
      #7216eb,
      #7216eb 100%
    );
    color: cornsilk;
  }
  ::placeholder {
    color: #ffffff;
    text-align: start;
  }
}
</style>