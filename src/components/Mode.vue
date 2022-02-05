<template>
  <li class="mode">
    <div class="sun-moon">
      <i class="bx bx-moon icon moon"></i>
      <i class="bx bx-sun icon sun"></i>
    </div>
    <span class="mode-text text">{{ modeTxt }}</span>

    <div class="toggle-switch" @click="changeMode">
      <span class="switch"></span>
    </div>
  </li>
</template>

<script>
export default {
  data() {
    return {
      modeTxt: "Light mode",
    };
  },
  methods: {
    changeMode() {
      const body = document.querySelector("body");
      body.classList.toggle("dark");

      if (body.classList.contains("dark")) {
        this.modeTxt = "Light mode";
      } else {
        this.modeTxt = "Dark mode";
      }
    },
  },
};
</script>

<style>
.mode {
  border-radius: 6px;
  background-color: var(--primary-color-light);
  position: relative;
  transition: var(--tran-05);
}
.sun-moon {
  height: 50px;
  width: 60px;
}
.sun-moon i {
  position: absolute;
}
.sun-moon i.sun {
  opacity: 0;
}
.toggle-switch {
  position: absolute;
  right: 0;
  height: 100%;
  min-width: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 6px;
  cursor: pointer;
}
.switch {
  position: relative;
  height: 22px;
  width: 40px;
  border-radius: 25px;
  background-color: var(--toggle-color);
  transition: var(--tran-05);
}
.switch::before {
  content: "";
  position: absolute;
  height: 15px;
  width: 15px;
  border-radius: 50%;
  top: 50%;
  left: 5px;
  transform: translateY(-50%);
  background-color: var(--sidebar-color);
  transition: var(--tran-04);
}
.dark .switch::before {
  left: 20px;
}
.dark .mode .sun-moon i.sun {
  opacity: 1;
}
.dark .mode .sun-moon i.moon {
  opacity: 0;
}
</style>