<script setup lang="ts">
    import Conteudo from './Conteudo.vue'
</script>

<template>
    <Conteudo>
        <template #titulo-publicacao>
            Seja bem-vindo ao meu site!!!
        </template>
        <template #imagem-publicacao>
            <img src="../assets/foto.jpg" width="100%"/>
        </template>
        <template #texto-publicacao>
            Sou Lina, cantora e artista apaixonada pela arte de expressar emoções através da música. 
            Este site é mais do que um mero currículo; é um portal que reflete minha jornada artística, repleto de momentos, canções e experiências que 
            moldaram quem sou.
            <br><br>
            Explore as diferentes seções para conhecer melhor meu trabalho, desde performances envolventes até projetos artísticos que marcaram minha
            trajetória. Este espaço virtual é um convite para você mergulhar na minha paixão pela música e descobrir a diversidade de sons e sentimentos que
            compartilho com o mundo.
            <br><br>
            Agradeço por sua visita e espero que esta plataforma seja uma porta de entrada para momentos musicais inesquecíveis. Sinta-se à vontade para
            explorar, conectar-se e, quem sabe, compartilhar essa jornada musical comigo. Obrigada por fazer parte deste encontro entre arte e audiência. 
            Espero que a música nos conecte de maneiras únicas!
        </template>
    </Conteudo>
</template>