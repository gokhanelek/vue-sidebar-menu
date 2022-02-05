<template>
  <Navbar />
  <Home />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./view/Home.vue";

export default {
  components: {
    Navbar,
    Home,
  },
};
</script>