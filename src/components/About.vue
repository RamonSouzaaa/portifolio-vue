<template>
  <div id="about">
      <article>
        <h2>Olá, tudo bem?</h2>
        <p>
          Me chamo Ramon tenho 23 anos, sou desenvolvedor de software pleno na
          empresa Thomson Reuters Brasil desde 2017 quando iniciei minha
          carreira como programador. Gosto de estudar novas tecnologias e
          aprimorar meus conhecimentos, com isso conclui alguns projetos que
          consegui na internet. Tenho conhecimento em banco de dados relacional,
          desenvolvimento de aplições web e desktop utilizando orientação a
          objetos.
        </p>
      </article>
  </div>
</template>

<script>
    export default {
        name: 'AboutComponent'
    };
</script>

<style scoped>
    #about > article {
        color: var(--color-light);
        border:1px solid white;
    }

    #about > article > h2 {
        font-family: "Rubik-Medium";
    }

    #about > article > p {
        font-family: "Rubik-Regular";
        word-spacing: 5px;
    }
</style>