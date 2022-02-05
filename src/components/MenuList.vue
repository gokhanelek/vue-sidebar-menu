<template>
  <MenuListItem :menuList="menuList" />
</template>

<script>
import MenuListItem from "./MenuListItem.vue";

export default {
  components: {
    MenuListItem,
  },
  data() {
    return {
      menuList: [
        { id: 1, title: "Dashboard", icon: "bx bx-home-alt" },
        { id: 2, title: "Revenue", icon: "bx bx-bar-chart-alt-2" },
        { id: 3, title: "Notifications", icon: "bx bx-bell" },
        { id: 4, title: "Analytics", icon: "bx bx-pie-chart-alt" },
        { id: 5, title: "Likes", icon: "bx bx-heart" },
        { id: 6, title: "Wallets", icon: "bx bx-wallet" },
      ],
    };
  },
};
</script>