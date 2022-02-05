<template>
  <div class="menu-bar">
    <div class="menu">
      <SearchBox />
      <MenuList />
    </div>
    <div class="bottom-content">
      <Logout />
      <Mode />
    </div>
  </div>
</template>

<script>
import SearchBox from "./SearchBox.vue";
import MenuList from "./MenuList.vue";
import Logout from "./Logout.vue";
import Mode from "./Mode.vue";

export default {
  components: {
    SearchBox,
    MenuList,
    Logout,
    Mode,
  },
};
</script>

<style>
.menu-bar {
  height: calc(100% - 55px);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow-y: scroll;
}
.menu-bar::-webkit-scrollbar {
  display: none;
}
.menu {
  margin-top: 40px;
}
</style>