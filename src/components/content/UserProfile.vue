<template>
  <div>
       <img src="@/assets/photo_profile.jpg" alt="">
       <p class="name"> Thiago Santos </p>
       <p class="usuario_ativo">Usuário ativo</p>
       <a href="#" class="login_facebook">Login com Facebook</a>
       <a href="#" class="login_google">Login com Google</a>
  </div>
</template>



<style scoped>
div {
  width: inherit;
  background-color: #ffffff;
  border-radius: 10px;
  display: flex;
  flex-flow: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}

img {
  width: 120px;
  border-radius: 100%;
}

.name {
  color: #575757;
  font-size: 22px;
}

.usuario_ativo {
  color: #a1a1a1;
  font-size: 14px;
}

a {
  border-radius: 5px;
  padding: 5px 40px;
  width: 100%;
  text-decoration: none;
  font-size: 14px;
}

.login_facebook {
  border: 1.5px solid #7f9ad1;
  color: #7f9ad1;
}

.login_google {
  border: 1.5px solid #e57370;
  color: #e57370;
}

/******SMALL SCREENS******/

@media (max-width: 640px) {
  a {
    width: inherit;
  }
}
</style>
