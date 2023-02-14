<template>
  <div id="app">
    <h1>Book Show | Hide</h1>
    <div v-if="showBook">
      <p>{{ title }} - {{ author }} - {{ age }}</p>
    </div>
    <button :class="active ? 'text-red' : 'text-green'" @click="toggleShowBook">
      <span v-if="showBook">Hide Book</span>
      <span v-else>Show Book</span>
    </button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      buttonClass: "text-green",
      active: true,
      showBook: true,
      title: "O'tgan kunlar",
      author: "O'tkir Hoshimov",
      age: 1999,
    };
  },
  methods: {
    toggleShowBook() {
      this.showBook = !this.showBook;
      this.active = !this.active;
    },
  },
};
</script>
<style>
.text-red {
  font-weight: bold;
  color: red;
  background: rgb(124, 194, 124);
}
.text-green {
  font-weight: bold;
  color: green;
  background-color: rgb(233, 130, 205);
}
button {
  padding: 10px 10px;
  cursor: pointer;
  border: 1px solid rebeccapurple;
  border-radius: 10px;
}
</style>
