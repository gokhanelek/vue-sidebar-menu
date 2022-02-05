<template>
  <li class="">
    <a href="#" @click="logout">
      <i class="bx bx-log-out icon"></i>
      <span class="text nav-text">Logout</span>
    </a>
  </li>
</template>

<script>
export default {
  methods: {
    logout(){
      console.log("Logout")
    }
  },
}
</script>