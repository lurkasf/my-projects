<template>
  <div class="card">
  <v-card max-width="375" outlined>
    <v-responsive class="pt-4">
      <v-img src="https://raw.githubusercontent.com/lurkasf/Anagrama/master/public/icon.png" height="100" width="100"></v-img>
      <v-card-text>
        <span class="subheading">{{name}}</span>
      </v-card-text>
    </v-responsive>

    
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="headline mb-1 title">{{name}}</v-list-item-title>
        <v-list-item-subtitle>{{description}}</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar>
    </v-list-item>

  </v-card>
  </div>
</template>

<script>
  export default {
    name: 'ProjectCard',
    props:['name', 'description'],

    data: () => ({
    }),
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
</style>