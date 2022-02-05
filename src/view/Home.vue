<template>
  <section class="home">
    <div class="text">Dashboard Sidebar</div>
  </section>
</template>

<style>
.home {
  position: absolute;
  top: 0;
  top: 0;
  left: 250px;
  height: 100vh;
  width: calc(100% - 250px);
  background-color: var(--body-color);
  transition: var(--tran-05);
}
.home .text {
  font-size: 30px;
  font-weight: 500;
  color: var(--text-color);
  padding: 12px 60px;
}

.dark .home .text {
  color: var(--text-color);
}

</style>