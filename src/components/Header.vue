<template>
  <header>
    <div class="image-text">
      <span class="image">
        <img src="@/assets/logo.svg" alt="" srcset="" />
      </span>
      <div class="text logo-text">
        <span class="name">Frontend</span>
        <span class="profession">Web Developer</span>
      </div>
    </div>
    <i class="bx bx-chevron-right toggle" @click="sidebarClose"></i>
  </header>
</template>

<script>
export default {
  methods: {
    sidebarClose() {
      const body = document.querySelector("body");
      const sidebar = body.querySelector("nav");
      sidebar.classList.toggle("close");
    },
  },
};
</script>

<style >
header {
  position: relative;
}
.image-text {
  display: flex;
  align-items: center;
}
.image {
  display: flex;
  align-items: center;
  justify-content: center;
}
.image img {
  width: 40px;
  border-radius: 6px;
}
.logo-text {
  display: flex;
  flex-direction: column;
}
.name {
  margin-top: 2px;
  font-size: 18px;
  font-weight: 600;
}
.profession {
  font-size: 16px;
  margin-top: -2px;
  display: block;
}
.toggle {
  position: absolute;
  top: 50%;
  right: -25px;
  transform: translateY(-50%) rotate(180deg);
  height: 25px;
  width: 25px;
  background-color: var(--primary-color);
  color: var(--sidebar-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  cursor: pointer;
  transition: var(--tran-05);
}
.dark header .toggle {
  color: var(--text-color);
}
</style>