<template>
  <div id="app">
    <div class="profile">
      <ProfilePicComponent/>
      <IconComponent/>
    </div>
    <div class="about">
      <AboutComponent/>
      <SkillComponent/>
    </div>
  </div>
</template>

<script>
import ProfilePicComponent from './components/ProfilePic.vue'
import AboutComponent from './components/About.vue'
import SkillComponent from './components/Skill.vue'
import IconComponent from './components/Icon.vue'

export default {
  name: 'App',
  components: {
    AboutComponent,
    ProfilePicComponent,
    SkillComponent,
    IconComponent
  }
};
</script>

<style scoped>
#app {
  width: 890px;
  height: 540px;
  border-radius: 19px;
  background-color: var(--backgroud-color-panel);
  display: flex;
  align-items: center;
}

#app > .profile {
  flex:1;
}

#app > .about {
  flex:2;
}


</style>
