<template>
    <form>
        
        <h3 class="form_header">INFORMAÇÕES CADASTRAIS</h3>            
        <a class="linkMenu"></a>         

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
          <label>Check 1
          <input type="checkbox" id="profile_check1" value=""> 
          <span class="checkmark"></span>
          </label>
          
          <label>Check 1
          <input type="checkbox" id="profile_check2" value=""> 
          <span class="checkmark"></span>
          </label>
        </div>

         <h3 class="form_header">USUÁRIOS MASTERS</h3>
         
        
        <div class="liberar_pontos_container">
            <div class="check_liberar_pontos">
               <icon-passeios class="icon_passeios"></icon-passeios>
                  <h4>Liberar pontos</h4>
                <p>A Bonitour oferece pontos dos agentes que podem
                    ser trocados por presentes.
                </p>
            </div>

            <div class="check_liberar_pontos">
               <icon-passeios class="icon_passeios"></icon-passeios>
                 <h4>Não liberar pontos</h4>
                <p>Nessa opção não libera pontuação e os agentes não poderão trocar.
                </p>
            </div>
        </div>

        <h3 class="form_header">USUÁRIOS MASTERS</h3>
        
        <div class="usuarios_masters_container">
         <div>
             <img src="@/assets/usuario master 1.jpg">
          
             <h3> Thiago Santos </h3>
             <p> thiago.santos@gmail.com </p>
             <a @click="clickMenuu(1)">
               <nav :class="{teste: UserMasterMenu === 1}">
               <ul>
                 <li><a>Tornar principal</a></li>
                 <li><a>Visualizar perfil</a></li>
               </ul>
             </nav>
             </a>
             
         </div>
         <div>
             <img src="@/assets/usuario master 2.jpg">
           
             <h3> Mariana Silva </h3>
             <p> mariana.silva@gmail.com </p>  
             <a @click="clickMenuu(2)">
                <nav :class="{teste: UserMasterMenu === 2}">
               <ul>
                 <li><a>Tornar principal</a></li>
                 <li><a>Visualizar perfil</a></li>
               </ul>
             </nav>
             </a>     
         </div> 
       </div> 
         
    </form>
</template>

<script>
import IconPasseios from "@/components/icons/IconPasseios.vue";

export default {
  components: {
    IconPasseios
  },
  data() {
    return {
      UserMasterMenu: "" // VARIÁVEL PARA SELECIONAR DE MENU DE ACORDO COM A ORDEM DOS USUARIOS
    };
  },
  methods: {
    clickMenuu(ordemUser) {
      if (this.UserMasterMenu != ordemUser) {
        this.UserMasterMenu = ordemUser;
      } else {
        this.UserMasterMenu = "";
      }
    }
  }
};
</script>


<style scoped>
.teste {
  display: inline !important;
}

form {
  background-color: #ffffff;
  border-radius: 10px;
  padding: 15px 25px;
}

.form_header {
  padding: 25px 0;
  color: #666666;
  font-weight: normal;
}

/***********************  PERSONAL INFORMATION *****************/

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
  font-size: 14px;
}

input[type="text"],
input[type="tel"] {
  width: 350px;
  padding: 8px;
  border: 1px solid #d5d5d5;
  box-shadow: none;
  border-radius: 5px;
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

label {
  color: #797979;
}

/*******************  PROFILE CUSTOM CHECKBOXES  ************************/

.profile_checkboxes_container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.profile_checkboxes_container label {
  position: relative;
  padding-left: 35px;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.profile_checkboxes_container label:nth-of-type(1) {
  margin-right: 290px;
}

.profile_checkboxes_container label input {
  opacity: 0;
  position: absolute;
  cursor: pointer;
}

.profile_checkboxes_container label span {
  position: absolute;
  top: 0;
  left: 0;
  height: 25px;
  width: 25px;
  border: 0.5px solid #c1c0c0;
  border-radius: 5px;
  background-color: #fff;
}

.profile_checkboxes_container label input:checked ~ span {
  background-color: #fff;
}

.profile_checkboxes_container label span:after {
  content: "";
  position: absolute;
  display: none;
}

.profile_checkboxes_container label input:checked ~ span:after {
  display: block;
}

.profile_checkboxes_container label span:after {
  left: 9px;
  top: 5px;
  width: 5px;
  height: 10px;
  border: solid #b6b5b5;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}

/*************** CHECKBOXES LIBERAR PONTOS  *******************/

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
  color: #9d9d9d;
  display: grid;
  grid-template-columns: auto 1fr;
  grid-template-rows: 1fr 1fr;
  grid-template-areas:
    "photo header"
    "photo text";
  grid-gap: 5px;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
}

.liberar_pontos_container div:hover {
  cursor: pointer;
  border: 2px solid #ffbf7f;
}

.liberar_pontos_container div .icon_passeios {
  width: 50px;
  grid-area: photo;
}

.liberar_pontos_container div h4 {
  grid-area: header;
}

.liberar_pontos_container div p {
  font-size: 12px;
  grid-area: text;
}

/*******************  USUARIOS MASTER CONTAINER  **********************/

.usuarios_masters_container {
  display: flex;
  flex-flow: column;
  justify-content: center;
}

.usuarios_masters_container div {
  border: 1px solid black;
  padding: 15px;
  margin: 10px 0;
  border: 1px solid #bfbfbf;
  border-radius: 10px;
  display: grid;
  grid-template-columns: 100px 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-template-areas:
    "photo name btnMenu"
    "photo email btnMenu";
  align-items: center;
}

.usuarios_masters_container div img {
  width: 70px;
  margin-left: 10px;
  border-radius: 100%;
  grid-area: photo;
}

.usuarios_masters_container div > a:after {
  content: "\2807"; /* TRÊS PONTOS NO FINAL DO CONTAINER */
  font-size: 30px;
  color: #acabab;
}

.usuarios_masters_container div h3 {
  grid-area: name;
  color: #5b5b5b;
  font-weight: normal;
}

.usuarios_masters_container div p {
  grid-area: email;
  color: #d1d1d1;
}

.usuarios_masters_container div > a {
  grid-area: btnMenu;
  justify-self: end;
  cursor: pointer;
  position: relative;
}
/******MENU DOS USUARIOS MASTER*******/
.usuarios_masters_container div nav {
  display: none;
  box-shadow: 0 1px 8px 0 rgba(0, 0, 0, 0.2), 0 1px 20px 0 rgba(0, 0, 0, 0.19);
  background-color: white;
  width: 180px;
  position: absolute;
  top: -120px;
  right: 0;
  border-radius: 8px;
}
/*******SETINHA EMBAIXO DO MENU*********/
.usuarios_masters_container div nav:after {
  border-top: 10px solid white;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  bottom: -10px;
  content: "";
  position: absolute;
  right: 5%;
  margin-left: -21px;
  width: 0;
  height: 0;
}

.usuarios_masters_container div nav ul {
  list-style: none;
  padding: 10px;
}

.usuarios_masters_container div nav ul li {
  padding: 10px;
  margin: 5px 0;
}

.usuarios_masters_container div nav ul li:hover {
  background-color: #f6f7f8;
}

.usuarios_masters_container div nav ul li a {
  font-size: 14px;
  color: #8d8d8d;
  text-decoration: none;
  padding-left: 30px;
}

.usuarios_masters_container div nav ul li::before {
  content: "";
  position: absolute;
  width: 20px;
  height: 30px;
  margin-left: -2px;
}

.usuarios_masters_container div nav ul li:nth-of-type(1)::before {
  background: url("../../assets/geral.svg") no-repeat;
}

.usuarios_masters_container div nav ul li:nth-of-type(2)::before {
  background: url("../../assets/editar.svg") no-repeat;
}

/*******SMALL SCREENS**********/

@media (max-width: 640px) {
  .personal_infor {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, fr);
    grid-template-areas:
      "razao_social"
      "nome_fantasia"
      "cnpj"
      "telefone";
    grid-gap: 10px;
  }

  .liberar_pontos_container {
    flex-flow: column;
    justify-content: space-between;
  }

  .liberar_pontos_container div {
    margin: 5px;
    padding: 20px;
    width: 100%;
  }
}
</style>
