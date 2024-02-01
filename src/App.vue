<script setup lang="ts">
  import { onMounted } from 'vue';
  import { RouterLink, RouterView } from 'vue-router'

  const timeZone = Intl.DateTimeFormat().resolvedOptions().timeZone;
  let time: String;

  onMounted(() => {
    setInterval(() => {
      time = new Date().toLocaleString("pt-BR", {timeZone: timeZone})
    }, 1000)
  })
</script>

<template>
  <header>
    <div id="caixa-logo">
      <RouterLink id="link-logo" to="/sobremim"><img alt="lina-logo" id="logo" src="./assets/LogoLina.png"/></RouterLink> 
    </div>
    <div>
      <span id="dataHora">{{ time }}</span>
    </div>
    <nav id="navegacao">
      <ul id="lista-items-navegacao">
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/sobremim">Sobre mim</RouterLink></li>
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/curriculo">Currículo</RouterLink></li>
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/galeria">Galeria</RouterLink></li>
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/audioteca">Audioteca</RouterLink></li>
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/videoteca">Videoteca</RouterLink></li>
        <li class="item-navegacao"><RouterLink class="link-item-navegacao" to="/contato">Contato</RouterLink></li>
      </ul>
    </nav>
  </header>
  <RouterView />
  <footer>
    <div>
      <p>Todos os direitos reservados sobre este site e seu conteúdo © Lina 2020 - 2024</p>
      <ul>
        <li> <a href="">Termos de Uso</a></li>
        <li>|</li>
        <li> <a href="">Política de Privacidade</a></li>
        <li>|</li>
        <li> <a href="">© Lina</a></li>
      </ul>
      <p>Feito com &lt;3 por L.L.M.</p>
    </div>
  </footer>
</template>

<style scoped>
  /* Header */
  header {
      border-top: 0px;
      display: block;
      width: 100%;
      position: relative;
      bottom: auto;
      top: 0;
      right: 0;
      background-color: #1f0b0c;
      z-index: 1000;
  }

  #caixa-logo  {
    display: block;
    padding: 15px;
    padding-bottom: 0;
    width: 200px;
    height: fit-content;
  }

  #dataHora {
    float: right;
    color: #FF001C;
  }

  #link-logo {
    display: inherit;
    width: inherit;
    height: inherit;
  }

  #logo  {
      width: 100%;
  }

  nav {
      width: 100%;
      border-top: 1px solid #FF001C;
      border-bottom: 1px solid #FF001C;
      display: block;
  }

  #lista-items-navegacao {
      margin: 0;
      padding: 0;
      height: inherit;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
  }

  #lista-items-navegacao > li {
      border-right: 1px solid #FF001C;
      height: 20px;
      min-width: fit-content;
      display: inline-block;
      position: relative;
      font-family: Arial, sans-serif;
      font-size: medium;
      color: #FF001C;
      padding: 0;
      top: 0;
      left: 0;
      bottom: auto;
      right: auto;
      text-align: center;
      flex: 1;
  }

  #lista-items-navegacao li:last-of-type {
      border-right: unset;
  }

  #lista-items-navegacao > li :hover{
      background-color: #FF001C;
      color: #231722;
  }

  #lista-items-navegacao > li > a{
      position: relative;
      display: inline-block;
      height: 100%;
      width: 100%;
      font-family: Arial, sans-serif;
      font-size: medium;
      color: #FF001C;
      text-decoration: none;
      min-width: 88px;
  }

  @media screen and (max-width: 355px) {
    #lista-items-navegacao :nth-child(n+4){
      border-top: 1px solid #FF001C;  
    }

    #lista-items-navegacao :nth-child(3){
      border-right: unset;
      padding-right: 1px;
    }

    #lista-items-navegacao :nth-child(4){
      border-right: 1px solid #FF001C;
    }
  }

  @media screen and (min-width: 356px) and (max-width: 444px) {
    #lista-items-navegacao :nth-child(4){
      border-right: unset;
      padding-right: 1px;
    }

    #lista-items-navegacao :nth-child(n+5){
      border-top: 1px solid #FF001C;
    }

    #lista-items-navegacao :nth-child(5){
      border-right: 1px solid #FF001C;
      border-bottom: unset;
    }
      
  }

  @media screen and (min-width: 445px) and (max-width: 532px) {
    #lista-items-navegacao > li {
      border-bottom: 1px solid #FF001C;
    }

    #lista-items-navegacao > li :hover{
      background-color: #FF001C;
      color: #231722;
    }
    
    #lista-items-navegacao :nth-child(5){
      border-right: unset;
      padding-right: 1px;
    }

    #lista-items-navegacao :last-child{
      border-bottom: unset;
    }
  }

  /* Footer */
  footer {
    border-top: 1px solid #FF001C;
    color: #FF001C;
    font-size: medium;
    width: 100%;
    height: 100px;
    position: relative;
    bottom: 0;
    top: auto;
    right: 0;
    min-height: 101px;
    background-color: #1f0b0c;
    z-index: 1000;
  }

  footer > div {
    position: relative;
    height: 100%;
    margin: 0;
    padding: 0 10px 0 10px;
  }

  footer > div > p:first-of-type{
    padding: 10px 0 10px 0;
  }

  footer > div > *{
    padding: 0 0 10px 0;
  }

  footer > div > p {
    margin: 0;
    text-align: center;
  }

  footer > div > p:nth-of-type(2){
    text-align: right;
  }

  footer > div > ul {
    display: flex;
    height: fit-content;
    width: fit-content;
    margin: 0 auto;
    list-style: none;
  }

  footer > div > ul > li {
    display: inline-block;
    height: fit-content;
    padding: 0;
    margin-right: 10px;
  }

  footer > div > ul > li > a {
    color: #FF001C;
  }

  @media screen and (max-width: 340px) {
    footer > div > ul > li{
      font-size: x-small;
    }
  }

  @media (max-width:586px)  { /* smartphones, iPhone, portrait 480x320 phones */ 
    footer > div > *{
      font-size: smaller;
    }
  }

  @media (max-width:641px)  { /* portrait tablets, portrait iPad, landscape e-readers, landscape 800x480 or 854x480 phones */ 
    footer {
      position: sticky;
    }

    #caixa-logo {
         margin: auto auto;
         width: 150px;
     }

    header {
      position: sticky;
    }
  }



</style>
