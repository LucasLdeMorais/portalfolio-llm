<template>
    <div id="conteudo">
        <div class="publicacao">
            <h3 class="titulo-publicacao">
                <slot name="titulo-publicacao"></slot>
            </h3>
            <div class="container-imagem-publicacao">
                <slot name="imagem-publicacao"></slot>
            </div>
            <p class="texto-publicacao">
                <slot name="texto-publicacao"></slot>
            </p>
        </div>
    </div>
</template>

<style scoped>
    #conteudo {
        width: 100%; 
        height: fit-content; 
        min-width: 300px;
        min-height: 505px;
        max-height: 475px; 
        overflow-y: auto;
        display: inline-flex;   
    }

    .publicacao {
        width: 100%;
        margin: 33px;
    }

    .titulo-publicacao {
        color: #FF001C;
        text-align: center;
        margin: 0 auto;
    }

    .container-imagem-publicacao {
        margin: 30px auto;
        min-width: 234px;
        max-width: 450px;
    }

    .texto-publicacao {
        font-size: medium;
        text-align: justify;
        color: #FF001C;
    }

    @media (max-width:641px)  {
        #conteudo {
            max-height: unset;
        }
    }
</style>