<template>
    <form>
        
        <h3 class="form_header">INFORMAÇÕES CADASTRAIS</h3>            

       <div class="personal_infor">

        <div class="razao_social">
        <label for="razao_social"> Razão social </label>
        <input type="text" name="razao_social">
        </div>

        <div class="nome_fantasia">
        <label for="nome_fantasia"> Nome fantasia </label>
        <input type="text" name="nome_fantasia">
        </div>
        
        <div class="cnpj">
        <label for="cnpj"> CNPJ </label>
        <input type="text" name="cnpj">
        </div>
        
        <div class="telefone">
        <label for="telefone"> Telefone </label>
        <input type="tel" name="telefone">
        </div>   

        </div>  
    
        <h3 class="form_header">INFORMAÇÕES CADASTRAIS</h3>

        <div class="profile_checkboxes_container">
        <div>
        <input type="checkbox" id="profile_check1" name="profile_check" value=""> <label for="profile_check1">Check 1</label>
        </div>
        <div>
        <input type="checkbox" id="profile_check2" name="profile_check" value=""> <label for="profile_check2">Check 2</label>
        </div>
        </div>

         <h3 class="form_header">USUÁRIOS MASTERS</h3>
         
        
        <div class="liberar_pontos_container">
            <div class="check_liberar_pontos">
                <h4>Liberar pontos</h4>
                <p>A Bonitour oferece pontos dos agentes que podem
                    ser trocados por presentes.
                </p>
            </div>

            <div class="check_liberar_pontos">
                 <h4>Não liberar pontos</h4>
                <p>Nessa opção não libera pontuação e os agentes não poderão trocar.
                </p>
            </div>
        </div>

         <h3 class="form_header">USUÁRIOS MASTERS</h3>
        
        <div class="usuarios_masters_container">
         <div>
             <img src="@/assets/usuario master 1.jpg">
          
             <h6> Thiago Santos </h6>
             <p> thiago.santos@gmail.com </p>
             <span></span> 
         </div>
         <div>
             <img src="@/assets/usuario master 2.jpg">
           
             <h6> Mariana Silva </h6>
             <p> mariana.silva@gmail.com </p>  
              <span></span>      
         </div> 
       </div> 
         
    </form>
</template>


<style scoped>
form {
  background-color: #ffffff;
  border-radius: 10px;
  padding: 15px 25px;
}

.form_header {
  padding: 25px 0;
}

.personal_infor {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: repeat(2, fr);
  grid-template-areas:
    "razao_social nome_fantasia"
    "cnpj telefone";
  grid-gap: 10px;
}

.personal_infor label {
  display: block;
}

.razao_social {
  grid-area: razao_social;
}
.nome_fantasia {
  grid-area: nome_fantasia;
}
.cnpj {
  grid-area: cnpj;
}
.telefone {
  grid-area: telefone;
}

input[type="text"],
input[type="tel"] {
  width: 350px;
  padding: 8px;
  border: 1px solid gray;
  box-shadow: none;
  border-radius: 5px;
}

.profile_checkboxes_container {
  display: flex;
  justify-content: space-around;
}

.profile_checkboxes_container div {
  width: 50%;
}

.liberar_pontos_container {
  display: flex;
  justify-content: space-between;
}
.liberar_pontos_container div {
  width: 50%;
  margin: 5px;
  padding: 20px;
  border: 1px solid #c7c7c7;
  border-radius: 8px;
}

.usuarios_masters_container {
  display: flex;
  flex-flow: column;
  justify-content: center;
}

.usuarios_masters_container div {
  border: 1px solid black;
  padding: 15px;
  display: grid;
}

.usuarios_masters_container div span:after {
  content: "\2807";
  font-size: 20px;
  color: #acabab;
}

.usuarios_masters_container div img {
  width: 12%;
  height: 12%;
  border-radius: 100%;
}
</style>
