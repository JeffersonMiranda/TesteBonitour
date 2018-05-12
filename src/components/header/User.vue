<template>
    <div>

    <img src="@/assets/photo_profile.jpg" alt="">
    <p>Clayton Augusto</p>
    <a class="linkMenu" @click="clickMenu()">&#780;</a>
      <ul class="menu" v-bind:style="{display: this.menuDisplay}">
        <li><a> Meu perfil</a> </li>
        <li><a> Parâmetros </a></li>
        <li><a> Sair </a></li>
      </ul> 
    </div>
</template>

<script>

export default {
  data() {
    return {
      menuDisplay: "none"
    };
  },
  methods: {
    openMenu() {
      this.menuDisplay = "inline";
    },
    closeMenu() {
      this.menuDisplay = "none";
    },
    clickMenu() {
      if (this.menuDisplay == "none") {
        this.openMenu();
      } else {
        this.closeMenu();
      }
    }
  }
};
</script>


<style scoped>
div {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding-right: 30px;
  position: relative;
}

img {
  width: 45px;
  border-radius: 100%;
  margin-right: 12px;
}

.linkMenu {
  font-weight: normal;
  font-size: 50px;
  padding: 30px 0 0 25px;
  color: #b5b5b5;
}

a:hover {
  cursor: pointer;
}

.linkMenu:active,
.linkMenu:visited {
  color: #b5b5b5;
}

.menu {
  display: inline;
  position: absolute;
  top: 100px;
  right: 12px;
  list-style: none;
  width: 210px;
  padding: 15px 5px;
  border-radius: 5px;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

/******** SETINHA EM CIMA DO MENU**************/
.menu:after {
  border-bottom: 10px solid white;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  top: -10px;
  content: "";
  position: absolute;
  right: 5%;
  margin-left: -21px;
  width: 0;
  height: 0;
}
/**********************/
.menu li {
  padding: 12px;
  margin: 5px;
  border-radius: 5px;
  position: relative;
}

.menu li a {
  display: block;
  width: 100%;
  padding-left: 30px;
}

.menu li:hover {
  background-color: #f6f7f8;
}

/********ICONES DO MENU********/

.menu li:nth-of-type(1)::before {
  background: url("../../assets/geral.svg") no-repeat;
}

.menu li:nth-of-type(2)::before {
  background: url("../../assets/editar.svg") no-repeat;
}

.menu li:nth-of-type(3)::before {
  background: url("../../assets/reenviar.svg") no-repeat;
}

.menu li:before {
  content: "";
  position: absolute;
  width: 20px;
  height: 30px;
  margin-left: -2px;
}
</style>
