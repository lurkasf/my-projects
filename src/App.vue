<template>
  <div>
    <div class="background">
      <Navbar @switch-ads="switchAds"></Navbar>
      <v-container>
        <v-layout row wrap align-center>
        <v-flex v-for="project in this.projects" :key="project.id" sml12 md6 lg4 xl4>
          <ProjectCard :name=project.name :description=project.description :icon=project.icon :url=project.url></ProjectCard>
        </v-flex>
        </v-layout>
      </v-container>
    </div>
    <div v-if="adsEnabled" class="banner">
      <div data-mvc-banner="sky-wide" class="magazine-banner"></div>
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
    enableAds: false,
    projects:[
        {
          url: 'https://lurkasf.github.io/Anagrama/',
          name: 'Anagrama',
          icon:'https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png',
          description:'Jogo do Anagrama o qual consiste em descobrir qual é a palavra que está embaralhada'},
      ],
    }
  },
  computed:{
    adsEnabled(){
      return this.enableAds
    }
  },
  watch:{
    enableAds: function(newer){
      if(newer){
        this.startBanner('bluestorm')
      }
    }

  },
  methods:{
    startBanner(storename){
      var b = document.createElement('script')
      b.type = 'text/javascript'
      b.async = true
      b.src = 'https://www.magazinevoce.com.br/js/banner.js?store='+ storename
      var s = document.getElementsByTagName('script')[0]
      s.parentNode.insertBefore(b, s)
    },
    switchAds(value){
      this.enableAds = value
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
  right: 6px;
  position: fixed;
  text-align: center;
  top: 10%;
  float: right;  
  background-color: white;
}

</style>
