<template>
    <aside>

        <nav>

            <ul>
                <li><a href="#"><img src="@/assets/editar.svg"></a></li>
                <li><a href="#"><img src="@/assets/conta.svg"></a></li>
                
              
            </ul>

        </nav>

    </aside>
</template>

<script>
export default {};
</script>


<style scoped>
aside {
  background-color: #ffffff;
  border: 1px solid #e5e7e8;
  padding: 15px 0;
}

ul {
  list-style: none;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
}

ul li {
  padding: 10px;
}

ul li a img {
  width: 25px;
}

</style>
