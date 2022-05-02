<template>
  <div id="app">
    <div class="utils">
      <Icon :icon="mode" class="iconMode" @click="modifyMode()"/>
      <Icon icon="openmoji:flag-brazil" class="icon" id="iconBr" @click="modifyLang()"/>
      <Icon icon="openmoji:flag-united-states" class="icon" id="iconEn" @click="modifyLang()"/>
    </div>
    <div class="container">
      <div class="profile">
        <ProfilePicComponent :title="titleProfileDefault"/>
        <IconComponent/>
      </div>
      <div class="line"></div>
      <div class="about">
        <AboutComponent :title="titleAboutDefault" :text="textAboutDefault"/>
        <SkillComponent :title="textSkillDefault"/>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";
import ProfilePicComponent from "./components/ProfilePic.vue";
import AboutComponent from "./components/About.vue";
import SkillComponent from "./components/Skill.vue";
import IconComponent from "./components/Icon.vue";
import moment from "moment";

export default {
  name: "App",
  components: {
    AboutComponent,
    ProfilePicComponent,
    SkillComponent,
    IconComponent,
    Icon,
  },
  data(){
    return {
      lang: 'en',
      modeLight: 'clarity:moon-solid',
      modeDark: 'bi:sun-fill',
      mode: '',
      titleAboutPtBr: `Olá, tudo bem?`,
      textAboutPtBr: `Me chamo Ramon tenho 23 anos, sou desenvolvedor de software pleno na
          empresa Thomson Reuters Brasil desde 2017 quando iniciei minha
          carreira como programador. Gosto de estudar novas tecnologias e
          aprimorar meus conhecimentos, com isso conclui alguns projetos que
          consegui na internet. Tenho conhecimento em banco de dados relacional,
          desenvolvimento de aplições web e desktop utilizando orientação a
          objetos.`,
      titleAboutEn: `Hi!`,
      textAboutEn: `My name is Ramon, I'm 23 years old, I've been a full-time 
               software developer at Thomson Reuters Brasil since 2017 when
               I started my career as a programmer. I like to study new technologies 
               and my knowledge, with that I complete some projects that I got 
               on the internet. I have knowledge in relational database, web and 
               desktop application development using object orientation.`,
      titleSkillPtBr: `Habilidades`,
      titleSkillEn: `Skills`,
      titleProfilePtBr: `Desenvolvedor de Software`,
      titleProfileEn: `Software developer`,
      titleAboutDefault: '',
      textAboutDefault: '',
      textSkillDefault: '',
      titleProfileDefault: ''
    }
  },
  methods: {
    calcAge() {
      let a = moment();
      let b = moment("1998-12-30");
      return a.diff(b, "years");
    },
    modifyLang(){
      if(this.lang === 'en'){
        document.getElementById('iconEn').style.borderBottom = '0';
        document.getElementById('iconBr').style.borderBottom = '2px solid var(--color-text)';
        this.titleAboutDefault = this.titleAboutPtBr
        this.textAboutDefault = this.textAboutPtBr
        this.textSkillDefault = this.titleSkillPtBr
        this.titleProfileDefault = this.titleProfilePtBr
        this.lang = 'pt'
      }else{
        document.getElementById('iconBr').style.borderBottom = '0';
        document.getElementById('iconEn').style.borderBottom = '2px solid var(--color-text)';
        this.titleAboutDefault = this.titleAboutEn
        this.textAboutDefault = this.textAboutEn
        this.textSkillDefault = this.titleSkillEn
        this.titleProfileDefault = this.titleProfileEn
        this.lang = 'en'
      }
    },
    modifyMode(){
      document.querySelector('html').classList.toggle('dark-mode')
      this.mode = this.mode === this.modeDark ? this.modeLight : this.modeDark
    }
  },
  created(){
    this.titleAboutDefault = this.titleAboutPtBr
    this.textAboutDefault = this.textAboutPtBr
    this.textSkillDefault = this.titleSkillPtBr
    this.titleProfileDefault = this.titleProfilePtBr
    this.mode = this.modeDark
  },
  mounted(){
    this.modifyLang()
  }
};
</script>

<style scoped>
#app > .utils {
  display: flex;
  width: 97%;
  padding: 5px 0px 5px;
  justify-content: flex-end;
}

#app > .utils > .icon {
  width: 25px;
  height: 25px;
  
}

#app > .utils > .iconMode {
  width: 20px;
  height: 20px;
  color: var(--color-text);
  margin:3px 10px 0px 0px;
}

#app {
  width: 914px;
  height: 540px;
  border-radius: 19px;
  background-color: var(--backgroud-color-panel);
}

#app > .container {
  display: flex;
}

#app > .container > .line {
  border-left: 2px solid var(--color-text);
  height: 457px;
}
#app > .container > .profile {
  flex: 1;
}

#app > .container > .about {
  flex: 2;
  margin-left: 30px;
  display: flex;
  flex-direction: column;
}

@media screen and (max-width: 944px) {
  #app {
    width: 95%;
    margin: 0 auto;
  }
}

@media screen and (max-width: 840px) {
  #app {
    width: 100%;
    height: auto;
    margin: 0;
    border-radius: 0;
  }

  #app > .container {
    flex-direction: column;
    padding-bottom: 20px;
    padding-top: 60px;
  }

  #app > .container > .about {
    margin-top: 50px;
    margin-left: 0px;
  }

  #app > .container > .line {
    display: none;
  }
}
</style>
