<template>
  <div>
    <div class="background">
      <Navbar></Navbar>
      <v-container>
        <v-layout row wrap align-center>
        <v-flex v-for="project in this.projects" :key="project.id" sml12 md6 lg4 xl4>
          <ProjectCard :name=project.name :description=project.description :icon=project.icon :url=project.url></ProjectCard>
        </v-flex>
        </v-layout>
      </v-container>
    </div>
    <div class="banner">
      <p> Banner para propaganda </p>
    <div id="adsgoeshere" style="background: grey; padding-top: 20px; text-align: center;" v-html="adsenseContent"></div>
    </div>
  </div>
</template>

<script>
import ProjectCard from './components/ProjectCard'
import Navbar from './components/Navbar'

export default {
  name: 'App',
  components: {
    ProjectCard,
    Navbar,
  },
  data(){
    return{
    projects:[
        {
          url: 'https://lurkasf.github.io/Anagrama/',
          name: 'Anagrama',
          icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png',
          description:'Jogo do Anagrama o qual consiste em descobrir qual é a palavra que está embaralhada'},
      ],
      adsenseContent: ''
    }
  },
  mounted(){
    this.adsenseContent = document.getElementById('divadsensedisplaynone').innerHTML
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
html{
  background-color: #2d4c66;
  height: auto !important;
  min-height: 100%
}
.cardList{
  display: flex;
  flex-direction: row;
  flex-flow: row;
  align-items: center;
  justify-content: center;
}
div.banner { 
  right: 0px;
  padding-top: 10vh;
  position: fixed;
  text-align: center;
  top: 0px;
  float: right;  
  width: 100px;
  height: 400px; 
  background-color: grey;  
}

#adsgoeshere{
  background: white;
}

</style>
