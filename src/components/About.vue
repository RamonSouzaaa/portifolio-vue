<template>
  <div id="about">
      <article>
        <h2>{{title}}</h2>
        <p>{{text}}</p>
      </article>
  </div>
</template>

<script>
    export default {
        name: 'AboutComponent',
        props: {
            title: String,
            text: String
        },
        data(){
            return {
                
            }
        }
    };
</script>

<style scoped>
    #about > article {
        color: var(--color-text);
    }

    #about > article > h2 {
        font-family: "Rubik-Medium";
        color: var(--color-text);
    }

    #about > article > p {
        font-family: "Rubik-Regular";
        word-spacing: 5px;
        line-height: 1.6;
        margin-right:50px;
        color: var(--color-text);
    }

    @media screen and (max-width: 840px) {
        #about{
            padding:0px 10px 0px 10px;
        } 

        #about > article > p {
            margin-right:0px;
        }
    }
</style>