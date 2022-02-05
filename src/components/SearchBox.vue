<template>
  <li class="search-box">
    <i class="bx bx-search icon" @click="search"></i>
    <input type="text" placeholder="Search..." />
  </li>
</template>

<script>
export default {
  methods: {
    search() {
      const body = document.querySelector("body"),
        sidebar = body.querySelector("nav");
      sidebar.classList.remove("close");
    },
  },
};
</script>

<style>
.search-box {
  border-radius: 6px;
  background-color: var(--primary-color-light);
  cursor: pointer;
  transition: var(--tran-05);
}
.search-box input {
  height: 100%;
  width: 100%;
  outline: none;
  border: none;
  background-color: var(--primary-color-light);
  color: var(--text-color);
  border-radius: 6px;
  font-size: 17px;
  font-weight: 500;
  transition: var(--tran-05);
}
</style>