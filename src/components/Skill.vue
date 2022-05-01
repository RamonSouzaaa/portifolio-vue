<template>
  <div id="skill">
      <h2>Habilidades</h2>
      <ul>
          <li><Icon icon="akar-icons:html-fill" class="icon"/></li>
          <li><Icon icon="akar-icons:css-fill" class="icon"/></li>
          <li><Icon icon="uil:java-script" class="icon"/></li>
          <li><Icon icon="bxl:java" class="icon"/></li>
      </ul>
  </div>
</template>

<script>
    import { Icon } from '@iconify/vue';
    export default {
        name:'SkillComponent',
        components: {
            Icon
        }
    }
</script>

<style scoped>
    #skill{
        color:white;
        border:1px solid white;
    }

    #skill > h2{
        font-family: "Rubik-Medium";
    }

    #skill > ul  {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }

    #skill > ul > li {
        display: inline;
    }

    #skill > ul > li >.icon{
        width: 48px;
        height: 50px;
        padding:0px 7px 0px 7px;
        border:1px solid white;
    }
</style>