<template>
    <header>            
            <img src="@/assets/cvc.png">
            <menu-bar class="menu_bar"></menu-bar>
            <user class="user"></user>
    </header>
</template>

<script>
import MenuBar from "@/components/header/MenuBar.vue";
import User from "@/components/header/User.vue";

export default {
  components: {
    MenuBar,
    User
  }
};
</script>


<style scoped>
header {
  background-color: #ffffff;
  border: 1px solid #e5e7e8;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

img {
  width: 61px;
  height: 37px;
}

.menu_bar {
  margin-left: 40px;
}

.user {
  margin-right: 50px;
  flex-grow: 1;
}

@media (max-width: 640px) {
  header {
    flex-flow: column;
    justify-content: center;
  }
  img {
    width: 81px;
    height: 57px;
  }
  .user, .menu_bar{
      margin:0;
  }
}
</style>
