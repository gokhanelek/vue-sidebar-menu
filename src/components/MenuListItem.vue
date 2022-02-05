<template>
  <ul class="menu-links">
    <li v-for="item in menuList" :key="item.id" class="nav-link">
      <a href="#">
        <i class="icon" :class="item.icon"></i>
        <span class="text nav-text">{{ item.title }}</span>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  props: ["menuList"],
};
</script>
<style>
li a {
  list-style: none;
  height: 100%;
  background-color: transparent;
  display: flex;
  align-items: center;
  height: 100%;
  width: 100%;
  border-radius: 6px;
  text-decoration: none;
  transition: var(--tran-03);
}
li a:hover {
  background-color: var(--primary-color);
}
li a:hover .icon,
li a:hover .text {
  color: var(--sidebar-color);
}
.dark li a:hover .icon,
li a:hover .text {
  color: var(--text-color);
}
</style>