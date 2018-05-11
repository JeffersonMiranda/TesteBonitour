<template>
    <nav>

      <ul>
          <li><a href="#">Roteiro Fácil</a></li>
          <li><a href="#">Pacote dinâmico</a></li>
          <li><a href="#">Agentes</a></li>
          <li><a href="#">Roteiros</a></li>
          <li><a href="#">Comissão</a></li>
          <li><a href="#">Prêmios</a></li>
      </ul>

    </nav>
</template>

<script>
export default {};
</script>


<style scoped>
ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
}
ul li {
  padding: 0 12px;
  height: 100%;
}

ul li a {
  text-decoration: none;
  color: #7c7c7c;
}

ul li a:hover {
  color: #ff8000;
}

@media (max-width:640px){
    ul{
        flex-flow: column;

    }
    ul li {
  padding: 3px 0;
}

}

</style>
