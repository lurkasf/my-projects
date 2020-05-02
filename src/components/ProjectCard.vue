<template>
  <div class="card">
  <v-card v-on:click="viajar(url)" hover shaped>
    <v-responsive class="pt-4">
      <v-img :src=icon height="150" width="150"></v-img>
    </v-responsive>

    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="headline mb-1 title">{{name}}</v-list-item-title>
        <v-list-item-subtitle class="description">{{description}}</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar>
    </v-list-item>

  </v-card>
  </div>
</template>

<script>
  export default {
    name: 'ProjectCard',
    props:['name', 'description', 'icon', 'url'],

    data: () => ({
    }),
    methods:{
      viajar(url){
        //this.console.log(url)
        window.open(url);
      }
    }
  }
</script>

<style scoped>
.card{
  padding: 10px;
}

.title{
  font-weight: bold;
  font-size: 300%;
}
.description{
  font-size: 150%;
}
</style>