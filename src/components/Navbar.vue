<template>
  <nav class="sidebar close">
    <Header />
    <MenuBar />
  </nav>
</template>

<script>
import Header from "./Header.vue";
import MenuBar from "./MenuBar.vue";
export default {
  components: {
    Header,
    MenuBar,
  },
};
</script>

<style>
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 250px;
  padding: 10px 14px;
  background: var(--sidebar-color);
  transition: var(--tran-05);
  z-index: 100;
}
.sidebar.close {
  width: 88px;
}
.sidebar li {
  height: 50px;
  list-style: none;
  display: flex;
  align-items: center;
  margin-top: 10px;
}
.sidebar header .image,
.sidebar .icon {
  min-width: 60px;
  border-radius: 6px;
}

.sidebar .icon {
  min-width: 60px;
  border-radius: 6px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
}

.sidebar .text,
.sidebar .icon {
  color: var(--text-color);
  transition: var(--tran-03);
}

.sidebar .text {
  font-size: 17px;
  font-weight: 500;
  white-space: nowrap;
  opacity: 1;
}
.sidebar.close .text {
  opacity: 0;
}
.sidebar.close .toggle {
  transform: translateY(-50%) rotate(0deg);
}

.sidebar.close ~ .home {
  left: 78px;
  height: 100vh;
  width: calc(100% - 78px);
}
</style>