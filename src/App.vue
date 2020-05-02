<template>
  <div class="background">
    <Navbar></Navbar>
    <v-container>
      <v-layout row wrap>
      <v-flex v-for="project in this.projects" :key="project.id">
        <ProjectCard :name=project.name :description=project.description :icon=project.icon></ProjectCard>
      </v-flex>
      </v-layout>
    </v-container>
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
        {name: 'Anagrama', description:'wtf, that´s a game', icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png'},
        {name: 'Anagrama2', description:'wtf, that´s an example', icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png'},
        {name: 'Anagrama3', description:'wtf, that´s an example', icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png'},
      ]
    }
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

  background-color: #242c33;
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

</style>
