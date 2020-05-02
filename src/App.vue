<template>
  <div class="background">
    <Navbar></Navbar>
    <v-container>
      <v-layout row wrap align-center>
      <v-flex v-for="project in this.projects" :key="project.id" sml12 md6 lg6 xl6>
        <ProjectCard :name=project.name :description=project.description :icon=project.icon :url=project.url></ProjectCard>
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
        {url: 'https://lurkasf.github.io/Anagrama/', name: 'Anagrama', description:'wtf, that´s a game', icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png'},
        {url: '#', name: 'Exemplo', description:'wtf, that´s an example', icon:'https://previews.123rf.com/images/fordzolo/fordzolo1506/fordzolo150600296/41026708-example-white-stamp-text-on-red-backgroud.jpg'},
        {url: '#', name: 'Exemplo', description:'wtf, that´s an example', icon:'https://previews.123rf.com/images/fordzolo/fordzolo1506/fordzolo150600296/41026708-example-white-stamp-text-on-red-backgroud.jpg'},
        {url: '#', name: 'Exemplo', description:'wtf, that´s an example', icon:'https://previews.123rf.com/images/fordzolo/fordzolo1506/fordzolo150600296/41026708-example-white-stamp-text-on-red-backgroud.jpg'},
        {url: '#', name: 'Exemplo', description:'wtf, that´s an example', icon:'https://previews.123rf.com/images/fordzolo/fordzolo1506/fordzolo150600296/41026708-example-white-stamp-text-on-red-backgroud.jpg'},
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
